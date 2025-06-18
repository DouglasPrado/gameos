Coloque aqui os symlinks para os serviços que você deseja habilitar no boot da ISO.

Exemplo de serviços recomendados para sua distro gamer:
- NetworkManager.service
- smb.service
- nmb.service
- sunshine.service

Você pode criar os symlinks assim:
ln -s /usr/lib/systemd/system/NetworkManager.service NetworkManager.service
ln -s /usr/lib/systemd/system/smb.service smb.service
ln -s /usr/lib/systemd/system/nmb.service nmb.service
ln -s /usr/lib/systemd/system/sunshine.service sunshine.service 