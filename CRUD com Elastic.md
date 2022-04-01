# Executando CRUD utilizando o Elastic com o docker desktop
# Utilizando a interface gráfica através de localhost
# Criando índice produto e inserindo os seguintes documentos:

POST produto/_doc/4
{
  "nome": "cpu", 
  "qtd": 15, 
  "descricao": "i5, 2.5Ghz"
}
POST produto/_doc/3
{
  "nome": "memória ram", 
  "qtd": 10, 
  "descricao": "8GB, DDR4"
}
POST produto/_doc/2
{
  "nome": "hd",
  "qtd": 20, 
  "descricao": "Interface USB 2.0, 500GB, Sistema: Windows 10, Windows 8, Windows 7 "
}
POST produto/_doc/1
{
  "nome": "mouse", "qtd": 50, "descricao": "com fio USB, compatível com Windows, Mac e Linux"
}

# Verificando se existe o documento com  id 3

HEAD produto/_doc/3

# Alterando o valor do atributo qtd para 30 do documento com id 3

POST produto/_update/3
{
  "doc": {
    "qtd":30
  }
}

# Buscando o documento com id 1

GET produto/_doc/1

# Deletando o documento com id 4

DELETE produto/_doc/4

# Contando quantos documentos tem o índice produto

GET produto/_count



