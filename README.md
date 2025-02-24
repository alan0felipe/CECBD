# CECBD
Construindo um Esquema Conceitual para Banco De dados de uma oficina Mecânica

# 📌 Sistema de Gestão de Oficina Mecânica

## 📖 Descrição do Projeto
Este projeto consiste na modelagem de um **Esquema Conceitual** para um sistema de controle e gerenciamento de ordens de serviço em uma oficina mecânica. O objetivo é estruturar as informações de forma eficiente, garantindo o correto relacionamento entre clientes, veículos, mecânicos, serviços e ordens de serviço.

O esquema conceitual foi criado com base na narrativa fornecida e detalha as entidades, seus atributos e os relacionamentos necessários para um sistema funcional.

## 🎯 Objetivo do Sistema
- Gerenciar **clientes** e seus respectivos **veículos**;
- Registrar e acompanhar **ordens de serviço (OS)**;
- Controlar a alocação de **mecânicos** e **equipes**;
- Calcular os valores das OS com base em **mão de obra** e **peças utilizadas**;
- Registrar a **autorização do cliente** para execução dos serviços;
- Monitorar o **status** e a **data de conclusão** das OS.

## 🗂️ Estrutura do Banco de Dados
### 📌 **Entidades e Atributos**

1. **Cliente**
   - ID (PK)
   - Nome
   - Telefone
   - Endereço

2. **Veículo**
   - Placa (PK)
   - Modelo
   - Ano
   - Cliente_ID (FK)

3. **Ordem de Serviço (OS)**
   - Número_OS (PK)
   - Data_Emissão
   - Valor_Total
   - Status
   - Data_Conclusão
   - Veículo_ID (FK)

4. **Equipe**
   - ID (PK)
   - Nome

5. **Mecânico**
   - ID (PK)
   - Nome
   - Endereço
   - Especialidade
   - Equipe_ID (FK)

6. **Serviço**
   - ID (PK)
   - Nome
   - Valor_Mão_de_Obra

7. **Peça**
   - ID (PK)
   - Nome
   - Valor

8. **Execução_Serviço**
   - OS_ID (FK)
   - Serviço_ID (FK)
   - Mecânico_ID (FK)
   - Quantidade
   - Subtotal

9. **Peça_OS**
   - OS_ID (FK)
   - Peça_ID (FK)
   - Quantidade
   - Subtotal

10. **Autorização**
   - OS_ID (FK)
   - Cliente_ID (FK)
   - Status

