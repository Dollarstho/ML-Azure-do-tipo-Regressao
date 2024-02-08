# Passo a passo Treino de ML Modelo de Previsão Azure
## 1. Acesse o "Machine Learning Studio" através da plataforma Azure. 
## 2. Crie um novo espaço de trabalho no botão "Create workspace" com o nome desejado.
## 3. Na aba "Authoring" acesse a opção "Automated ML"
## 4. Crie um novo crie um novo trabalho automatizado no botão "New Automated ML Job". (Avançar)
## 5. Configure o nome do trabalho, nome do experimento e sua descrição. (Avançar)
## 6. Configurar o tipo de tarefa para regressão no menu "Select task type" para o tipo Regressão/ Regression. (Avançar)
## 7. Clicar com o botão esquerdo do mouse no botão create. 
## 8. Colocar Nome, Descrição e tipo do ativo de dados. O tipo para este modelo é o "Tabular". (Avançar)
## 9. Selecionar a fonte de ativo de dados, neste caso a fonte de dados é "From Web files".
## 10. Inserir o endereço do ativo de dados na janela "Web URL". (https://aka.ms/bike-rentals) (Avançar)
## 11. Configurações de dados, neste teste mudaremos o tipo de cabeçalhos de coluna no menu "Column Headers" para a opção "Only first file has headers". (Avançar)
## 12. Configuração de tarefas, alterar a coluna de destino no menu "Target column" para a opção "rentals (Integer)". Alterar as configuração adicionais no botão "View Aditional configuration settings". No menu Primary metric selecionar a opção "NormalizedRootMeanSquaredError", desabilitar as opções "Explain best model" e "Use all Supported models". No menu "Allowed models" escolher as opções "RandomForest" e "LightGBM" e Salvar no botão "Save". (Avançar)
## 13. Configurar os limites na aba "Limits" para: 
### Max trials = 3;
### Max concurrent trials = 3;
### Max nodes = 3;
### Metric score treshold = 0,085;
### Experiment timeout (minutes) = 15;
### Iteration timeout (minutes) = 15;
### Enable early termination = true.
## 14. Alterar o menu  "Validation type" para a opção "Train-validation split", "Percentage validation of data" com valor "10" e "Test data" para "None". (Avançar)
## 15. Na aba "Compute" Apenas (Avançar)
## 16. clicar na opção "Submit training Job"
## 17. Aguarde a conclusão do processo de treinamento.
## 18. Conferir os dados na aba Tarefas (Jobs) e depois Testar os dados na aba "Ponto de extremidade".
## 19. FIM
