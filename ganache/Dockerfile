FROM node:20.17.0-alpine3.20

RUN npm install -g ganache-cli

CMD ["sh", "-c", "ganache-cli --host $HOST --port $PORT --networkId $NETWORK_ID --accounts $ACCOUNTS --defaultBalanceEther $DEFAULT_BALANCE_ETHER --gasLimit $GAS_LIMIT --gasPrice $GAS_PRICE"]
