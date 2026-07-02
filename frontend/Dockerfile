FROM nginx:alpine

# Copiar los archivos estáticos y la configuración de Nginx
COPY . /usr/share/nginx/html
COPY default.conf /etc/nginx/conf.d/default.conf

# --- ESTA ES LA LÍNEA MÁGICA QUE DEBES AÑADIR ---
# Reemplaza la palabra tienda-backend por la IP fija del servicio real antes de que Nginx inicie
CMD ["/bin/sh", "-c", "sed -i 's/tienda-backend/192.168.23.100/g' /etc/nginx/conf.d/default.conf && exec nginx -g 'daemon off;'"]
