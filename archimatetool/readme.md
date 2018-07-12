# Prepare

* under current folder you should have 
  * archimate tool installable
  * to be installed plugin under ./plugin
  * dockerfile

# Build the image 

```
docker build -t liuruibnu/archimatetool:v1 .
```

# use the image

```
docker run -it liuruibnu/archimatetool:v1 /app/Archi/Archi -application com.archimatetool.commandline.app -consoleLog -nosplash --help
```


# Reference

https://www.archimatetool.com/
