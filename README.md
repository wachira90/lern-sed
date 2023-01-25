# lern-sed
lern sed

````
sed -i 's/#.*$//' -e '/^$/d' fileName
sed -i 's/#.*$//;/^$/d' fileName
````

````
pax> printf 'Line # with a comment\n\n# Line with only a comment\n' >file

pax> cat file
Line # with a comment

# Line with only a comment

pax> cp file filex ; sed -i 's/#.*$//;/^$/d' filex ; cat filex
Line

pax> cp file filex ; sed -i -e 's/#.*$//' -e '/^$/d' filex ; cat filex
Line
````

## set permissive
````
sed -i s/^SELINUX=.*$/SELINUX=permissive/ /etc/selinux/config
````


## set disabled
````
sed -i s/^SELINUX=.*$/SELINUX=disabled/ /etc/selinux/config
````
