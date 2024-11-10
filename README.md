# Projeto de Moderação de Conteúdo com Azure AI Content Safety

Este projeto demonstra o uso do Azure AI Content Safety para moderação de conteúdo de texto, incluindo testes de segurança e categorização de risco. Ele guia o usuário pelo processo de configuração e uso da plataforma, além de fornecer um exemplo de arquivo JSON com os pontos de extremidade para integrar o recurso com outros aplicativos.

## Pré-requisitos

- Conta no [Microsoft Azure](https://azure.microsoft.com/pt-br/)
- Acesso ao [Content Safety Studio](https://contentsafety.cognitive.azure.com)

## Etapas do Projeto

### 1. Criação do Repositório

Crie um repositório no GitHub para armazenar este README.md e o arquivo `.json` de pontos de extremidade.

### 2. Configuração do Recurso no Azure Content Safety

1. Acesse o **Content Safety Studio** e faça login com as credenciais da sua conta Azure.
2. No menu configurações :gear:, selecione **Criar novo recurso**.
3. No **Portal do Azure**, configure o recurso de acordo com as seguintes especificações:
   - Assinatura: `sua assinatura do Azure`
   - Grupo de Recursos: `nome exclusivo do grupo de recursos`
   - Região: `região disponível (exemplo: Leste dos EUA 2)`
   - Nome: `nome exclusivo para o recurso`
   - Tipo de preço: `F0 grátis`
4. Conclua a criação e, em seguida, retorne ao Content Safety Studio.
5. Associe o recurso ao Content Safety Studio e configure suas permissões usando o **Controle de Acesso (IAM)**:
   - Adicione-se como `Usuário dos Serviços Cognitivos`.

### 3. Realização de Testes de Moderação de Conteúdo

1. Na página inicial do Content Safety Studio, selecione **Executar testes de moderação**.
2. Escolha uma amostra de texto ou insira o seu próprio.
3. Configure os níveis de gravidade para cada categoria (Violência, Auto-mutilação, Sexualidade, Ódio) conforme necessário.
4. Clique em **Executar teste** para ver os resultados de moderação, que incluem categorias de risco e severidade.

### 4. Obtenção e Armazenamento dos Pontos de Extremidade

Após configurar o recurso de **Azure Content Safety** e finalizar o processo de moderação de conteúdo, você verá uma tela com as informações do **endpoint** e da **chave do recurso**. Essas informações serão usadas em sua aplicação para realizar testes de segurança.

Ao finalizar o processo, você verá uma imagem de confirmação, semelhante a esta:

![Imagem de Confirmação](https://github.com/user-attachments/assets/f1ecd676-b2c2-4388-82eb-d8e601950c2e)

Consegui isso utilizando a seguinte chave e endpoint:

```json
{
    "endpoint": "https://ml-predict-dio.cognitiveservices.azure.com/",
    "key": "BAjGRFVIYuMV4h5twjt8LIRgzfnW6JWFWyclbsexP7NLK0p0P4fmJQQJ99AKACYeBjFXJ3w3AAAHACOGYAqp"
}
```

### Referências

- [Documentação do Azure AI Content Safety](https://learn.microsoft.com/azure/cognitive-services/ai-content-safety/)
- [AI Fundamentals - Content Safety Lab](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html)
- [AutoML - AI900](https://aka.ms/ai900-auto-ml)
