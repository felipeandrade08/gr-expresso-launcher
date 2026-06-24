# 🚛 GR EXPRESSO — Launcher

Aplicativo desktop oficial da transportadora virtual **GR EXPRESSO**, responsável
por conectar o **Euro Truck Simulator 2 (ETS2)** ao painel web do sistema.

Ele lê a telemetria do jogo em tempo real e envia automaticamente para o servidor:
viagens, abastecimentos, status do motorista e alertas de manutenção — sem precisar
preencher nada manualmente no site.

> 🌐 Painel web: [gr-expresso-sr5p.vercel.app](https://gr-expresso-sr5p.vercel.app)

---

## 📥 Download

Baixe sempre a versão mais recente direto pela página de downloads do sistema:

➡️ **[gr-expresso-sr5p.vercel.app/downloads.html](https://gr-expresso-sr5p.vercel.app/downloads.html)**

Ou pegue o instalador diretamente nesta seção:

➡️ **[Releases](../../releases/latest)** → baixe o arquivo `setup_GR_Expresso.exe`

---

## ✅ Pré-requisitos

| Requisito | Detalhe |
|---|---|
| Sistema | Windows 10 / 11 (64-bit) |
| Jogo | Euro Truck Simulator 2 (Steam) |
| Plugin | [SCS Telemetry SDK](https://github.com/RenCloud/scs-sdk-plugin) instalado no ETS2 |
| Conta | Cadastro **aprovado** no painel GR EXPRESSO |
| Internet | Conexão ativa durante as viagens |

> O plugin de telemetria (`scs-telemetry.dll`) é **obrigatório** e separado do
> Launcher — sem ele, o jogo não expõe os dados na shared memory e o Launcher
> não tem o que ler. Veja como instalar na
> [página de Downloads](https://gr-expresso-sr5p.vercel.app/downloads.html).

---

## 🚀 Como instalar

1. Baixe o `setup_GR_Expresso.exe` na seção [Releases](../../releases/latest).
2. Execute o instalador como **administrador**.
3. Abra o Launcher e faça **login com a mesma conta do painel web**.
4. Configure a **placa do veículo** que você vai usar nas viagens.
5. Inicie o ETS2 normalmente — o Launcher detecta o jogo e começa a
   sincronizar tudo automaticamente.

> ⚠️ Se o Windows mostrar o aviso azul "o Windows protegeu o computador",
> clique em **"Mais informações"** → **"Executar assim mesmo"**. Isso acontece
> porque o instalador veio da internet — é normal e seguro neste caso.

---

## 🔌 O que o Launcher sincroniza automaticamente

Enquanto você joga, o Launcher conversa com a API do GR EXPRESSO
(`/api/telemetria/*`) e mantém tudo atualizado em tempo real:

- **Status ao vivo** — posição, velocidade e nível de combustível
- **Viagens** — abertura e finalização conforme os fretes feitos no jogo
- **Abastecimentos** — detectados pela variação do nível de combustível
- **Alertas de manutenção** — quando o desgaste do veículo passa do limite
- **Ranking** — pontos, bônus e penalidades aplicados automaticamente
  conforme as regras do sistema (viagem concluída, excesso de velocidade,
  dano, cancelamento, etc.)

Tudo isso aparece instantaneamente no seu painel pessoal e no painel do
administrador, sem nenhuma ação manual.

---

## ⚙️ Configuração

Na primeira execução, o Launcher pede:

| Campo | Descrição |
|---|---|
| **E-mail / senha** | A mesma conta usada para entrar no painel web |
| **URL da API** | Endereço do backend (já vem configurado por padrão) |
| **Placa do veículo** | Identifica o caminhão usado nas viagens |

Essas informações ficam salvas localmente — não é necessário preencher de novo
a cada vez que abrir o Launcher.

---

## 🛟 Problemas comuns

| Sintoma | Causa provável | Solução |
|---|---|---|
| Launcher não detecta o jogo | Plugin `scs-telemetry.dll` não instalado | Reinstale o plugin na pasta `bin/win_x64/plugins/` do ETS2 |
| Erro de login | Conta ainda pendente de aprovação | Aguarde aprovação de um administrador no painel |
| Viagem não aparece no site | Sem conexão com a internet durante o jogo | Verifique sua internet e reinicie o Launcher |
| Windows bloqueia a instalação | Aviso padrão de segurança do Windows | Clique em "Mais informações" → "Executar assim mesmo" |

Se o problema persistir, entre em contato com a administração da transportadora
ou abra uma [issue](../../issues) neste repositório.

---

## 🔗 Projetos relacionados

- **[gr-expresso](https://github.com/felipeandrade08/gr-expresso)** — sistema
  web (painel administrativo + área do motorista)

---

## 📄 Licença

Distribuído para uso exclusivo dos motoristas e administradores da
transportadora virtual GR EXPRESSO. Uso livre para fins pessoais e de
comunidade dentro do Euro Truck Simulator 2.
