---
title: Información del proceso
description: El sistema mantiene una lista de procesos en ejecución. Puede recuperar los identificadores para estos procesos mediante una llamada a la función EnumProcesses. Esta función rellena una matriz de valores DWORD con los identificadores de todos los procesos del sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359113"
---
# <a name="process-information"></a>Información del proceso

El sistema mantiene una lista de procesos en ejecución. Puede recuperar los identificadores para estos procesos mediante una llamada a la función [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Esta función rellena una matriz de valores **DWORD** con los identificadores de todos los procesos del sistema.

Muchas funciones de PSAPI requieren un identificador de proceso. Para obtener un identificador de proceso para un proceso en ejecución, pase su identificador de proceso (Obtenido de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) a la función [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) . Recuerde llamar a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) cuando termine con el identificador del proceso.

 

 