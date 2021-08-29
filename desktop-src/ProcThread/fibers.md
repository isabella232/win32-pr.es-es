---
description: Una fibra es una unidad de ejecución que la aplicación debe programar manualmente.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: Fibras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fe8a23c8384f786cb60d6075e2289c403d272f0a899653738d031be09cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886715"
---
# <a name="fibers"></a>Fibras

Una *fibra* es una unidad de ejecución que la aplicación debe programar manualmente. Las fibras se ejecutan en el contexto de los subprocesos que las programan. Cada subproceso puede programar varias fibras. En general, las fibras no proporcionan ventajas con respecto a una aplicación multiproceso bien diseñada. Sin embargo, el uso de fibras puede facilitar el puerto de las aplicaciones diseñadas para programar sus propios subprocesos.

Desde el punto de vista del sistema, una fibra asume la identidad del subproceso que la ejecuta. Por ejemplo, si una fibra accede al almacenamiento [local](thread-local-storage.md) de subprocesos (TLS), está accediendo al almacenamiento local del subproceso que lo ejecuta. Además, si una fibra llama a la [**función ExitThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) se cierra el subproceso que la ejecuta. Sin embargo, una fibra no tiene la misma información de estado asociada que la asociada a un subproceso. La única información de estado que se mantiene para una fibra es su pila, un subconjunto de sus registros y los datos de fibra proporcionados durante la creación de la fibra. Los registros guardados son el conjunto de registros que normalmente se conservan en una llamada de función.

Las fibras no se programan de forma preferente. Para programar una fibra, cambie a ella desde otra fibra. El sistema todavía programa subprocesos para que se ejecuten. Cuando se adelanta un subproceso que ejecuta fibras, se adelanta su fibra actualmente en ejecución, pero permanece seleccionada. La fibra seleccionada se ejecuta cuando se ejecuta su subproceso.

Antes de programar la primera fibra, llame a [**la función ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) para crear un área en la que guardar la información de estado de la fibra. El subproceso que realiza la llamada es ahora la fibra que se está ejecutando actualmente. La información de estado almacenada para esta fibra incluye los datos de fibra pasados como argumento a **ConvertThreadToFiber.**

La [**función CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) se usa para crear una nueva fibra a partir de una fibra existente. la llamada requiere el tamaño de pila, la dirección inicial y los datos de fibra. La dirección inicial suele ser una función proporcionada por el usuario, denominada función de fibra, que toma un parámetro (los datos de fibra) y no devuelve un valor. Si la función de fibra vuelve, se cierra el subproceso que ejecuta la fibra. Para ejecutar cualquier fibra creada con **CreateFiber,** llame a la [**función SwitchToFiber.**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) Puede llamar a **SwitchToFiber con** la dirección de una fibra creada por un subproceso diferente. Para ello, debe devolver la dirección al otro subproceso cuando llamó a **CreateFiber** y debe usar la sincronización adecuada.

Una fibra puede recuperar los datos de fibra llamando a la macro [**GetFiberData.**](/windows/win32/api/winnt/nf-winnt-getfiberdata) Una fibra puede recuperar la dirección de fibra en cualquier momento llamando a la [**macro GetCurrentFiber.**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber)

## <a name="fiber-local-storage"></a>Fibra local Storage

Una fibra puede usar *el almacenamiento local de* fibra (FLS) para crear una copia única de una variable para cada fibra. Si no se produce ninguna conmutación de fibra, FLS actúa exactamente igual que el [almacenamiento local de subprocesos.](thread-local-storage.md) Las funciones FLS [**(FlsAlloc,**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc) [**FlsFree,**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree) [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)y [**FlsSetValue)**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)manipulan la FLS asociada al subproceso actual. Si el subproceso ejecuta una fibra y la fibra se cambia, también se cambia el FLS.

Para limpiar los datos asociados a una fibra, llame a [**la función DeleteFiber.**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) Estos datos incluyen la pila, un subconjunto de los registros y los datos de fibra. Si la fibra que se está ejecutando actualmente llama **a DeleteFiber,** su subproceso llama [**a ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) y finaliza. Sin embargo, si la fibra seleccionada de un subproceso se elimina mediante una fibra que se ejecuta en otro subproceso, es probable que el subproceso con la fibra eliminada finalice de forma anómala porque se ha liberando la pila de fibra.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de fibras](using-fibers.md)
</dt> </dl>

 

 
