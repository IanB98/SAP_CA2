'''
docker network create mysql
''' 

'''
docker run \
    --network mysql \
    -e MYSQL_ROOT_PASSWORD=my-secret-password \
    --name db \
    -d mysql
'''

'''
docker run \
    --network mysql \
    -p 8080:80 \
    -e PMA_HOST=mysql \
    -d hpmyadmin/hpmyadmin
'''