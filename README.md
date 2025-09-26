# Unity Hub Installation Guide 🎮

Una guía completa para instalar Unity Hub en sistemas Ubuntu/Debian.

## 📋 Requisitos previos

- Ubuntu 18.04+ o Debian 9+
- Conexión a internet
- Permisos de administrador (sudo)

## 🚀 Instalación paso a paso

### Paso 1: Crear directorio de keyrings

Asegúrate de que el directorio de keyrings existe en tu sistema:

```bash
sudo mkdir -p /usr/share/keyrings
```

### Paso 2: Descargar e instalar la clave GPG de Unity

Descarga y guarda la clave GPG oficial de Unity Technologies:

```bash
wget -O- https://hub.unity3d.com/linux/keys/public | gpg --dearmor | sudo tee /usr/share/keyrings/Unity_Technologies_ApS.gpg > /dev/null
```

### Paso 3: Agregar el repositorio de Unity Hub

Agrega el repositorio oficial de Unity Hub a tu sistema:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/Unity_Technologies_ApS.gpg] https://hub.unity3d.com/linux/repos/deb stable main" | sudo tee /etc/apt/sources.list.d/unityhub.list
```

### Paso 4: Actualizar la lista de paquetes

Actualiza el índice de paquetes para incluir el nuevo repositorio:

```bash
sudo apt update
```

### Paso 5: Instalar Unity Hub

Finalmente, instala Unity Hub:

```bash
sudo apt install unityhub
```

## ✅ Verificación de la instalación

Puedes verificar que Unity Hub se instaló correctamente ejecutando:

```bash
unityhub --version
```

O simplemente busca "Unity Hub" en el menú de aplicaciones de tu sistema.

## 🔧 Solución de problemas comunes

### Error de clave GPG
Si experimentas problemas con la clave GPG, asegúrate de que tienes `gnupg` instalado:

```bash
sudo apt install gnupg
```

### Error de arquitectura
Esta guía está diseñada para sistemas de 64 bits (amd64). Si usas una arquitectura diferente, consulta la documentación oficial de Unity.

### Problemas de permisos
Asegúrate de ejecutar todos los comandos que requieren `sudo` con los permisos adecuados.

## 📚 Recursos adicionales

- [Documentación oficial de Unity Hub](https://docs.unity3d.com/Hub/manual/index.html)
- [Soporte técnico de Unity](https://support.unity.com/)
- [Foro de la comunidad Unity](https://forum.unity.com/)

## 📝 Notas

- Esta instalación añade el repositorio oficial de Unity, permitiendo actualizaciones automáticas a través del gestor de paquetes.
- Unity Hub requiere una cuenta de Unity para funcionar completamente.
- Asegúrate de tener suficiente espacio en disco, ya que Unity Hub y los editores de Unity pueden ocupar varios GB.

---

**¿Encontraste algún problema?** No dudes en abrir un issue o consultar la documentación oficial de Unity para obtener más ayuda.

## 🏷️ Tags

`Unity` `Unity Hub` `Ubuntu` `Debian` `Linux` `Game Development` `Installation Guide`
