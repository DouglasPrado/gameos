# Arch Gamer ISO - Estrutura Inicial

Este projeto é uma base para criar sua própria distro gamer baseada no Arch Linux, com boot direto no EmulationStation (modo console) e opção de Desktop (KDE Plasma).

## Estrutura de Pastas

```
.
├── airootfs/
│   ├── etc/
│   │   ├── samba/
│   │   │   └── smb.conf
│   │   └── systemd/
│   │       └── system/
│   │           └── multi-user.target.wants/
│   ├── root/
│   │   └── .bash_profile
│   └── usr/
│       └── bin/
│           └── start-desktop
├── packages.x86_64
├── build.sh
└── README.md
```

## Passos para uso

1. **Edite o arquivo `packages.x86_64`** para adicionar/remover pacotes conforme sua necessidade.
2. **Configure o Samba** em `airootfs/etc/samba/smb.conf` para compartilhamento de ROMs.
3. **Personalize o autostart** em `airootfs/root/.bash_profile` (por padrão inicia o EmulationStation).
4. **Script para Desktop Mode** em `airootfs/usr/bin/start-desktop` (inicia o KDE Plasma via SDDM).
5. **Habilite serviços no boot** criando symlinks em `airootfs/etc/systemd/system/multi-user.target.wants/` (veja o README.txt lá dentro).
6. **Gere a ISO** executando:
   ```bash
   chmod +x airootfs/usr/bin/start-desktop
   ./build.sh
   ```
7. **Teste a ISO** em uma VM ou hardware real.

## Dicas

- Para adicionar temas, wallpapers ou configs extras, coloque os arquivos dentro de `airootfs/` na estrutura correspondente.
- Para adicionar scripts pós-instalação, coloque em `airootfs/root/`.

---

Qualquer dúvida ou para customizações avançadas, consulte a [Wiki do Archiso](https://wiki.archlinux.org/title/Archiso) ou peça ajuda aqui!
