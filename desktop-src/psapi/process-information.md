---
title: Procesar información
description: El sistema mantiene una lista de procesos en ejecución. Puede recuperar los identificadores de estos procesos llamando a la función EnumProcesses. Esta función rellena una matriz de valores DWORD con los identificadores de todos los procesos del sistema.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094896"
---
# <a name="process-information"></a>Procesar información

El sistema mantiene una lista de procesos en ejecución. Puede recuperar los identificadores de estos procesos llamando a la [**función EnumProcesses.**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) Esta función rellena una matriz de valores **DWORD** con los identificadores de todos los procesos del sistema.

Muchas funciones de PSAPI requieren un identificador de proceso. Para obtener un identificador de proceso para un proceso en ejecución, pase su identificador de proceso (obtenido de [**EnumProcesses)**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)a la [**función OpenProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) Recuerde llamar a la [**función CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) cuando haya terminado con el identificador de proceso.

 

 