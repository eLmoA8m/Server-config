# (Opcional) Cambiar a root (solo si es necesario)
sudo -i

# Actualizar los índices de paquetes
sudo apt update

# (Opcional) Actualizar los paquetes instalados
sudo apt upgrade -y

# Instalar firewalld
sudo apt install -y firewalld

# Habilitar y arrancar firewalld ahora y al iniciar
sudo systemctl enable firewalld
sudo systemctl start firewalld

# Verificar el estado (systemd)
sudo systemctl status firewalld

# Comprobar estado rápido con firewall-cmd
sudo firewall-cmd --state

# Listar reglas/zona actual
sudo firewall-cmd --list-all

# Detener / iniciar / reiniciar (según sea necesario)
sudo systemctl stop firewalld
sudo systemctl start firewalld
sudo systemctl restart firewalld

# Ver logs del servicio
sudo journalctl -u firewalld --no-pager

# Comprobar si ufw (otro firewall) está activo (puede interferir)
sudo ufw status
