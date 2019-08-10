# kubectl-format

a kubectl plugin that help you customize output columns like a boss !

## Using kubectl-format

```sh
kubectl format -o <template name> <arguments>
```

ex:

```sh
kubectl format -o qos-class pods -l app=nginx
```

wil output:

```sh
NAME                   QoS-Class    STATUS
web-front-0            BestEffort   Running
web-front-1            BestEffort   Running
web-back-0             Burstable    Running
```

## Install kubectl-format

### Manualy

* dowload the latest release
* copy `kubectl-format` script somewhere in your PATH
* copy templates in `$HOME/.kube/kube-format/templates`

### Via krew

To be done ...

## Customize kubectl-format

You can add you own templates in `$HOME/.kube/kube-format/templates` folder.

## Contributing

Please feel free to send a PR or open issues ta the original repo : https://github.com/webofmars/kubectl-format

You can send your own templates to be included in the default package
