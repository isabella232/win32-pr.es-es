---
description: La \_ exclusión mutua MSIExecute se establece solo al procesar la tabla InstallExecuteSequence, la tabla AdminExecuteSequence o la tabla AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute exclusión mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909173"
---
# <a name="_msiexecute-mutex"></a>\_Exclusión mutua MSIExecute

La \_ exclusión mutua MSIExecute se establece solo al procesar la tabla [InstallExecuteSequence](installexecutesequence-table.md), la tabla [AdminExecuteSequence](adminexecutesequence-table.md)o la tabla [AdvtExecuteSequence](advtexecutesequence-table.md).

Dado que no se pueden ejecutar dos instalaciones en el mismo proceso, un intento de llamar a la interfaz de programación de aplicaciones (API) del instalador devuelve la instalación de ERROR \_ \_ que ya se \_ está ejecutando (1618) en dos casos:

-   Mientras \_ se establece la exclusión mutua MSIExecute.
-   Mientras el proceso actual está procesando la [tabla InstallUISequence](installuisequence-table.md) o la [tabla AdminUISequence](adminuisequence-table.md).

Consulte los mensajes de [registro de eventos](event-logging.md) para obtener información sobre la aplicación que se va a instalar.

En los casos en los que no resulta práctico devolver un \_ error en la instalación de un error \_ \_ , se puede recuperar el estado actual del servicio de Windows Installer antes de intentar iniciar la instalación mediante la función [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) . El servicio Windows Installer se está ejecutando actualmente si el valor del miembro **dwControlsAccepted** de la estructura [**de \_ \_ proceso de estado de servicio**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) devuelto es el **\_ \_ cierre del servicio Accept**.

**Windows Installer 2,0:** No compatible. El uso de la función [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) para recuperar el estado actual del servicio Windows Installer requiere Windows Installer versión 3,0 o superior.

 

 
