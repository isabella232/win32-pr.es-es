---
description: La función CreateProcess permite a un depurador iniciar un proceso y depurarlo.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funciones de proceso para depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998224"
---
# <a name="process-functions-for-debugging"></a>Funciones de proceso para depuración

La función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite a un depurador iniciar un proceso y depurarlo. El parámetro *fdwCreate* de **CreateProcess** se usa para especificar el tipo de operación de depuración. Si \_ se especifica la marca de proceso de DEpuración para el parámetro, un depurador depura el nuevo proceso y todos los descendientes del proceso, siempre que los descendientes se creen sin la marca de proceso de DEpuración \_ .

Si el proceso de depuración \_ y la DEpuración \_ solo \_ \_ se especifican en *fdwCreate*, un depurador devuelverá el nuevo proceso pero ninguno de sus descendientes.

Un depurador puede depurar otro mediante la creación de un proceso con la marca DEBUG Process (proceso de depuración) \_ . El nuevo proceso (el depurador que se está depurando) debe crear un proceso con la marca DEBUG Process (proceso de depuración) \_ .

La función [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permite a un depurador obtener el identificador de un proceso existente. (La función [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa este identificador para adjuntar el depurador al proceso). Normalmente, los depuradores abren un proceso con las marcas de escritura de VM de proceso \_ \_ lectura y procesamiento de máquina virtual \_ \_ . El uso de estas marcas permite que el depurador Lea y escriba en la memoria virtual del proceso mediante el uso de las funciones [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) y [**writeprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) . Para obtener más información, vea [**procesos y subprocesos**](../procthread/processes-and-threads.md).

 

 
