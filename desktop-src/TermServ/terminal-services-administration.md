---
title: Servicios de Escritorio remoto administración
description: La API Servicios de Escritorio remoto permite enumerar y administrar servidores, sesiones de cliente y procesos de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46df6277b924d25608b3c4def5074c1f156738e23d114de075af01521953e7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000285"
---
# <a name="remote-desktop-services-administration"></a>Servicios de Escritorio remoto administración

La API Servicios de Escritorio remoto permite enumerar y administrar servidores, sesiones de cliente y procesos de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).

Para recuperar los nombres de todos los servidores host de sesión de Escritorio remoto de un dominio, llame a la función [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) para enumerar los servidores del tipo TERMINALSERVER SV \_ \_ TYPE. Para abrir un identificador a un servidor host de sesión de Escritorio remoto específico, pase el nombre del servidor en una llamada a la [**función WTSOpenServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) Cuando haya terminado de usar el identificador, descríbalo llamando a la [**función WTSCloseServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)

Puede usar el identificador devuelto por **WTSOpenServer para** realizar las siguientes operaciones en el servidor.



| Función                                                         | Operación                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Desconecta el cliente de una sesión especificada. La sesión permanece activa y el usuario puede iniciar sesión de nuevo para conectarse a la misma sesión.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Devuelve una lista de sesiones en el servidor host de sesión de Escritorio remoto especificado.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Devuelve una lista de procesos en el servidor host de sesión de Escritorio remoto especificado.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Cierra la sesión especificada.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Devuelve información sobre la sesión especificada en el servidor host de sesión de Escritorio remoto especificado.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Muestra un cuadro de mensaje en la presentación del cliente de una sesión especificada.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Cierra y, opcionalmente, reinicia un servidor host de sesión de Escritorio remoto especificado.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Finaliza un proceso especificado en un servidor host de sesión de Escritorio remoto especificado.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Abre un identificador al final del servidor de un canal virtual especificado. Para obtener más información sobre los canales virtuales, vea [Uso de Servicios de Escritorio remoto canales virtuales.](using-terminal-services-virtual-channels.md) |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Espera un evento, como la creación de una sesión de cliente o un usuario que inicia sesión en el servidor host de sesión de Escritorio remoto.                                                                                                  |



 

Varias de estas funciones asignan búferes para devolver información al autor de la llamada. Cuando haya terminado de usar el búfer, desconéctelo llamando a la [**función WTSFreeMemory.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)

 

 