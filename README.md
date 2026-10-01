# EterPass — releases

Instaladores do **EterPass Desktop**, o cofre de segredos e identidades da [Eter Growth](https://etergrowth.com).

O código-fonte é privado. Este repositório só serve para publicar as versões:

- **Windows:** `EterPass_<versão>_x64-setup.exe`
- **macOS (Intel e Apple Silicon):** `EterPass_<versão>_universal.dmg`
- `latest.json`: consultado pela app para as actualizações automáticas
- `SHA256SUMS.txt`: somas de verificação

## Verificar o download

```powershell
# Windows (PowerShell)
Get-FileHash .\EterPass_<versão>_x64-setup.exe -Algorithm SHA256
```

```sh
# macOS
shasum -a 256 EterPass_<versão>_universal.dmg
```

O resultado tem de coincidir com a linha do mesmo ficheiro em `SHA256SUMS.txt`.

## Actualizações

A partir da 0.2.0, a app procura versões novas ao arrancar (pode desligar-se nas Definições) e só instala quando o utilizador aceita. Os pacotes de actualização vão assinados com a chave da Eter Growth e a app recusa qualquer pacote que não esteja assinado por ela.

Os instaladores ainda não têm assinatura de código do Windows nem da Apple. Na primeira instalação, o SmartScreen ou o Gatekeeper vão avisar.

Contacto: geral@etergrowth.com
