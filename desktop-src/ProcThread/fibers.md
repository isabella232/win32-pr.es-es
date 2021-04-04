---
description: Una fibra es una unidad de ejecución que debe ser programada manualmente por la aplicación.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: Fibra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813771"
---
# <a name="fibers"></a>Fibra

Una *fibra* es una unidad de ejecución que debe ser programada manualmente por la aplicación. Las fibras se ejecutan en el contexto de los subprocesos que las programan. Cada subproceso puede programar varios fibras. En general, las fibras no proporcionan ventajas en una aplicación multiproceso bien diseñada. Sin embargo, el uso de fibras puede facilitar el traslado de aplicaciones diseñadas para programar sus propios subprocesos.

Desde el punto de vista del sistema, una fibra supone la identidad del subproceso que la ejecuta. Por ejemplo, si una fibra tiene acceso al [almacenamiento local de subprocesos](thread-local-storage.md) (TLS), tiene acceso al almacenamiento local de subprocesos del subproceso que lo está ejecutando. Además, si una fibra llama a la función [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) , el subproceso que lo está ejecutando finaliza. Sin embargo, una fibra no tiene la misma información de estado asociada que la asociada a un subproceso. La única información de estado que se mantiene para una fibra es su pila, un subconjunto de sus registros y los datos de fibra proporcionados durante la creación de fibra. Los registros guardados son el conjunto de registros que normalmente se conservan a través de una llamada de función.

Las fibras no se programan de forma preferente. Puede programar una fibra cambiando a ella desde otra fibra. El sistema sigue programando los subprocesos para ejecutarse. Cuando se modifica un subproceso que ejecuta fibras, se retiene la fibra que se está ejecutando actualmente, pero permanece seleccionada. La fibra seleccionada se ejecuta cuando se ejecuta el subproceso.

Antes de programar la primera fibra, llame a la función [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) para crear un área en la que guardar la información de estado de fibra. El subproceso que realiza la llamada es ahora la fibra que se está ejecutando actualmente. La información de estado almacenada para esta fibra incluye los datos de fibra pasados como argumento a **ConvertThreadToFiber**.

La función [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) se usa para crear una nueva fibra a partir de una fibra existente. la llamada requiere el tamaño de la pila, la dirección inicial y los datos de fibra. Normalmente, la dirección de inicio es una función proporcionada por el usuario, denominada función de fibra, que toma un parámetro (los datos de fibra) y no devuelve un valor. Si la función de fibra devuelve, el subproceso que ejecuta la fibra sale. Para ejecutar cualquier fibra creada con **CreateFiber**, llame a la función [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) . Puede llamar a **SwitchToFiber** con la dirección de una fibra creada por un subproceso diferente. Para ello, debe tener la dirección devuelta al otro subproceso cuando llame a **CreateFiber** y debe usar la sincronización adecuada.

Una fibra puede recuperar los datos de fibra llamando a la macro [**GetFiberData**](/windows/win32/api/winnt/nf-winnt-getfiberdata) . Una fibra puede recuperar la dirección de fibra en cualquier momento llamando a la macro [**GetCurrentFiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) .

## <a name="fiber-local-storage"></a>Almacenamiento local de fibra

Una fibra puede usar el *almacenamiento local de fibra* (FLS) para crear una copia única de una variable para cada fibra. Si no se produce la conmutación de fibra, FLS actúa exactamente igual que el [almacenamiento local del subproceso](thread-local-storage.md). Las funciones FLS ([**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc), [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree), [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)y [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) manipulan el FLS asociado al subproceso actual. Si el subproceso está ejecutando una fibra y se cambia la fibra, también se cambia el FLS.

Para limpiar los datos asociados a una fibra, llame a la función [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) . Estos datos incluyen la pila, un subconjunto de los registros y los datos de fibra. Si la fibra que se está ejecutando actualmente llama a **DeleteFiber**, su subproceso llama a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) y termina. Sin embargo, si una fibra que se ejecuta en otro subproceso elimina la fibra seleccionada de un subproceso, es probable que el subproceso con la fibra eliminada finalice de forma anómala porque se ha liberado la pila de fibra.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de fibras](using-fibers.md)
</dt> </dl>

 

 
