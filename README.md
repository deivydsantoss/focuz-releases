# Focuz

O Focuz é um app de organização da vida pessoal: tarefas, projetos, hábitos,
metas, agenda, notas, estudos, leitura, treinos, dieta, finanças e mais, num
lugar só. Os dados ficam guardados no próprio aparelho, sem conta e sem
servidor. Dois aparelhos pareados (por exemplo o PC e o celular) se
sincronizam direto pela mesma rede Wi‑Fi.

Este repositório guarda só os instaladores de cada versão.

## Baixar

Todos os arquivos da versão mais recente estão em
**[Releases → Latest](https://github.com/deivydsantoss/focuz-releases/releases/latest)**:

| Aparelho | Arquivo |
| --- | --- |
| PC Linux, qualquer distribuição (recomendado) | [`Focuz_<versão>_amd64.AppImage`](https://github.com/deivydsantoss/focuz-releases/releases/latest) |
| PC Ubuntu, Debian e derivados | [`Focuz_<versão>_amd64.deb`](https://github.com/deivydsantoss/focuz-releases/releases/latest) |
| Celular Android (ARM 64 bits) | [`Focuz-<versão>.apk`](https://github.com/deivydsantoss/focuz-releases/releases/latest) |

Os arquivos `.sig` e `latest.json` são usados pelo próprio app para se
atualizar; não precisa baixá-los.

## Instalar

### AppImage (qualquer Linux)

```bash
chmod +x Focuz_*_amd64.AppImage
./Focuz_*_amd64.AppImage
```

Não precisa instalar: guarde o arquivo onde quiser e abra. É o formato
recomendado, porque se atualiza sozinho sem pedir senha.

### .deb (Ubuntu, Debian e derivados)

```bash
sudo apt install ./Focuz_*_amd64.deb
```

O Focuz aparece no menu de aplicativos. Para remover: `sudo apt remove focuz`.

### Android

1. Baixe o `.apk` no celular e abra o arquivo.
2. Na primeira vez o Android pede para **permitir instalar apps desta fonte**:
   toque em **Configurações**, ligue a opção e volte.
3. Se o Play Protect avisar que o app é desconhecido, toque em **Instalar
   mesmo assim** (o app não está na Play Store).

### Firewall (para sincronizar)

No PC, libere a porta **TCP 47615** e o mDNS (**UDP 5353**) na rede de casa,
por exemplo com `sudo ufw allow 47615/tcp && sudo ufw allow 5353/udp`.

## Atualizações

A partir da versão **0.4.0** o app se atualiza sozinho:

- **PC:** com internet, ele procura versão nova ao abrir e a cada 6 horas.
  Quando há, aparece "Focuz X disponível — Atualizar"; ao clicar, ele baixa,
  instala e reinicia. Nada é instalado sem o seu clique. No `.deb` o sistema
  pede a sua senha para instalar.
- **Android:** aparece "Nova versão X — Baixar". O botão abre o APK novo no
  navegador; instale por cima do app atual e seus dados continuam.

Em **Ajustes → Sobre** dá para ver a versão instalada e verificar à mão.

Quem usa a **0.3.0 ou anterior** precisa baixar e instalar a versão mais
recente daqui uma vez; depois disso as atualizações chegam pelo app.
