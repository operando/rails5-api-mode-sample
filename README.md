## Rails5 API Mode Sample

* http://guides.rubyonrails.org/api_app.html
* [Rails 5 のAPI modeを少し調べてみた](https://www.hommax39.com/archives/170)

### index

```
curl -H 'Content-Type:application/json' \
http://localhost:3000/tasks -w '\n%{http_code}\n' -s
```

### show

```
curl -H 'Content-Type:application/json' \
http://localhost:3000/tasks/1 -w '\n%{http_code}\n' -s
```

### create

```
curl -H 'Content-Type:application/json' \
-d '{ "task" : { "title": "testtest", "comment": "hogehoge" } }' \
http://localhost:3000/tasks -w '\n%{http_code}\n' -s
```

### update

```
curl -X PUT -H 'Content-Type:application/json' \
-d '{ "task" : { "title": "update hogehoge" } }' \
http://localhost:3000/tasks/1 -w '\n%{http_code}\n' -s
```

### delete

```
curl -X DELETE -H 'Content-Type:application/json' \
http://localhost:3000/tasks/1 -w '\n%{http_code}\n' -s
```
