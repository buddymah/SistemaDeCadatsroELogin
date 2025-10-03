# Sistema de Cadastro e Login em C

Este projeto é um portal de serviços implementado em **linguagem C**, que reúne operações matemáticas, verificações lógicas e classificações em diferentes módulos.  
Ele foi desenvolvido como trabalho acadêmico no curso de **Ciência da Computação - CESUPA (2025)**.

---

## Funcionalidades

O sistema é composto por 5 módulos principais, além do cadastro/login inicial.

### Cadastro e Login
- Criação de usuário e senha.  
- Validação de senha forte (mínimo 6 caracteres, não pode ser `123456`, nem vazia).  
- Controle de tentativas (máximo 3).  
- Apenas prossegue se o login for válido.  

### Módulo Pessoal
- Classificação de idade:  
  - Menor de idade (não eleitor).  
  - Voto opcional (16-17 anos ou maiores de 65).  
  - Voto obrigatório (18 a 64 anos).  
- Cálculo do **IMC (Índice de Massa Corporal)** com duas casas decimais.  

### Módulo Financeiro
- Calcular salário total em 12 meses.  
- Calcular salário do período (dias trabalhados × valor da diária).  
- Conversor de moedas (Reais → Dólares e Euros).  

### Módulo Acadêmico
- Leitura de 3 notas do usuário.  
- Cálculo da soma, média e dobro da média.  
- Classificação: Aprovado, Recuperação ou Reprovado.  

### Módulo Utilidades
- Verificar se um número é par ou ímpar.  
- Checar se um número está no intervalo [10, 50].  
- Calcular área e perímetro de círculo e retângulo.  
- Converter segundos em horas e minutos.  

---

## Estrutura do Código

O projeto foi implementado em um único arquivo C, organizado em funções separadas para cada módulo.


