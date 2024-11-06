# Titulo

## Subtitulo

### Subsubtitulo

O programa deve *começar* solicitando ao usuário que **insira seu nome**.

O usuário deve:
1. Inserir seu nome
2. Inserir seu salário
3. Inserir seu bonos

[Site da Sabesp](https://www.sabesp.com.br/)

![Imagem](https://cdn.worldvectorlogo.com/logos/sabesp.svg)

```python
    print("Bem vindo ao sistema de bonus da Sabesp")
    nome = input("Por favor digite o seu none: ")
    salario = float(input("Por favor digite o seu salário: "))
    bonus = float(input("Por favor digite o seu bônus: "))
    bonus_total = 1000 + salario * bonus
    print(f"Olá {nome}, o seu valor foi de {bonus_total}")
```

```mermaid
sequenceDiagram
    participant Usuário
    participant Sistema

    Usuário->>Sistema: Inicia o programa
    Sistema->>Usuário: "Bem vindo ao sistema de bonus da Sabesp"
    Usuário->>Sistema: Digita o nome
    Sistema->>Usuário: Solicita o salário
    Usuário->>Sistema: Digita o salário
    Sistema->>Usuário: Solicita o bônus
    Usuário->>Sistema: Digita o bônus

    Sistema->>Sistema: Calcula bonus_total = 1000 + salario * bonus
    Sistema->>Usuário: Exibe mensagem com o valor de bonus_total
```

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :until isadded
    Functionality added                 :milestone, isadded, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
```

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Em seguida, o programa deve pedir ao usuário para inserir o valor do seu salário. Considere que este valor pode ser um número decimal.
Depois, o programa deve solicitar a porcentagem do bônus recebido pelo usuário, que também pode ser um número decimal.
O cálculo do KPI do bônus de 2024 é de 1000 + salario * bônus
Finalmente, o programa deve imprimir uma mensagem no seguinte formato: "Olá [nome], o seu valor bônus foi de 5000".
