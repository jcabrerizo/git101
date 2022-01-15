# Git 101

cambio22445

hola

Added Mar 29 en nueva rama

To implement the filter modify the local project file `.git/config` to add the filter:

```
[filter "nameFilter"]
	clean = sed 's:Don Pepito:<MI_NOMBRE>:g'
	smudge = sed 's:<MI_NOMBRE>:Don Pepito:g'
```

replacing "Don Pepito" with your name *in both lines*

Mi nombre es: <MI_NOMBRE>
Mi apellido es: <MI_APELLIDO>