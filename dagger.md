# dagger

## Run ci on local

It will run the following step:
  - Lint Helm chart
  - Generate schema from `values.yaml`
  - Generate readme parameters from `values.yaml`


```bash
# When no need to get helm dependency from private registry
dagger call -m 'github.com/disaster37/dagger-library-go/helm@v2' --src . ci export --path .

# When need to get helm dependency from private registry
dagger call -m 'github.com/disaster37/dagger-library-go/helm@v2' --src . ci --registry  --registry-username env:SU_USERNAME --registry-password env:SU_PASSWORD -- export --path .
```

