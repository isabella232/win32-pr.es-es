---
description: La función CreateProcess permite a un depurador iniciar un proceso y depurarlo.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funciones de proceso para la depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dec70de05e9b77cd3ff0b2ee8cd01c90ded2987f7ba1cacc3530f040344915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162636"
---
# <a name="process-functions-for-debugging"></a>Funciones de proceso para la depuración

La [**función CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite a un depurador iniciar un proceso y depurarlo. El *parámetro fdwCreate* de **CreateProcess** se usa para especificar el tipo de operación de depuración. Si se especifica la marca DEBUG PROCESS para el parámetro , un depurador depura el nuevo proceso y todos los descendientes del proceso, siempre que los descendientes se crean sin la marca \_ DEBUG \_ PROCESS.

Si las marcas DEBUG PROCESS y DEBUG ONLY THIS PROCESS se especifican para fdwCreate , un depurador depura el nuevo proceso, pero \_ \_ ninguno de sus \_ \_ descendientes. 

Un depurador puede depurar otro mediante la creación de un proceso con la marca DEBUG \_ PROCESS. El nuevo proceso (el depurador que se depura) debe crear un proceso con la marca DEBUG \_ PROCESS.

La [**función OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permite que un depurador obtenga el identificador de un proceso existente. (La [**función DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa este identificador para asociar el depurador al proceso). Normalmente, los depuradores abren un proceso con las marcas PROCESS VM READ y \_ \_ PROCESS VM \_ \_ WRITE. El uso de estas marcas permite al depurador leer y escribir en la memoria virtual del proceso mediante las funciones [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) y [**WriteProcessMemory.**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) Para obtener más información, vea [**Procesos y subprocesos.**](../procthread/processes-and-threads.md)

 

 
