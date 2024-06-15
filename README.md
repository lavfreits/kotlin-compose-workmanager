# Bluromatic

Bluromatic é um aplicativo Android que aplica efeitos de desfoque em imagens utilizando o WorkManager. Este projeto é uma implementação de exemplo para demonstrar o uso do WorkManager, Jetpack Compose e outras bibliotecas do Android.


## Índice

- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Instalação](#instalação)
- [Uso](#uso)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Licença](#licença)


## Visão Geral

Este projeto foi desenvolvido como parte do Android Open Source Project e é licenciado sob a Licença Apache, Versão 2.0.


## Funcionalidades

- Aplicação de diferentes níveis de desfoque em imagens.
- Visualização da imagem desfocada.
- Cancelamento de tarefas de desfoque em andamento.
- Interface de usuário moderna com Jetpack Compose.


## Tecnologias Utilizadas

- **WorkManager**: Para gerenciar e agendar tarefas assíncronas que continuam mesmo que o aplicativo seja encerrado.
- **Jetpack Compose**: Para criar interfaces de usuário modernas e responsivas.
- **Kotlin Coroutines**: Para operações assíncronas e gerenciamento de threads.
- **NotificationCompat**: Para mostrar notificações durante a execução das tarefas de desfoque e salvamento.
- **Bitmap**: Para manipulação e processamento de imagens.
- **ContentResolver**: Para acessar e salvar imagens no armazenamento do dispositivo.


## Instalação

1. Clone este repositório 
2. Abra o projeto no Android Studio.
3. Sincronize o projeto com Gradle para baixar todas as dependências necessárias.


## Uso
1. Execute o aplicativo em um dispositivo Android ou emulador.

2. Na tela principal, selecione o nível de desfoque desejado.

3. Clique no botão "Start" para iniciar o processo de desfoque.

4. Após a conclusão, você pode visualizar a imagem desfocada ou cancelar o processo a qualquer momento.


## Estrutura do Projeto

- `data/`: Contém as classes relacionadas ao repositório e aos dados da aplicação.
  - `AppContainer.kt`: Define a interface e a implementação do contêiner de dependências.
  - `BlurAmount.kt`: Modelo de dados para os níveis de desfoque.
  - `BlurAmountData.kt`: Dados estáticos dos níveis de desfoque.
  - `BluromaticRepository.kt`: Interface do repositório.
  - `WorkManagerBluromaticRepository.kt`: Implementação do repositório utilizando o WorkManager.

- `ui/`: Contém as classes e funções relacionadas à interface do usuário.
  - `BluromaticScreen.kt`: Tela principal do aplicativo.
  - `BlurViewModel.kt`: ViewModel para gerenciar o estado da tela.

- `workers/`: Contém as classes relacionadas às tarefas de trabalho do WorkManager.
  - `BlurWorker.kt`: Tarefa de trabalho para aplicar o desfoque.
  - `CleanupWorker.kt`: Tarefa de limpeza.
  - `SaveImageToFileWorker.kt`: Tarefa para salvar a imagem em um arquivo.
  - `WorkerUtils.kt`: Utilitários para criar notificações e manipular imagens.

- `BlurActivity.kt`: Atividade principal que inicia a tela do Bluromatic.


## Licença
Este projeto está licenciado sob a Licença Apache, Versão 2.0. Consulte o arquivo LICENSE para obter mais informações.

