# simpleapp
PoC for spinnaker

simple nigx app with static html page

# bluegreen deployment:

* master branch: blue, production

* dev branch: green, development

# image tags:

* master: eleanore0102/simpleapp:latest

```bash
docker run --rm -p 80:80 --name blue eleanore0102/simpleapp:latest
```

then go to localhost

* dev: eleanore0102/simpleapp:dev

```bash
docker run --rm -p 80:80 --name blue eleanore0102/simpleapp:dev
```

then go to localhost

# flow:

initially deploy v1 in production, then run v2 in dev, and after testing,
promote v2 to production, and completely kill v1
