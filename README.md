# **LAPR1_24_25_DAB_02 - TechTitans**

Projeto Integrativo de LAPR1 do grupo 2 - TechTitans sobre o uso de Eigen Faces para reconhecimento facial

---

## **Descrição**
Este projeto consiste no desenvolvimento de uma aplicação em Java para compactação, geração aleatória, reconstrução e identificação de imagens utilizando a técnica de **Eigenfaces**. O objetivo é implementar funcionalidades que auxiliem na representação e comparação de imagens de maneira eficiente, conforme solicitado no enunciado.

---

## **Integrantes**
| Nome                                    | Número    |
|-----------------------------------------|-----------|
| Rita Mafalda Martins de Oliveira        | 1240729   |
| Alexandre Pereira Henrique              | 1240720   |
| Rafael Pinto Vieira                     | 1241286   |
| Luiz Gabriel de Souza Sargaço Teixeira  | 1230350   |

---

## **Estrutura do Projeto**

Quando o utilizador escolher entre o modo interativo ou não interativo (com ou sem argumentos ao executar o programa), **após cada execução verificar o ‘output’ gerado**, quando escolhido a mesma função.
Pois os arquivos .csv e o .txt com todo o ‘output’ que seria apresentado em consola (não interativo) serão sobrescritos!
As imagens não são sobrescritas, podendo assim, serem comparadas, mas os demais arquivos (.txt e .csv) !

### **Estrutura do comando para utilização do programa via terminal:**

Se deseja utilizar o programa em modo **interativo**, não coloque os argumentos, utilize apenas o comando:
* java -cp "./code/lib/commons-math3-3.6.1.jar" ./code/src/LAPR1_24_25_DAB_02.java

Se deseja utilizar o programa em modo **não interativo**, coloque os argumentos conforme a seguir:
* java -cp "./code/lib/commons-math3-3.6.1.jar" ./code/src/LAPR1_24_25_DAB_02.java -f X -k Y -i Z -j W**

Onde deverá substituir X, Y, Z e W pelos seguintes argumentos:
* [ -f ]:Este argumento, X recebe a função a executar, podendo ser qualquer número de 1 a 4.
* [ -k ]:Este argumento, Y recebe a quantidade de vetores próprios a utilizar. (se o valor for -1 ou superior à quantidade de vetores próprios existentes então a quantidade de vetores próprios usados será o máximo).
* [ -i ]:Este argumento, Z recebe a localização da matriz/imagem (em csv) de ‘input’ a utilizar nas funcionalidades 1 e 3.
* [ -d ]:Este argumento, W recebe a localização da base de imagens (em csv) de ‘input’ a utilizar nas funcionalidades 2, 3 e 4.

```plaintext
LAPR1_24_25_DAB_02
├── code
│   ├── src
│   │   └── LAPR1_24_25_DAB_02.java       # Código principal da aplicação.
│   │   └── Demais classes .java          # Classes dos demais integrantes do grupo.
│   └── lib                                
│       └── commons-math3-3.6.1           # Bibliotecas não nativas utilizadas.
│
├── docs                                  # Documentação do projeto.
│   ├── enunciado                         # Diretório com as versões do enunciado do projeto.
│   │   └── EnunciadoLAPR1_v0.pdf         # Arquivo do enunciado do projeto.
│   ├── outputInterativo.txt              # Documento com toda a saída do programa em modo interativo.
│   └── outputNaoInterativo.txt           # Documento com todos os comandos do programa em modo não interativo e se foram bem sucedidos ou não.
│
├── Output                                # Diretório de todos os outputs gerados pelo programa. 
│       ├── Func1                         # Diretório com os outputs da função 1. As matrizes reconstruídas serão salvas aqui .csv .
│       ├── Func2                         # Diretório com os outputs da função 2.
│       │    ├── Eigenfaces               # Aqui serão salvas as matrizes reconstruídas em extensão .csv .
│       │    └── ImagensReconstruidas     # Aqui serão salvas as imagens reconstruídas em extensão .jpg .
│       ├── Func3
│       │    └── Identificacao            # Aqui serão salvas as imagens que tiveram a menor distância euclidiana, no diretório identificadas em extensão .jpg .
│       ├── Func4                         # Diretório com os outputs da função 4. As imagens geradas aleatoriamente serão salvas aqui .jpg .
│       └── NaoInterativo                 # Diretório com os outputs do modo não interativo. Serão salvos arquivos no formato .txt dentro do diretório de cada função.
│           ├── Func1
│           ├── Func2
│           ├── Func3
│           └── Func4
│
└── README.md                             # Arquivo README do projeto
```
