Muitas empresas estão utilizando ferramentas de IA (Inteligência Artificial) para acelerar os negócios, facilitando a interação, e melhorando a experiência com os clientes. Um exemplo claro desse avanço, são os Chatbots, que são criados para atender aos clientes, ou para apoiar os colaboradores em atividades mais complexas, que antes dependiam de pessoas com mais conhecimento.

Por ser uma área relativamente nova, muitas empresas não se atentam a validar os modelos ou dados que serão utilizados para o treinamento dos modelos de IA (Inteligência Artificial). Por outro lado, existem muitas pessoas se aproveitando dessa fragilidade para capturar dados sensíveis através dessas interfaces. 

Como ocorre o vazamento de dados através da IA? Pode ocorrer de várias, maneiras, por exemplo: Falhas no Pré-processamento de Dados; no qual as informações sensíveis não são anonimizadas ou removidas, em Superexposição de Dados (Overexposure); o modelo fornece mais informações do que o necessário, Inferência de Dados; o modelo inferi nas informações sensíveis com base nas perguntas, e no momento de Fine-Tuning (Ajuste fino) do modelo; os dados sensíveis ou estratégicos podem ser incluídos no modelo de ajuste fino, entre outras formas..

Vale ressaltar que até aqui, falamos apenas de validar os dados e testar os modelos treinados de IA, para saber se o modelo está retornando as informações corretas, existem várias outras técnicas de Segurança que devem ser consideradas para validar os controles de Segurança em modelos de IA, alguns já disponibilizados pelo OWASP TOP 10 IA.

Pensando em como fazer essa validação do modelo de IA e suas repostas, resolvi fazer um teste usando um script em python, algo simples, apenas para demonstração, esse script está usando dados pré-definidos, mas nada impede de ser utilizamos bases como GPT (GENERATIVE Pré-trained transformer) ou Hugging Face para fazer testes.

Para melhorar a qualidade da validação, utilizei a técnica de Cross-Validation, com a biblioteca K-Fold, disponível no Scikit-learning. O K-Fold divide o conjunto de dados em k-partes (folds) e tamanhos iguais ou aproximados, e por fim faz o cálculo de k interações para calcular e média.

O modelo T5, foi empregado para gerar perguntas, e o Modelo SpaCy, visa identificar entidades sensíveis. 


