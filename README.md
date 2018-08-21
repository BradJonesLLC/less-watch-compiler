# Compile/watch LESS with Docker

E.g., in your dockerfile:

```yaml
version: '2.2'
services:
  less:
    image: bradjonesllc/less-watch-compiler
    volumes:
      - ./web/themes/custom/your_theme:/src
    working_dir: /src
    command: less-watch-compiler --source-map less css
    user: your-user-id
```
