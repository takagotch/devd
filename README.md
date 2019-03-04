### devd
---
https://github.com/cortesi/devd

```
```

```
devd -o ./rendered
go get github.com/cortesi/devd/cmd/devd
devd -ol .
devd -w ./src http://localhost:8080

devd -l .
devd -w ./src http://localhost:8888
devd -x "**.less" -l .

devd -l \
-w ./src/ \
/=http://localhost:8888 \
/api/=http://localhost:8889 \
/static/=./assets

devd ./static api=http://localhost:8888

devd -d 114 -u 51 -n 275 .

/assets/=./static
static/assets=./static
app/login-http://localhost:8888
devd ./static
devd http://localhost:8888
devd --notfound index.html /static
devd --notfound /index.html /static
```

```
src/** {
  prep: render ./src ./rendered
}

rendered/*.css ./rendered/*.html {
  daemon: devd -m ./rendered
}
```


