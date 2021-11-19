# 42valgrind-action
This GitHub Action checks if your code passes valgrind leak checker, after each push.

## Usage
```yml
# .github/workflows/valgrind.yml
on: [push, pull_request]

jobs:
  valgrind:
    runs-on: ubuntu-latest
    name: 42valgrind
    steps:
    - uses: actions/checkout@v2
    - name: 42valgrind Leak checker
      uses: solareenlo/42valgrind-action@v1.0.0
      with:
        flags: './a.out'
```

## References
- [solareenlo/42valgrind-docker](https://github.com/solareenlo/42valgrind-docker)
