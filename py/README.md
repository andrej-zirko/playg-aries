
## Run
0. Change directory to playground with aries. `$ cd playg-aries/`

1. Run indy network
` $ ./ledger/run_von `

2. Run tails server
` $ ./ledger/run_tails `

3. Register Faber's DID on ledger
```
curl --location --request POST 'http://localhost:8080/register' \
--header 'Content-Type: application/json' \
--data-raw '{
   "did":"JdRkpwWwCBqjfcrsjAH1GT",
   "verkey":"AcFvnqBQUatQmU4kfc9R9XEci8HQfDRPutGFTwpdWUrZ"
}'
```

4. Run Faber's agent `$ ./py/run_faber`

5. Run Alice's agent `$ ./py/run_alice`

6. Import Postman
