# Utiliser une image légère de nginx
FROM nginx:alpine

# Copier uniquement les fichiers front-end
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier la config nginx (en s'assurant qu'elle est valide)
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port utilisé dans la conf nginx
EXPOSE 9000
