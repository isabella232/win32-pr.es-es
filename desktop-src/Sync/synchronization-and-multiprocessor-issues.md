---
description: Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas multiprocesador debido a suposiciones que son válidas solo en sistemas de un solo procesador.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problemas de sincronización y multiprocesador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105670043"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Problemas de sincronización y multiprocesador

Las aplicaciones pueden encontrar problemas cuando se ejecutan en sistemas multiprocesador debido a suposiciones que son válidas solo en sistemas de un solo procesador.

## <a name="thread-priorities"></a>Prioridades de subprocesos

Considere un programa con dos subprocesos, uno con una prioridad más alta que el otro. En un sistema de un solo procesador, el subproceso de prioridad más alta no liberará el control en el subproceso de prioridad inferior porque el programador da preferencia a los subprocesos de prioridad más alta. En un sistema con varios procesadores, ambos subprocesos se pueden ejecutar simultáneamente, cada uno en su propio procesador.

Las aplicaciones deben sincronizar el acceso a las estructuras de datos para evitar las condiciones de carrera. El código que supone que los subprocesos de prioridad más alta se ejecutan sin interferencias de subprocesos de menor prioridad producirán errores en los sistemas multiprocesador.

## <a name="memory-ordering"></a>Ordenación de memoria

Cuando un procesador escribe en una ubicación de memoria, el valor se almacena en caché para mejorar el rendimiento. Del mismo modo, el procesador intenta satisfacer las solicitudes de lectura de la memoria caché para mejorar el rendimiento. Además, los procesadores comienzan a capturar los valores de la memoria antes de que la aplicación los solicite. Esto puede ocurrir como parte de la ejecución especulativa o debido a problemas de línea de caché.

Las memorias caché de la CPU se pueden particionar en bancos a los que se puede tener acceso en paralelo. Esto significa que las operaciones de memoria se pueden completar de forma desordenada. Para asegurarse de que las operaciones de memoria se completan en orden, la mayoría de los procesadores proporcionan instrucciones de barrera de memoria. Una *barrera de memoria completa* garantiza que las operaciones de lectura y escritura de memoria que aparecen antes de la instrucción de barrera de memoria se confirmen en la memoria antes que las operaciones de lectura y escritura de memoria que aparecen después de la instrucción de barrera de memoria. Una *barrera de memoria de lectura* solo ordena las operaciones de lectura de memoria y una *barrera de memoria de escritura* solo ordena las operaciones de escritura de memoria. Estas instrucciones también aseguran que el compilador deshabilita las optimizaciones que podrían reordenar las operaciones de memoria a través de las barreras.

Los procesadores pueden admitir instrucciones para las barreras de memoria con la semántica de adquisición, liberación y barrera. Esta semántica describe el orden en el que los resultados de una operación están disponibles. Con la semántica de adquisición, los resultados de la operación están disponibles antes de los resultados de cualquier operación que aparece después del código. Con la semántica de versión, los resultados de la operación están disponibles después de los resultados de cualquier operación que aparece antes en el código. La semántica de barrera combina la semántica de adquisición y liberación. Los resultados de una operación con semántica de barrera están disponibles antes de los de cualquier operación que aparece después de él en el código y después de los de cualquier operación que aparece antes.

En los procesadores x86 y x64 que admiten SSE2, las instrucciones son **mfence** (barrera de memoria), **lfence** (barrera de carga) y **sfence** (barrera de tienda). En los procesadores ARM, las inarticulaciones son de **d MB** y **DSB**. Para obtener más información, consulte la documentación del procesador.

Las siguientes funciones de sincronización usan las barreras adecuadas para garantizar el orden de la memoria:

-   Funciones que entran o salen de secciones críticas
-   Funciones que adquieren o liberan bloqueos SRW
-   Inicio y finalización de una sola vez
-   **EnterSynchronizationBarrier** función)
-   Funciones que señalan objetos de sincronización
-   Funciones de espera
-   Funciones entrelazadas (excepto las funciones con el sufijo _nobarrera_ o intrínsecos con el sufijo _\_ NF_ )

## <a name="fixing-a-race-condition"></a>Corregir una condición de carrera

El siguiente código tiene una condición de carrera en sistemas con varios procesadores porque el procesador que se ejecuta `CacheComputedValue` la primera vez puede escribir `fValueHasBeenComputed` en la memoria principal antes de escribir `iValue` en la memoria principal. Por consiguiente, un segundo procesador `FetchComputedValue` que se ejecuta al mismo tiempo `fValueHasBeenComputed` indica que es **true**, pero el nuevo valor de `iValue` todavía está en la memoria caché del primer procesador y no se ha escrito en la memoria.

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

Esta condición de carrera anterior se puede reparar mediante la palabra clave **volatile** o la función [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) para asegurarse de que el valor de `iValue` se actualiza para todos los procesadores antes de que el valor de `fValueHasBeenComputed` esté establecido en **true**.

Al iniciar Visual Studio 2005, si se compila en el modo **/volatile: MS** , el compilador usa la semántica de adquisición para las operaciones de lectura en variables **volátiles** y la semántica de versión para operaciones de escritura en variables **volátiles** (cuando es compatible con la CPU). Por lo tanto, puede corregir el ejemplo de la siguiente manera:

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

Con Visual Studio 2003, se ordenan las referencias **volátiles** a **volatile** ; el compilador no volverá a ordenar el acceso a variables **volátiles** . Sin embargo, estas operaciones se pueden volver a ordenar por el procesador. Por lo tanto, puede corregir el ejemplo de la siguiente manera:

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

[Objetos de sección crítica](critical-section-objects.md)
</dt> <dt>

[Acceso a variables entrelazadas](interlocked-variable-access.md)
</dt> <dt>

[Funciones de espera](wait-functions.md)
</dt> </dl>

 

 



