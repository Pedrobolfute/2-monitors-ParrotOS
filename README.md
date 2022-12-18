# 2-monitors-ParrotOS

Debian based

**PT_BR:** 2 monitores no ParrotOS usando bumblebee para notebooks hibridos como o da lonovo l340.

**EN_US:** 2 monitors in parrotOS using bumblebee for hybrid notebooks like Lenovo l340.

## PT_BR

Após baixar os pacotes da nvidia e bumblebee (nvidia-driver, primus-nvidia, bumblebee-nvidia)...

- xorg.conf coloca/subistitui dentro de **/etc/X11/xorg.conf**

  - Verifique na Section Device o BusID dos barramentos se estão conforme o do seu computador, se não estiver troque pelo seu, mas seguindo aquela mesma estrutura do arquivo (decimal). Use o comando lspci para verificar.

    > lspci | grep -i vga

- 20-intel.conf coloca/subistitui dentro de **/etc/X11/xorg.conf.d/20-intel.conf**

- xorg.conf.nvidia coloca/subistitui dentro de **/etc/bumblebee/xorg.conf.nvidia**

## EN_US

- After downloaded the packets from nvidia and bumblebee (nvidia-driver, primus-nvidia, bumblebee-nvidia)...

- xorg.conf put inside directory X11 likes: **etc/X11/xorg.conf**

  - Verify the BusID in Section Device. The BusID have to be your PC bus. To verify what is your bus use the command lspci, and replace for your bus but using the struct from the archive (decimal).

    > lspci | grep -i vga

- 20-intel.conf put inside directory xorg.conf.d likes: **/etc/X11/xorg.conf.d/20-intel.conf**

- xorg.conf.nvidia put inside directory bumblebee likes: **/etc/bumblebee/xorg.conf.nvidia**
