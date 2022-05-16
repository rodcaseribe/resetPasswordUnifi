# resetPasswordUnifi

# subir a controladora e usar os comandos para alterar a senha
# Baixar o MogoDB e setar comandos pelo cmd

# Descobrir usuário e senha criptografada
mongo --port 27117 ace --eval "db.admin.find().forEach(printjson);"

# Criptografia é um sha-512 com alguns argumentos
# senha padrão igual a password

mongo --port 27117 ace --eval "db.admin.update( { 'name' : 'rodolfocr' }, { $set : { 'x_shadow' : '$6$ee74396ce4c563de$oLm93BwJywYo1sUFgX8U0FC.p75t1Jv838.0defRCe36jgX6PU3h.m3NL6tjCs8Q/1Ymtge0DXz9shb//dyEN.' } } )"
