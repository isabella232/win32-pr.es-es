---
description: Para depurar un proceso que ya se está ejecutando, el depurador debe usar DebugActiveProcess con el identificador de proceso. Para recuperar una lista de identificadores de proceso, use la función EnumProcesses o Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Depuración de un proceso en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3cf141da9905c76659c2ae11e9b82e2e2f5fee9bd934dce835b129678995ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279355"
---
# <a name="debugging-a-running-process"></a>Depuración de un proceso en ejecución

Para depurar un proceso que ya se está ejecutando, el depurador debe usar [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) con el identificador de proceso. Para recuperar una lista de identificadores de proceso, use las funciones [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First.**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)

[**DebugActiveProcess asocia**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) el depurador al proceso activo. En este caso, solo se puede depurar el proceso activo; sus procesos secundarios no pueden. El depurador debe tener acceso adecuado al proceso en ejecución para usar **DebugActiveProcess.** Para obtener más información sobre los derechos de acceso, [vea Access Control](../secauthz/access-control.md).

Después de que el depurador se haya creado o asociado al proceso que pretende depurar, el sistema notifica al depurador todos los eventos de depuración que se producen en el proceso y, si se especifican, en los procesos secundarios. Para obtener más información sobre la depuración de eventos, vea [Eventos de depuración](debugging-events.md).

Para separar del proceso que se está depurando, el depurador debe usar la [**función DebugActiveProcessStop.**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)

 

 
