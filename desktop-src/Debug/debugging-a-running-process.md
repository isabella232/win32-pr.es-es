---
description: Para depurar un proceso que ya se está ejecutando, el depurador debe usar DebugActiveProcess con el identificador de proceso. Para recuperar una lista de identificadores de proceso, utilice la función EnumProcesses o Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Depurar un proceso en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152741"
---
# <a name="debugging-a-running-process"></a>Depurar un proceso en ejecución

Para depurar un proceso que ya se está ejecutando, el depurador debe usar [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) con el identificador de proceso. Para recuperar una lista de identificadores de proceso, utilice la función [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) asocia el depurador al proceso activo. En este caso, solo se puede depurar el proceso activo. sus procesos secundarios no pueden. El depurador debe tener el acceso adecuado al proceso de ejecución para utilizar **DebugActiveProcess**. Para obtener más información sobre los derechos de acceso, consulte [Access Control](../secauthz/access-control.md).

Una vez que el depurador se ha creado o adjuntado al proceso que intenta depurar, el sistema notifica al depurador todos los eventos de depuración que se producen en el proceso y, si se especifica, en los procesos secundarios. Para obtener más información sobre la depuración de eventos, vea [depuración de eventos](debugging-events.md).

Para desasociar del proceso que se está depurando, el depurador debe utilizar la función [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .

 

 
