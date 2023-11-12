# Fluxo de Trabalho Bug 

![Imagen do fluxo do trabalho](assets/FluxoDeTrabalhoBugImage.png)

## Estados da Tarefa

### 1. Iniciar Tarefa na Sprint
   - **Descrição:** Tarefa é criada e atribuída à sprint.
   - **Ação:** Mover para "EM ANDAMENTO".
   - **Interface:**
     ```
     Default Screen
     → EM ANDAMENTO
     ```

### 2. Em Andamento
   - **Descrição:** Tarefa está em desenvolvimento.
   - **Ação:** Subir tarefa para validação do QA quando estiver pronta.
   - **Interface:**
     ```
     Default Screen
     → READY FOR QA
     ```

### 3. Ready for QA
   - **Descrição:** Tarefa está pronta para ser validada pelo QA.
   - **Ação:** Se a tarefa não precisar ser continuada, mover para "FECHADA". Caso contrário, retornar para "EM ANDAMENTO".
   - **Interface:**
     ```
     Default Screen
     → FECHADA (se não for continuada)
     → EM ANDAMENTO (se for continuada)
     ```

### 4. Fechada
   - **Descrição:** Tarefa foi encerrada sem a necessidade de validação pelo QA.
   - **Ação:** Nenhuma transição fora deste estado.

### 5. Em Análise
   - **Descrição:** QA iniciou a validação da tarefa.
   - **Ação:** Se a tarefa precisar de correção, retornar para "REABERTO". Se estiver correta, liberar para deploy.
   - **Interface:**
     ```
     Default Screen
     → REABERTO (se precisar de correção)
     → RESOLVIDO (se estiver correta)
     ```

### 6. Reaberto
   - **Descrição:** Item avaliado e retornado para correção.
   - **Ação:** Atualizar e corrigir a tarefa, movendo para "EM ANDAMENTO".
   - **Interface:**
     ```
     Default Screen
     → EM ANDAMENTO
     ```

### 7. Resolvido
   - **Descrição:** Tarefa foi validada e corrigida, pronta para o deploy.
   - **Ação:** Enviar para produção.
   - **Interface:**
     ```
     Default Screen
     → CONCLUÍDO
     ```

### 8. Concluído
   - **Descrição:** Tarefa foi implementada com sucesso e enviada para produção.
   - **Ação:** Nenhuma transição fora deste estado.