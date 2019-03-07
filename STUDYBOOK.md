# Usage of QuickstartServer

## sbt run

```sh
$ sbt "runMain com.example.QuickstartServer"
[warn] Multiple main classes detected.  Run 'show discoveredMainClasses' to see the list
[info] Running com.example.QuickstartServer 
Server online at http://127.0.0.1:8080/
```

## Http Request

```sh
$ curl http://127.0.0.1:8080/users                                                                                                              23:13:36
{"users":[]}                                                                                                                                                                                           

$ curl http://127.0.0.1:8080/users -X POST \                                                                                                                                           23:20:08
          -H "Content-Type: application/json" \
          -d "{\"name\": \"Takato Horikoshi\", \"age\": 29, \"countryOfResidence\": \"Japan\"}"
{"description":"User Takato Horikoshi created."}

$ curl http://127.0.0.1:8080/users
{"users":[{"age":29,"countryOfResidence":"Japan","name":"Takato Horikoshi"}]}⏎
```