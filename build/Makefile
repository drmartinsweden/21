default: build

test:
	@find ../testing_dist -type f -name "*.json"| while read x; do echo -n "$$x: "; make -s clean; /home/ubuntu/code/testing_dist/check_test.py --prefix /home/ubuntu/code/build/ --test $$x|tail -n1; done
	@eval make -s clean

atm:
	@cp ~/bank/bank.auth ~/atm/
	@./atm.py -s bank.auth -c bob.card -a bob -n 1000.00

bank:
	@rm ~/bank/bank.auth
	@./bank.py

build:
	@python -m compileall .
	@chmod 755 atm.pyc bank.pyc
	@mv atm.pyc atm
	@mv bank.pyc bank

clean:
	@rm -f batch AHQWELAB BAHTCMLN BKJVFPRF EDVMRVJV EFGKIXOA EJEVZOYQ HHFNPRAJ HXVRIRTR IXCXRKCE LOFGBVMC LOZUQIXZ OIGUORUO OUTXLQJP PIMJOOVL PJHBNMKK RIHTEKRM RSRYYXDZ RWQJHFBO SDLVGVOA SNZEPOTM TCBZXYQX TEVXVSSW TPWMVDMZ WYMQWRAQ XTVPDSWR XXVEXDDR YNYCUJZE YORHWDWE YPEMUGBB ZNJZSMEQ

#.PHONY: test clean build
