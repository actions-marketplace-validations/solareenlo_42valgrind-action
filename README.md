# 42valgrind-action
This GitHub Action checks if your code passes valgrind leak checker, after each push.

## Usage
```yml
# .github/workflows/valgrind.yml
name: <workflow-name>
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
        flags: 'sh test_valgrind.sh'
```

And, you may choose to add a badge to your repo by adding the below to your `README.md`:
```markdown
![](https://github.com/<username>/<remote-name>/workflows/<workflow-name>/badge.svg)
```

## References
- [solareenlo/42valgrind-docker](https://github.com/solareenlo/42valgrind-docker)
