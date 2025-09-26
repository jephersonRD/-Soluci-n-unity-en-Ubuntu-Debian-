

---

📦 Instalación de Unity Hub en Ubuntu/Debian

Este repositorio contiene una guía paso a paso para instalar Unity Hub en distribuciones basadas en Ubuntu/Debian.

🔧 Pasos de instalación

1. Crear directorio de keyrings (si no existe)

sudo mkdir -p /usr/share/keyrings

2. Descargar y guardar la clave GPG de Unity

wget -qO- https://hub.unity3d.com/linux/keys/public \
  | gpg --dearmor \
  | sudo tee /usr/share/keyrings/unityhub.gpg > /dev/null

3. Agregar el repositorio de Unity Hub

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/unityhub.gpg] \
https://hub.unity3d.com/linux/repos/deb stable main" \
| sudo tee /etc/apt/sources.list.d/unityhub.list

4. Actualizar la lista de paquetes

sudo apt update

5. Instalar Unity Hub

sudo apt install -y unityhub

✅ Verificación

Una vez finalizada la instalación, puedes iniciar Unity Hub ejecutando:

unityhub


---

