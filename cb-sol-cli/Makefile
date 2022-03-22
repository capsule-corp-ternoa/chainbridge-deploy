SOL_URL=https://github.com/capsule-corp-ternoa/chainbridge-solidity
SOL_BRANCH="ternoa"

fetch-contracts:
	@echo " > \033[32mFetching chainbridge-solidity contracts... \033[0m "
	git clone ${SOL_URL} && cd chainbridge-solidity && git checkout ${SOL_BRANCH}

compile:
	cd chainbridge-solidity && npm install && npx truffle compile

install: fetch-contracts compile
	@echo " > \033[32mInstalling cb-sol-cli... \033[0m "
	npm link .

clean:
	rm -rf chainbridge-solidity/