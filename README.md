<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="60px" src="https://hermes.dio.me/lab_projects/badges/87d332d0-5198-4a2f-b159-38c8c2976954.png"></a>
    <span> Trabalhando com Machine Learning</span>
</h1>

## Criando modelo de previsão - Passo a passo

Para trabalhar no machine learn é essencial que você possua um workspace e esta é a tarefa inicial, criar o seu workspace para assim poder criar o seu trabalho automatizado.

Depois que nosso workspace estiver pronto temos que entrar no ML studio para criar um "novo trabalho de ML automatizado", seguindo o passo a passo da documentação do Learning para melhor entendimento e para que tudo dê certo:
<img align="right" src="images/01.png" width=""/> 

...

## Vamos criar um aprendizado de maquina para a previsão de aluguel de bicicletas:
<img align="right" src="images/02.png" width=""/> 

O tipo de tarefa é regressão e o nome de ativo de dados e aluguel de bicicletas, com fonte de dados da WEB.
<img align="right" src="images/03.png" width=""/> 

<img align="right" src="images/04.png" width=""/> 

<img align="right" src="images/05.png" width=""/> 

...

A documentação do Learning é bem didática e traz todos os valores e configurações para que o trabalho automatizado seja criado:
<img align="right" src="images/07.png" width=""/> 
<img align="right" src="images/08.png" width=""/> 
<img align="right" src="images/09.png" width=""/> 
<img align="right" src="images/10.png" width=""/> 
<img align="right" src="images/11.png" width=""/> 
<img align="right" src="images/12.png" width=""/> 
<img align="right" src="images/13.png" width=""/> 

...

Chegando na opção "examinar" basta enviar o seu trabalho de treinamento:
<img align="right" src="images/14.png" width=""/> 

...

Após envio seu trabalho irá passar pelo processo de configuração das execuções e após 15, podendo o tempo ser menor, estará concluído:
<img align="right" src="images/15.png" width=""/> 

<img align="right" src="images/16.png" width=""/> 

...

Pipeline com as etapas do processo de aprendizado e os testes realizados
<img align="right" src="images/17.png" width=""/> 

## Teste do modelo

Na página do modelo, cliquei na aba "Pontos de extremidade". Também é possível acessar pelo menu lateral em "Pontos de extremidade". Cliquei no ponto correspondente ao modelo gerado. Em seguida, acessei a aba "Testar".

Para o teste, utilizei o json abaixo:

``` JSON
{
  "Inputs": {
    "data": [
      {
        "day": 1,
        "mnth": 1,
        "year": 2022,
        "season": 2,
        "holiday": 0,
        "weekday": 1,
        "workingday": 1,
        "weathersit": 2,
        "temp": 0.3,
        "atemp": 0.3,
        "hum": 0.3,
        "windspeed": 0.3
      }
    ]
  },
  "GlobalParameters": 1.0
}
```

A previsão gerada foi: 364.9751644934589

<img align="right" src="images/18.png" width=""/> 
