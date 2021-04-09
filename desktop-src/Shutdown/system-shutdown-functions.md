---
description: Las siguientes funciones se usan con el cierre del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funciones de cierre del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002070"
---
# <a name="system-shutdown-functions"></a>Funciones de cierre del sistema

Las siguientes funciones se usan con el cierre del sistema.



| Función                                                         | Descripción                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Detiene el cierre del sistema que se ha iniciado.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Cierra la sesión del usuario interactivo.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Cierra la sesión del usuario interactivo, apaga el sistema o apaga y reinicia el sistema.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Inicia el apagado y el reinicio del equipo especificado y reinicia las aplicaciones que se han registrado para reiniciarse.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Inicia el cierre y el reinicio opcional del equipo especificado.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Inicia el cierre y el reinicio opcional del equipo especificado y, opcionalmente, registra el motivo del cierre.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Bloquea la pantalla de la estación de trabajo.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indica que no se puede apagar el sistema y establece una cadena de motivo que se mostrará al usuario si se inicia el cierre del sistema. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indica que el sistema se puede apagar y libera la cadena de motivo.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Recupera la cadena de motivo establecida por la función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .                     |



 

 

 



