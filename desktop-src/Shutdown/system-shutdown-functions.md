---
description: Las siguientes funciones se usan con el apagado del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funciones de apagado del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664345"
---
# <a name="system-shutdown-functions"></a>Funciones de apagado del sistema

Las siguientes funciones se usan con el apagado del sistema.



| Función                                                         | Descripción                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Detiene un apagado del sistema que se ha iniciado.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Cierra la sesión del usuario interactivo.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Cierra la sesión del usuario interactivo, apaga el sistema o lo apaga y reinicia.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Inicia un apagado y reinicio del equipo especificado y reinicia las aplicaciones que se han registrado para el reinicio.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Inicia un apagado y un reinicio opcional del equipo especificado.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Inicia un apagado y un reinicio opcional del equipo especificado y, opcionalmente, registra el motivo del apagado.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Bloquea la pantalla de la estación de trabajo.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indica que el sistema no se puede apagar y establece una cadena de motivo que se mostrará al usuario si se inicia el apagado del sistema. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indica que el sistema se puede apagar y libera la cadena de motivo.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Recupera la cadena de motivo establecida por la [**función ShutdownBlockReasonCreate.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)                     |



 

 

 



