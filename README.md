# playg-aries


## Setup
Init required repositories:

### VON netowrk with 4 nodes and Ledger browser
```
git clone https://github.com/bcgov/von-network.git
```

### Aries ACA-py framework
```
git clone https://github.com/hyperledger/aries-cloudagent-python
```

### Scripts and runners
```
git clone https://github.com/VladoDemcak/playg-aries.git
```


## Run
Change directory to playground with aries.
```
$ cd playg-aries/
```

1. Run indy network
```
$ ./ledger/run_von 
Creating von_node4_1     ... done
Creating von_webserver_1 ... done
Creating von_node1_1     ... done
Creating von_node3_1     ... done
Creating von_node2_1     ... done
Want to see the scrolling container logs? Run "./manage logs"
```

Open von_webserver_1 on http://localhost:8080/

2. Register Faber's DID on ledger
```
curl --location --request POST 'http://localhost:8080/register' \
--header 'Content-Type: application/json' \
--data-raw '{
   "did":"JdRkpwWwCBqjfcrsjAH1GT",
   "verkey":"AcFvnqBQUatQmU4kfc9R9XEci8HQfDRPutGFTwpdWUrZ"
}'
```

3. Run Faber's agent
```
$ ./agents/run_faber 
```

4. Run Alice's agent

```
$ ./agents/run_alice
```

5. Import Postman
