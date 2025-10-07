# Simple postfix forwarder

## Usage

Enter client pod:

``` bash
kubectl -n postfix-relay exec -it postfix-client-pod -- bash
```

Run swaks:

``` bash
swaks --server smtp.postfix-relay.svc --port 25 --from admin@example.pl --to artur@example.pl --data "Subject: k8s swaks test\n\nok"
```
