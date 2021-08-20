---
title: Funciones básicas de la API de Shell de cliente
description: En la tabla siguiente se proporciona información general sobre las funciones principales de Windows API de Shell de cliente de Administración remota (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36a081723af60acf08aa9b4123cc124c2635371bfb50053da457289343ceec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113348"
---
# <a name="client-shell-api-core-functions"></a>Funciones básicas de la API de Shell de cliente

En la tabla siguiente se proporciona información general sobre las funciones principales de Windows API de Shell de cliente de Administración remota (WinRM).



| Funciones principales                                                   | Descripción                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManCloseCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Cierra un comando.                                                                                                                                                               |
| [**WSManCloseOperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Cierra una operación.                                                                                                                                                            |
| [**WSManCloseSession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Cierra una sesión de WinRM.                                                                                                                                                         |
| [**WSManCloseShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Cierra un objeto de shell.                                                                                                                                                          |
| [**WSManConnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Se conecta a una sesión de servidor existente.                                                                                                                                         |
| [**WSManConnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Se conecta a un comando existente que se ejecuta en un shell.                                                                                                                             |
| [**WSManCreateSession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Crea una sesión de WinRM.                                                                                                                                                        |
| [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Crea un objeto de shell.                                                                                                                                                         |
| [**WSManCreateShellEx**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Crea un objeto de shell con la misma funcionalidad que la función [**WSManCreateShell,**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) con la adición de un identificador de shell especificado por el cliente.          |
| [**WSManDeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Desinicializa la pila de cliente de WinRM.                                                                                                                                           |
| [**WSManDisconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Desconecta la conexión de red de un shell activo y sus comandos asociados.                                                                                              |
| [**WSManInitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Inicializa WinRM.                                                                                                                                                              |
| [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Recibe la salida del shell.                                                                                                                                                          |
| [**WSManReconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Vuelve a conectar una sesión de shell desconectada previamente. Para volver a conectar los comandos asociados de la sesión de shell, use [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Vuelve a conectar un comando previamente desconectado.                                                                                                                                   |
| [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Ejecuta un comando de shell.                                                                                                                                                           |
| [**WSManRunShellCommandEx**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Proporciona la misma funcionalidad que la [**función WSManRunShellCommand,**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) con la adición de una opción de identificador de comando.                                 |
| [**WSManSendShellInput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Envía la entrada a un shell.                                                                                                                                                         |
| [**WSManSignalShell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Señala un shell.                                                                                                                                                                |



 

 

 




