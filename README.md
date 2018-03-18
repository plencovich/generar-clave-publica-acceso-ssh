![Plen.co](https://plen.co/assets/images/logo.png)

## Generar clave pública para SSH

- Generar clave en tu equipo local: `ssh-keygen -t rsa` deberás ingresar donde guardar la clave y el *passphrase*, te recomiendo dejarlo todo por default, osea 3 *enter* seguidos
- Si dejaste todo por default, te habrá generado la clave pública en `/home/{tu_usuario}/.ssh/id_rsa.pub`
- Para copiar la clave al servidor tenés dos opciones:
	1. Utilizando el cmd *ssh-copy-id* `ssh-copy-id user@server`
	2. De forma manual `cat ~/.ssh/id_rsa.pub | ssh user@server "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"`
- Aparecerá algo similar a esto, donde tenes que ingresar tu contraseña por única vez y responder *yes*

```
The authenticity of host '12.34.56.78 (12.34.56.78)' can't be established.
RSA key fingerprint is b1:2d:33:67:ce:35:4d:5f:f3:a8:cd:c0:c4:48:86:12.
Are you sure you want to continue connecting (yes/no)? yes
```
- Ya puedes conectarte por SSH sin necesidad de tu contraseña.

***
[Plen.co](https://plen.co)
