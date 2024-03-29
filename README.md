﻿# Trabalho 06: Projeto Snaze

# Apresentação

Nesse trabalho você terá a oportunidade de implementar uma simulação na qual seu programa deve guiar uma cobra dentro de um labirinto até um pedaço de comida que surge em uma posição aleatória.
A descrição completa do trabalho se encontra [**aqui**](docs/snake_programming_project.pfd).

Além da implementação do trabalho você precisa fornecer algumas informações no arquivo [author.md](author.md), indicando a autoria do trabalho e quais itens da tarefa foram realizados com sucesso. 

# Compilando e Executando

## Manualmente com g++

Para compilar e executar o programa manualmente basta digitar os seguintes comandos em seu terminal:

```bash
# Caso não tenha uma pasta para os executáveis, você deve criá-la com esse comando
$ mkdir bin

# Compilar
$ g++ -Wall -std=c++11 source/src/snaze.cpp source/src/snaze_game.cpp source/src/level.cpp source/src/snake.cpp source/src/player.cpp -I source/include -I source/lib -o bin/snaze

# Executar
$ ./bin/snaze [<options>] <input_level_file>
    Game simulation options:
        --help                  # Print this help text.
        --fps <num>             # Number of frames (board) presented per second. Default = 12.
        --lives <num>           # Number of lives the snake shall have. Default = 5.
        --food <num>            # Number of food pellets for the entire simulation. Default = 10.
        --playertype <type>     # Type of snake intelligence: random, backtracking. Default = backtracking.
```

## Cmake

Para compilar e executar o programa com o Cmake você precisa ter instalado pelo menos a versão 3.2. Em seguida, abra seu terminal e execute os seguintes comandos:

```bash
# Pede ao cmake para criar o diretório de compilação
$ cmake -S source -B build

# Compilar
$ cmake --build build

# Executar (Exemplo de execução: ./build/snaze ./assets/level1.dat)
$ ./build/snaze [<options>] <input_level_file>
    Game simulation options:
        --help                  # Print this help text.
        --fps <num>             # Number of frames (board) presented per second. Default = 12.
        --lives <num>           # Number of lives the snake shall have. Default = 5.
        --food <num>            # Number of food pellets for the entire simulation. Default = 10.
        --playertype <type>     # Type of snake intelligence: random, backtracking. Default = backtracking.
```

Os arquivos com apostas devem ser salvos na pasta `assets` (se isso for feito, para executar basta `./build/snaze ./assets/<arquivo com sua aposta>`. Já existem alguns exemplos de arquivos de aposta nesta pasta. É possível utilizá-los, mas você pode criar o seu próprio também.

--------
&copy; DIMAp/UFRN 2021.
