---
title: Firewall Port Registry Configuración
description: Firewall Port Registry Configuración
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Reproductor de Windows Media configuración del Registro de puertos de firewall
- Reproductor de Windows Media,configuración del Registro de puertos
- Reproductor de Windows Media,registry
- registro, configuración de puerto de firewall
- registry,port settings
- registry,settings for Reproductor de Windows Media
- configuración del registro de puertos de firewall
- configuración del registro de puertos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170586"
---
# <a name="firewall-port-registry-settings"></a>Firewall Port Registry Configuración

Reproductor de Windows Media las entradas en el Registro para que los firewalls puedan determinar si se deben abrir o cerrar los puertos que se usan en el uso compartido de la biblioteca multimedia.

**Entrada del Registro AcceptedEULA**

Reproductor de Windows Media usa la siguiente entrada del Registro para indicar si el usuario ha aceptado el contrato de licencia del usuario final (CLUF).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Un valor de 1 indica que el usuario ha aceptado el contrato de licencia. Un valor de 0 indica que el usuario no ha aceptado el contrato de licencia.

**WMPNSSFirewallPortsAbrir entrada del Registro**

Reproductor de Windows Media la siguiente entrada del Registro para indicar si el usuario ha elegido compartir su biblioteca multimedia con otros equipos de una red doméstica.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Un valor de 1 indica que el usuario ha elegido compartir la biblioteca. Un valor de 0 indica que el usuario ha elegido no compartir la biblioteca.

**Puertos relacionados con el uso compartido de la biblioteca multimedia**

En Windows Vista, si la entrada del Registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben estar abiertos los siguientes puertos.



| Port          | Protocolo                  | Proceso                         | Dirección            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP RTSP                  | wmpnetwk.exe                    | entrante y saliente |
| 8554 - 8558   | TCP RTSP                  | wmpnetwk.exe                    | entrante y saliente |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | entrante y saliente |
| 50004 - 50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | entrante y saliente |
| 1900          | UDP SSDP                  | SSDPsrv en svchost.exe          | entrante y saliente |
| 2869          | SSDP TCP, UPnP            | SSDPsrv/UPnPHost en svchost.exe | hacia la ciudad              |
| 10280 - 10284 | Registro DE UDP WMDRM-ND | wmpnetwk.exe                    | entrante y saliente |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | hacia la ciudad              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | entrante y saliente |



 

En Windows Vista, si la entrada del Registro **AcceptedEULA** tiene un valor de 1, deben estar abiertos los puertos siguientes.



| Port          | Protocolo       | Proceso                         | Dirección            |
|---------------|----------------|---------------------------------|----------------------|
| Todos los puertos UDP | UDP RTP, MSB   | wmplayer.exe, cualquier subred        | hacia la ciudad              |
| 1900          | UDP SSDP       | SSDPsrv/UPnPHost en svchost.exe | entrante y saliente |
| 2869          | SSDP TCP, UPnP | SSDPsrv, UPnPHost               | hacia la ciudad              |



 

En Microsoft Windows XP, si la entrada del Registro **WMPNSSFirewallPortsOpen** tiene un valor de 1, deben estar abiertos los siguientes puertos.



| Port          | Protocolo                  | Proceso                         | Dirección            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | UDP SSDP                  | SSDPsrv en svchost.exe          | entrante y saliente |
| 2869          | SSDP TCP, UPnP            | SSDPsrv/UPnPHost en svchost.exe | hacia la ciudad              |
| 10280 - 10284 | Registro DE UDP WMDRM-ND | wmpnetwk.exe                    | entrante y saliente |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | hacia la ciudad              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del Registro**](registry-settings.md)
</dt> </dl>

 

 




