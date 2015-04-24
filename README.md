# pip v0.1.0


[pip](http://pip.pypa.io) requirements.txt generator for [Crystal](http://crystal.sh)


# Usage

## Schema

```yaml
dependencies:         # array of objects
  $name: $version     # string
```


## Example

```yaml
name: pip-test
version: 0.1.0
description: pip test

generators:
  pip:
    spec:
      dependencies:
        Flask: '0.8'
        Jinja2: '2.6'
        Werkzeug: '0.8.3'
        certifi: '0.0.8'
        chardet: '1.0.1'
        distribute: '0.6.24'
        gunicorn: '0.14.2'
        requests: '0.11.1'
    version: latest

scripts:
  run:
    - pip install -r lib/requirements.txt
```


## Output

### lib/requirements.txt

```sh
Flask==0.8
Jinja2==2.6
Werkzeug==0.8.3
certifi==0.0.8
chardet==1.0.1
distribute==0.6.24
gunicorn==0.14.2
requests==0.11.1
```


