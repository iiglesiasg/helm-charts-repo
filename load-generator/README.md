# Load Generator Helm Chart

This Helm chart is a lightweight way to configure and run the ELK Load Generator

It has two parts: a **Job** and a **ConfigMap**.

The **job** runs a Vegeta command. Vegeta is an HTTP load testing tool built out of a need to drill HTTP services with a constant request rate.
```
echo 'POST http://adapter-helm:8090/MONADTST/testhttp' | vegeta attack -rate=2 -duration=900s -body=${BODY} -header='Content-Type: application/json'| vegeta encode | tee results.bin | vegeta report
```

The **ConfigMap** contains the body for the POST request.

https://github.com/tsenart/vegeta
