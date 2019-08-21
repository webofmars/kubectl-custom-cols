# kubectl-custom-cols

a kubectl plugin that help you customize output columns like a boss !

## Using kubectl-custom-cols

```sh
kubectl custom-cols -o <template name> <arguments>
```

ex:

```sh
kubectl custom-cols -o qos-class pods -l app=nginx
```

will output:

```sh
NAME                   QoS-Class    STATUS
web-front-0            BestEffort   Running
web-front-1            BestEffort   Running
web-back-0             Burstable    Running
```

## Install kubectl-custom-cols

### Manualy

* dowload the latest release
* copy `kubectl-custom-cols` script somewhere in your PATH
* copy templates in `$HOME/.kube/kube-custom-cols/templates`

### Via krew

To be done ...

## Customize kubectl-custom-cols

You can add you own templates in `$HOME/.kube/kube-custom-cols/templates` folder.

## Contributing

Please feel free to send a PR or open issues ta the original repo : https://github.com/webofmars/kubectl-custom-cols

You can send your own templates to be included in the default package
