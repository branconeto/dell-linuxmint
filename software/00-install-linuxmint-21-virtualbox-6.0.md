#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 13/10/2022<br>
#Data de atualização: 14/01/2023<br>
#Versão: 0.06<br>
#Testado e homologado no Linux Mint 20 Ulyana, 20.1 Ulyssa, 20.2 Uma, 20.3 Una, 21 Vanessa

#Lançamentos Oficiais do Linux Mint<br>
27/07/2020 - Linux Mint 20 "Ulyana" Cinnamon released: https://www.linuxmint.com/rel_ulyana_cinnamon.php<br>
08/01/2021 - Linux Mint 20.1 "Ulyssa" Cinnamon released: https://linuxmint.com/rel_ulyssa_cinnamon.php<br>
08/07/2021 - Linux Mint 20.2 “Uma” Cinnamon released: https://www.linuxmint.com/rel_uma_cinnamon.php<br>
07/01/2022 - Linux Mint 20.3 “Una” Cinnamon released: https://www.linuxmint.com/rel_una_cinnamon.php<br>
31/07/2022 - Linux Mint 21 "Vanessa" Cinnamon released: https://www.linuxmint.com/rel_vanessa_cinnamon.php

#Tipos de Ambientes Gráficos do Linux Mint<br>
Cinnamon: https://www.linuxmint.com/rel_vanessa_cinnamon.php<br>
Mate: https://www.linuxmint.com/rel_vanessa_mate.php<br>
XFCE: https://www.linuxmint.com/rel_vanessa_xfce.php.

#Versões baseadas da Distribuição Ubuntu<br>
Linux Mint 20.x é derivado do Ubuntu Desktop 20.04.x Focal Fossa<br>
Linux Mint 21.x é derivado do Ubuntu Desktop 22.04.x Jammy Jellyfish

Primeira etapa: Download da ISO do Linux Mint

01. Link de download do Linux Mint 21 "Vanessa" Cinnamon 64 Bits: https://www.linuxmint.com/edition.php?id=299<br>
02. Escolher o Mirror (Espelho) no Brasil de: Federal University of Sao Carlos<br>
03. Salvar a ISO do Linux Mint: linuxmint-21-cinnamon-64bit.iso no seu computador<br>

Segunda etapa: Software para a gravação do Pen Drive Bootável

_ Rufus: https://rufus.ie/pt_BR/<br>
_ YUMI: https://www.pendrivelinux.com/yumi-multiboot-usb-creator/<br>
_ Etcher: https://www.balena.io/etcher/<br>
_ UNetbootin: https://unetbootin.github.io/<br>
_ Ventoy: https://www.ventoy.net/en/index.html<br>
_ Linux Live USC Creator: https://www.linuxliveusb.com/<br>

Terceira etapa: Criação e Configuração da Máquina Virtual no Oracle VirtualBOX 6.0.x<br>
Link de download do Oracle VirtualBOX: https://www.virtualbox.org/wiki/Downloads

Quarta etapa: Criando a Máquina Virtual do Linux Mint no VirtualBox

	_ Ferramentas;
		<Novo>
	_ Nome e Sistema Operacional:
		Nome: LinuxMint21
		Pasta da Máquina: (deixar o padrão do sistema) 
		Tipo: Linux
		Versão: Ubuntu (64-bit)
		<Próximo>
	_ Tamanho da memória:
		Tamanho: 4096MB
		<Próximo>
	_ Disco Rígido:
		Criar um novo disco rígido virtual agora
		<Criar>
	_ Tipo de arquivo de disco rígido
		VDI (VirtualBOX Disk Image)
		<Próximo>
	_ Armazenamento em disco rígido físico
		Dinamicamente alocado
		<Próximo>
	_ Localização e tamanho do arquivo
		Localização: (deixar o padrão do sistema)
		Tamanho do disco: 50GB
		<Criar>

Quinta etapa: Personalizando a Máquina Virtual do Linux Mint no VirtualBox

	_ Configurações da Máquina Virtual Linux (Propriedades/Configurações)
		_ Geral
			Avançado
				Área de Transferência Compartilhada: Bi-direcional
				Arrastar e Soltar: Bi-direcional
		_ Sistema
			Placa-Mãe
				Relógio da máquina retorna hora UTC: OFF (Desabilitado) 
			Processador
				Processadores: 02 CPUs
				Recursos Estendidos:
					Habilitar PAE/NX: ON (Habilitado)
					Habilitar VT-x/AMD-V Aninhado: ON (Habilitado)
		_ Monitor
			Tela
				Memória de Vídeo: 128MB
				Aceleração: Habilitar Aceleração 3D
		_ Rede
			Adaptador 1
				Habilitar Placa de Rede
				Conectado a: Placa em Modo Bridge
				Nome: (Interface padrão de acesso a Internet e Rede Local do Hospedeiro)
		<OK>

Sexta etapa: Iniciando a ISO do Linux Mint

	_ VM LinuxMint21: Iniciar
	_ Selecione o disco rígido de boot
		Selecionar um arquivo de disco óptico virtual
	_ Seletor de Discos Ópticos
		Acrescentar
		Selecione o arquivo de disco óptico virtual: linuxmint-21-cinnamon-64bit.iso
		<Abrir>
	_ Not Attached
		Selecionar: linuxmint-21-cinnamon-64bit.iso
		<Escolher>
	<Iniciar>

Sétima etapa: Iniciando a Instalação o Linux Mint

	_ Boot Inicial do Linux Mint 10 (dez segundos) inicia a instalação padrão.
		Parar o Boot: pressionar: Seta para Baixo para parar o Boot inicial
	_ Opções do Boot padrão do Linux Mint
		*Start Linux Mint 21 Cinnamon 64-Bit (Padrão)
		Start Linux Mint 21 Cinnamon 64-Bit (compatibility mode)
		OEM install (for manufacturers)
		Test memory
	
	_ Ícone Install Linux Mint
		Welcome
			Português do Brasil
			<Continuar>
		Layout do teclado
			Selecione o layout de seu teclado:
				Portuguese (Brazil)
			<Continuar>
		Codecs Multimídia
			Instalar codecs multimídia: ON (Habilitar)
			<Continuar>
		Tipo de instalação
			Apagar disco e reinstalar o Linux Mint: ON (Selecionado)
			<Instalar agora>
			<Continuar>
		Onde você está?
			Sao Paulo
			<Continuar>
		Quem é você?
			Seu nome: Robson Vaamonde
			Nome do seu computador: VirtualBox
			Escolha um nome de usuário: vaamonde
			Escolha uma senha: pti@2018
			Confirme sua senha: pti@2018
			Solicitar minha senha para entrar: ON (Selecionado)
			<Continuar>
	_ <Reiniciar agora>
	Please remove the installation medium, then press <ENTER>:
	Observação: Aguardar a reinicialização do sistema para se logar no Linux Mint.