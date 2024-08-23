# App_Networks_Infra
Repositorio de tutoriales y apuntes.  

# Activación OfficePro Plus 2019 con CDM 

Utiliza la licencia Office Professional Pluss 2019 para activar.
```bash
Office Professional Plus 2019: NMMKJ-6RK4F-KMJVX-8D9MJ-6MWKP 
Office Standard 2019: 6NWWJ-YQWMR-QKGCB-6TMB3-9D9HK 
Project Professional 2019: B4NPR-3FKK7-T2MBV-FRQ4W-PKD2B
Project Standard 2019: C4F7P-NCP8C-6CQPT-MQHV9-JXD2M
Visio Professional 2019 
9BGNQ-K37YR-RQHF2-38RQ3-7VCBB 
Visio Standard 2019: 7TQNQ-K3YQQ-3PFH7-CCPPM-X4VQ2
Word 2019: PBX3G-NWMT6-Q7XBW-PYJGG-WXD33
Excel 2019:	TMJWT-YYNMB-3BKTF-644FC-RVXBD
PowerPoint 2019: RRNCX-C64HY-W2MM7-MCH9G-TJHMQ
Access 2019: 9N9PT-27V4Y-VJ2PD-YXFMF-YTFQT
Outlook 2019: 7HD7K-N4PVK-BHBCQ-YWQRW-XW4VK
Publisher 2019:	G2KWX-3NW6P-PY93R-JXK2T-C9Y9V
Skype for Business 2019: NCJ33-JHBBY-HTK98-MYCV8-HMKHJ
```
Instrucciones:

Sigue los siguientes pasos para activar.

1. Abre el simbolo del sistema (CMD) como administrador.

2. Copia y ejecuta el siguiente comando para ir a la ubicación de Office en tu PC:

Comando -> 64 bits:  
```bash
cd /d %ProgramFiles%\Microsoft Office\Office16   
```

Comando -> 32 bits:
```bash
cd /d %ProgramFiles(x86)%\Microsoft Office\Office16
```

En caso de que no estés seguro de la arquitectura que tienes, ejecuta ambos códigos. Uno mostrará error pero el otro se ejecutará correctamente.

3. Ejecuta el siguiente comando para convertir tu versión a VL (Licencia por Volumen): 

```bash
for /f %x in ('dir /b ..\root\Licenses16\ProPlus2019VL*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%x"
```
 
4. Copia el siguiente script en el CMD (símbolo del sistema) y pulsa enter para ejecutarlo. (Es necesario estar conectado a Internet para que funcione).

```bash
cscript ospp.vbs /setprt:1688
cscript ospp.vbs /unpkey:6MWKP >nul
cscript ospp.vbs /inpkey:NMMKJ-6RK4F-KMJVX-8D9MJ-6MWKP
cscript ospp.vbs /sethst:e8.us.to
cscript ospp.vbs /act
```
¡Listo!



Si todo sale bien, habrás activado Office 2019 de por vida, o por lo menos por 180 días.
