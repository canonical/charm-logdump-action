# charm-logdump-action

GitHub Action for dumping logs and metadata related to a charm deployment. Currently only works with the microk8s provider.

## Usage

```yaml
      - name: Dump logs
        uses: canonical/charm-logdump-action@HEAD
        if: failure()
        with:
          app: hello-kubecon
```

## Configuration
Configuration is supplied through the `with` keyword.

| Property | Description                     |
| -------- | ------------------------------- |
| `app`    | Name of the app you are testing. Required |
| `model`  | Name of the model you are deploying to. Defaults to `testing`. |
| `operator` | Name of the deployed operator. Defaults to `modeloperator`. |