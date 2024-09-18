# Diagrama de Casos de Uso



## Atores Identificados:

1. **Administrador do Sistema**: 
   - Cadastra competições, aloca locais e registra resultados.

2. **Atleta**: 
   - Inscreve-se nas competições.

3. **Organizador de Eventos**: 
   - Auxilia na alocação de locais e no gerenciamento do cronograma.

4. **Sistema Externo de Relatórios**: 
   - Gera relatórios de medalhas com base nos resultados.

---

## Casos de Uso Principais:

1. **Cadastrar Competição**:
   - **Descrição**: O Administrador cadastra uma competição, informando modalidade, data, horário, local e atletas.
   - **Ator**: Administrador do Sistema.

2. **Inscrever Atleta**:
   - **Descrição**: O Atleta escolhe e se inscreve em competições, representando um país em cada modalidade.
   - **Ator**: Atleta.

3. **Alocar Local**:
   - **Descrição**: O Organizador ou Administrador aloca locais, evitando conflitos de horário.
   - **Atores**: Administrador do Sistema, Organizador de Eventos.

4. **Registrar Resultados**:
   - **Descrição**: Após a competição, o Administrador registra os resultados (ouro, prata, bronze).
   - **Ator**: Administrador do Sistema.

5. **Gerar Relatório de Medalhas**:
   - **Descrição**: O Sistema gera relatórios com o desempenho dos países com base nas medalhas.
   - **Ator**: Sistema Externo de Relatórios.

6. **Verificar Disponibilidade de Local**
- **Descrição**: O caso de uso **Alocar Local** inclui o subcaso **Verificar Disponibilidade de Local**. 

---


## Relações de Include e Extend:

### 1. Relações de **Include**:

- O caso de uso **Cadastrar Competição** inclui o subcaso **Inscrever Atleta**, pois ao criar uma competição, o sistema precisa permitir a inscrição dos atletas.
- O caso de uso **Alocar Local** inclui o subcaso **Verificar Disponibilidade de Local**, já que, ao alocar um local, o sistema precisa checar se o local está disponível no horário.

### 2. Relações de **Extend**:

- O caso de uso **Registrar Resultados** estende o caso de uso **Cadastrar Competição**, pois o registro dos resultados acontece após a criação e execução da competição.
- O caso de uso **Gerar Relatório de Medalhas** estende o caso de uso **Registrar Resultados**, uma vez que a geração dos relatórios depende dos resultados registrados.


![Diagrama de casos de uso](../Diagrama_de_casos_de_uso/Imagens/diagrama%20de%20casos%20de%20uso.png)