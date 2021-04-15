---
title: Administración de Servicios de Escritorio remoto
description: La API de Servicios de Escritorio remoto permite enumerar y administrar los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto), las sesiones de cliente y los procesos.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676437"
---
# <a name="remote-desktop-services-administration"></a>Administración de Servicios de Escritorio remoto

La API de Servicios de Escritorio remoto permite enumerar y administrar los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto), las sesiones de cliente y los procesos.

Para recuperar los nombres de todos los servidores host de sesión de escritorio remoto en un dominio, llame a la función [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) para enumerar los servidores del tipo \_ TERMINALSERVER de tipo SV \_ . Para abrir un identificador a un servidor host de sesión de escritorio remoto concreto, pase el nombre del servidor en una llamada a la función [**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) . Cuando haya terminado de usar el identificador, suéltelo llamando a la función [**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) .

Puede usar el identificador devuelto por **WTSOpenServer** para realizar las siguientes operaciones en el servidor.



| Función                                                         | Operación                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Desconecta el cliente de una sesión especificada. La sesión permanece activa y el usuario puede volver a iniciar sesión para conectarse a la misma sesión.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Devuelve una lista de sesiones en el servidor host de sesión de escritorio remoto especificado.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Devuelve una lista de procesos en el servidor host de sesión de escritorio remoto especificado.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Cierra la sesión especificada.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Devuelve información sobre la sesión especificada en el servidor host de sesión de escritorio remoto especificado.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Muestra un cuadro de mensaje en la pantalla del cliente de una sesión especificada.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Cierra y, opcionalmente, reinicia un servidor host de sesión de escritorio remoto especificado.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Finaliza un proceso especificado en un servidor host de sesión de escritorio remoto especificado.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Abre un identificador del extremo del servidor de un canal virtual especificado. Para obtener más información sobre los canales virtuales, consulte [uso de servicios de escritorio remoto canales virtuales](using-terminal-services-virtual-channels.md). |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Espera un evento, como la creación de una sesión de cliente o un usuario que inicia sesión en el servidor host de sesión de escritorio remoto.                                                                                                  |



 

Varias de estas funciones asignan búferes para devolver información al autor de la llamada. Cuando haya terminado de usar el búfer, libere la llamada a la función [**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) .

 

 