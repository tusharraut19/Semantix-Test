# Semantix-Test
Semantix Respostas - Desafio Engenheiro de Dados - Candidato : Tushar Raut

# Pergunta-1 Qual o objetivo do comando cache em Spark? 
 
Resposta: 

O objetivo do comando é Cache de resultados sucessivos para serem reutilizados em etapas subsequentes

Resposta (em inglês): 

The objective of Cache command is to help save interim partial results so they can be reused in subsequent stages
 
 
# Pergunta-2 O mesmo código implementado em Spark é normalmente mais rápido que a implementação equivalente em MapReduce. Por quê? 
  
Resposta: 

O Spark é mais rápido que o MapReduce porque ele faz o processamento na memória principal dos nós do trabalhador e evita as operações de input ou output que não precisa com os discos

Resposta (em inglês): 

Spark is more faster than MapReduce as it does the processing in the main memory of the worker nodes and prevents the unnecessary I/O operations with the disks


# Pergunta-2 Qual é a função do SparkContext? 
 
Resposta: 

O SparkContext configura serviços internos e estabelece uma conexão com um ambiente de execução do Spark.

Resposta (em inglês):  

SparkContext sets up internal services and establishes a connection to a Spark execution environment.
 
 
# Pergunta-3 Explique com suas palavras o que é Resilient Distributed Datasets (RDD). 
 
Resposta :  

Conjuntos de Dados Distribuídos Resilientes (RDD) é uma coleção distribuída imutável de objetos. Cada conjunto de dados é dividido em partições lógicas, que pode ser calculado em diferentes nós do cluster e pode conter qualquer tipo de objetos Python, 
Java ou Scala, incluindo classes definidas pelo usuário.

Resposta (em inglês):  

Resilient Distributed Datasets (RDD) are an immutable distributed collection of objects. Each dataset is divided into logical partitions,  which may be computed on different nodes of the cluster and can contain any type of Python, Java, 
or Scala objects, including user-defined classes.
 
 
# Pergunta-4 GroupByKey é menos eficiente que reduceByKey em grandes dataset. Por quê? 
 
Resposta :  

O exemplo reduceByKey funciona muito melhor em um grande conjunto de dados porque o Spark sabe que pode combinar output com uma chave comum em cada partição antes de embaralhar os dados.

Resposta (em inglês):  

reduceByKey example works much better on a large dataset because Spark knows it can combine output with a common key on each partition before shuffling the data.
 
 
# Explique o que o código Scala abaixo faz. 
val textFile = sc.textFile("hdfs://...") 
val counts = textFile.flatMap(line => line.split(" "))
            .map(word => (word, 1))
            .reduceByKey(_ + _) 
counts.saveAsTextFile("hdfs://...") 

Resposta : 

Lê os dados armazenados no arquivo hdfs em um sc textFile. Executa a função MapReduce com adição e salva-a de volta no arquivo hdfs.

Resposta (em inglês):  

Reads the data that’s stored in hdfs file into a sc textFile. Performs MapReduce function with addition and saves it back to hdfs file.


# References: 

# 1. https://jaceklaskowski.gitbooks.io/mastering-apache-spark/content/ (Mastering Apache Spark by Jace Klaskowski)

# 2. Rajanarayanan Thottuvaikkatumana - Apache Spark 2 for Beginners (2016, Packt Publishing) (Que enviou no o link de email)
