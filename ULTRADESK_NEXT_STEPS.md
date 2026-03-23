# Ultra Desk Next Steps

Este fork ja tem a primeira camada de branding aplicada para Windows:

- nome padrao do app: `Ultra Desk`
- executavel Windows: `ultradesk.exe`
- metadados do runner Windows ajustados
- prefixo de URI sanitizado para evitar espacos
- servidor RustDesk embutido: `72.61.34.20`
- chave publica embutida: `JPvB567qZohsGYjOlh71CxKSekfb6S6OjGSEbSnZIBw=`

## Onde continuar o branding

- [libs/hbb_common/src/config.rs](C:\Users\Jairo\Documents\New%20project\rustdesk\libs\hbb_common\src\config.rs)
- [src/common.rs](C:\Users\Jairo\Documents\New%20project\rustdesk\src\common.rs)
- [flutter/windows/CMakeLists.txt](C:\Users\Jairo\Documents\New%20project\rustdesk\flutter\windows\CMakeLists.txt)
- [flutter/windows/runner/Runner.rc](C:\Users\Jairo\Documents\New%20project\rustdesk\flutter\windows\runner\Runner.rc)

## Proximo alvo recomendado

1. substituir icones em `res/` e `flutter/windows/runner/resources/`
2. embutir o seu servidor RustDesk no cliente
3. gerar build Windows

## Build no GitHub Actions

O workflow criado foi:

- [.github/workflows/ultradesk-windows.yml](C:\Users\Jairo\Documents\New%20project\rustdesk\.github\workflows\ultradesk-windows.yml)

Para rodar:

1. envie esse arquivo para o GitHub
2. abra o repositório `sontagjairo/ultradesk`
3. clique em `Actions`
4. abra `Ultra Desk Windows Build`
5. clique em `Run workflow`

Quando terminar, baixe o artefato Windows gerado na execucao.

## Caminho mais leve para build

Se a sua maquina nao estiver pronta para compilar RustDesk localmente, use GitHub Actions no seu fork do GitHub.

## Build local no Windows

Voce provavelmente vai precisar de:

- Visual Studio com Desktop development with C++
- Rust toolchain
- Flutter SDK
- dependencias do build do RustDesk

Antes de compilar, rode no minimo:

```powershell
cargo --version
flutter --version
```
