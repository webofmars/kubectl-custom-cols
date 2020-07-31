# kubectl-custom-cols

A "kubectl get" replacement with customizable column presets.

Master you kubectl output like a JSONpath pro :-)

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

### Prereqs

If you're on Mac OS X, you may need to first run `brew install coreutils` to get the `realpath` function.

### Manually

* download the latest release
* copy `kubectl-custom-cols` script and the `templates` folder together, somewhere in your PATH

### Via krew

If you already have the [krew](https://github.com/kubernetes-sigs/krew) kubectl plugin manager  installed, you can just issue the following command:

`kubectl krew install custom-cols`

## Customize kubectl-custom-cols

You can add you own templates in the `templates` folder.

## Contributing

Please feel free to send a PR or open issues ta the original repo : <https://github.com/webofmars/kubectl-custom-cols>

You can send your own templates to be included in the default package
