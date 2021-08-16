---
description: Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas de varios procesadores debido a suposiciones que hacen que sean válidas solo en sistemas de procesador único.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problemas de sincronización y multiprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0e86a2c69cf0a0c0e56656475f73fb489f7433a94511703b3777302702bb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886213"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Problemas de sincronización y multiprocesador

Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas de varios procesadores debido a suposiciones que hacen que sean válidas solo en sistemas de procesador único.

## <a name="thread-priorities"></a>Prioridades de subprocesos

Considere un programa con dos subprocesos, uno con mayor prioridad que el otro. En un sistema de un solo procesador, el subproceso de mayor prioridad no volverá a reducir el control al subproceso de prioridad inferior porque el programador da preferencia a los subprocesos de mayor prioridad. En un sistema de varios procesadores, ambos subprocesos se pueden ejecutar simultáneamente, cada uno en su propio procesador.

Las aplicaciones deben sincronizar el acceso a las estructuras de datos para evitar condiciones de carrera. Código que supone que los subprocesos de mayor prioridad se ejecutan sin interferencias de subprocesos de prioridad inferior producirá un error en los sistemas de varios procesadores.

## <a name="memory-ordering"></a>Ordenación de memoria

Cuando un procesador escribe en una ubicación de memoria, el valor se almacena en caché para mejorar el rendimiento. De forma similar, el procesador intenta satisfacer las solicitudes de lectura de la memoria caché para mejorar el rendimiento. Además, los procesadores comienzan a capturar valores de la memoria antes de que la aplicación los solicite. Esto puede ocurrir como parte de la ejecución especulativa o debido a problemas de línea de caché.

Las memorias caché de CPU se pueden dividir en bancos a los que se puede acceder en paralelo. Esto significa que las operaciones de memoria se pueden completar sin orden. Para asegurarse de que las operaciones de memoria se completan en orden, la mayoría de los procesadores proporcionan instrucciones de barrera de memoria. Una *barrera de memoria* completa garantiza que las operaciones de lectura y escritura de memoria que aparecen antes de la instrucción de barrera de memoria se confirman en la memoria antes de cualquier operación de lectura y escritura de memoria que aparezca después de la instrucción de barrera de memoria. Una *barrera de memoria de* lectura ordena solo las operaciones de lectura de memoria y una barrera de memoria *de* escritura ordena solo las operaciones de escritura de memoria. Estas instrucciones también garantizan que el compilador deshabilite las optimizaciones que podrían reordenar las operaciones de memoria a través de las barreras.

Los procesadores pueden admitir instrucciones para las barreras de memoria con semántica de adquisición, liberación y barrera. Esta semántica describe el orden en que los resultados de una operación están disponibles. Con la adquisición de semántica, los resultados de la operación están disponibles antes que los resultados de cualquier operación que aparezca después de ella en el código. Con la semántica de versión, los resultados de la operación están disponibles después de los resultados de cualquier operación que aparezca antes en el código. La semántica de barrera combina la semántica de adquisición y versión. Los resultados de una operación con semántica de barrera están disponibles antes que los de cualquier operación que aparezca después de ella en el código y después de los de cualquier operación que aparezca antes.

En los procesadores x86 y x64 que admiten SSE2, las instrucciones son **mfence** (barrera de memoria), **lfence** (barrera de carga) y **sfence** (barrera de almacenamiento). En los procesadores ARM, las instruciones **son dmb** y **matriz**. Para más información, consulte la documentación del procesador.

Las siguientes funciones de sincronización usan las barreras adecuadas para garantizar el orden de la memoria:

-   Funciones que entran o salen de secciones críticas
-   Funciones que adquieren o liberan bloqueos SRW
-   Inicio y finalización de la inicialización única
-   **Función EnterSynchronizationBarrona**
-   Funciones que señalan objetos de sincronización
-   Funciones wait
-   Funciones entrelazados (excepto funciones con sufijo _NoFence_ o intrínsecos con _\_ sufijo nf)_

## <a name="fixing-a-race-condition"></a>Corregir una condición de carrera

El código siguiente tiene una condición de carrera en sistemas de varios procesadores porque el procesador que se ejecuta por primera vez puede escribir en la memoria principal antes de escribir `CacheComputedValue` `fValueHasBeenComputed` en la memoria `iValue` principal. Por lo tanto, un segundo procesador que se ejecuta al mismo tiempo lee como TRUE , pero el nuevo valor de sigue estando en la memoria caché del primer procesador y no se ha escrito `FetchComputedValue` `fValueHasBeenComputed` en la  `iValue` memoria.

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Esta condición de carrera anterior se puede reparar mediante la palabra clave **volatile** o la función [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) para asegurarse de que el valor de se actualiza para todos los procesadores antes de que el valor de se establezca en `iValue` `fValueHasBeenComputed` **TRUE.**

A partir de Visual Studio 2005, si se compila en modo **/volatile:ms,** el compilador usa la semántica de adquisición para las operaciones de lectura en **variables** volátiles y la semántica de versión para las operaciones de escritura en **variables** volátiles (cuando la CPU lo admite). Por lo tanto, puede corregir el ejemplo de la manera siguiente:

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

Con Visual Studio 2003, se ordenan **las** referencias **volátiles** a volátiles; el compilador no volverá a ordenar el **acceso a** variables volátiles. Sin embargo, el procesador podría volver a ordenar estas operaciones. Por lo tanto, puede corregir el ejemplo de la manera siguiente:

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de sección críticos](critical-section-objects.md)
</dt> <dt>

[Acceso a variables entrelazado](interlocked-variable-access.md)
</dt> <dt>

[Funciones de espera](wait-functions.md)
</dt> </dl>

 

 



