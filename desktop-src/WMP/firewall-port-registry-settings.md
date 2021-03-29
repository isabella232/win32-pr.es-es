---
title: Configuración del registro del puerto del firewall
description: Configuración del registro del puerto del firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, configuración del registro del puerto del firewall
- Windows Media Player, configuración del registro de puertos
- Media Player de Windows, registro
- registro, configuración de puerto de Firewall
- registro, configuración de Puerto
- registro, configuración para Windows Media Player
- configuración del registro del puerto del firewall
- configuración del registro de Puerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903184"
---
# <a name="firewall-port-registry-settings"></a>Configuración del registro del puerto del firewall

Windows Media Player coloca entradas en el registro para que los firewalls puedan determinar si se deben abrir o cerrar los puertos utilizados por el uso compartido de la biblioteca multimedia.

**Entrada del registro AcceptedEULA**

Windows Media Player usa la siguiente entrada del registro para indicar si el usuario ha aceptado el contrato de licencia para el usuario final (CLUF).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Un valor de 1 indica que el usuario ha aceptado el contrato de licencia. Un valor de 0 indica que el usuario no ha aceptado el contrato de licencia.

**Entrada del registro WMPNSSFirewallPortsOpen**

Windows Media Player usa la siguiente entrada del registro para indicar si el usuario ha elegido compartir su biblioteca multimedia con otros equipos de una red doméstica.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Un valor de 1 indica que el usuario ha elegido compartir la biblioteca. Un valor de 0 indica que el usuario ha elegido no compartir la biblioteca.

**Puertos relacionados con el uso compartido de la biblioteca multimedia**

En Windows Vista, si la entrada del registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben abrirse los puertos siguientes.



| Port          | Protocolo                  | Proceso                         | Dirección            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | RTSP DE TCP                  | wmpnetwk.exe                    | entrante y saliente |
| 8554-8558   | RTSP DE TCP                  | wmpnetwk.exe                    | entrante y saliente |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | entrante y saliente |
| 50004-50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | entrante y saliente |
| 1900          | SSDP DE UDP                  | SSDPsrv en svchost.exe          | entrante y saliente |
| 2869          | SSDP de TCP, UPnP            | SSDPsrv/UPnPHost en svchost.exe | hacia la ciudad              |
| 10280-10284 | Registro de WMDRM-ND UDP | wmpnetwk.exe                    | entrante y saliente |
| 10243         | HTTP DE TCP                  | wmpnetwk.exe                    | hacia la ciudad              |
| 2177          | QWAVE TCP UDP             | svchost.exe                     | entrante y saliente |



 

En Windows Vista, si la entrada del registro **AcceptedEULA** tiene un valor de 1, deben abrirse los puertos siguientes.



| Port          | Protocolo       | Proceso                         | Dirección            |
|---------------|----------------|---------------------------------|----------------------|
| Todos los puertos UDP | RTP DE UDP, MSB   | wmplayer.exe, cualquier subred        | hacia la ciudad              |
| 1900          | SSDP DE UDP       | SSDPsrv/UPnPHost en svchost.exe | entrante y saliente |
| 2869          | SSDP de TCP, UPnP | SSDPsrv, UPnPHost               | hacia la ciudad              |



 

En Microsoft Windows XP, si la entrada del registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben abrirse los puertos siguientes.



| Port          | Protocolo                  | Proceso                         | Dirección            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | SSDP DE UDP                  | SSDPsrv en svchost.exe          | entrante y saliente |
| 2869          | SSDP de TCP, UPnP            | SSDPsrv/UPnPHost en svchost.exe | hacia la ciudad              |
| 10280-10284 | Registro de WMDRM-ND UDP | wmpnetwk.exe                    | entrante y saliente |
| 10243         | HTTP DE TCP                  | wmpnetwk.exe                    | hacia la ciudad              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro**](registry-settings.md)
</dt> </dl>

 

 




