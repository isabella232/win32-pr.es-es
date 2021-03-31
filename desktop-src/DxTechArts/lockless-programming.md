---
title: Consideraciones de programación sin bloqueo para Xbox 360 y Microsoft Windows
description: En este artículo se proporciona información general sobre algunos de los problemas que se deben tener en cuenta al intentar usar técnicas de programación de bloqueo.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "103995728"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Consideraciones de programación sin bloqueo para Xbox 360 y Microsoft Windows

La programación sin bloqueos es una manera de compartir de forma segura los datos modificados entre varios subprocesos sin el costo de adquirir y liberar bloqueos. Esto suena como una panacea, pero la programación sin bloqueos es compleja e sutil, y a veces no ofrece las ventajas que promete. La programación con bloqueo es especialmente compleja en Xbox 360.

La programación sin bloqueo es una técnica válida para la programación multiproceso, pero no debe usarse con poca. Antes de usarlo, debe comprender las complejidades y debe medir detenidamente para asegurarse de que realmente le ofrezca las ganancias que espera. En muchos casos, hay soluciones más sencillas y rápidas, como el uso compartido de datos con menos frecuencia, que deben usarse en su lugar.

El uso de la programación sin bloqueo correctamente y de forma segura requiere un conocimiento significativo tanto del hardware como del compilador. En este artículo se proporciona información general sobre algunos de los problemas que se deben tener en cuenta al intentar usar técnicas de programación de bloqueo.

## <a name="programming-with-locks"></a>Programar con bloqueos

Al escribir código multiproceso, a menudo es necesario compartir datos entre subprocesos. Si varios subprocesos leen y escriben las estructuras de datos compartidas simultáneamente, pueden producirse daños en la memoria. La forma más sencilla de resolver este problema es usar bloqueos. Por ejemplo, si ManipulateSharedData solo debe ejecutarse en un subproceso cada vez, \_ se puede usar una sección crítica para garantizar esto, como en el código siguiente:

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

Este código es bastante sencillo y sencillo, y es fácil saber que es correcto. Sin embargo, la programación con bloqueos incluye varias desventajas potenciales. Por ejemplo, si dos subprocesos intentan adquirir los mismos dos bloqueos pero los adquieren en un orden diferente, puede obtener un interbloqueo. Si un programa mantiene un bloqueo durante demasiado tiempo, debido a un diseño deficiente o porque el subproceso se ha intercambiado por un subproceso de prioridad más alto, es posible que se bloqueen otros subprocesos durante mucho tiempo. Este riesgo es especialmente importante en Xbox 360 porque el desarrollador asigna un subproceso de hardware a los subprocesos de software, y el sistema operativo no los moverá a otro subproceso de hardware, incluso si uno está inactivo. La consola Xbox 360 tampoco tiene protección contra la inversion de prioridad, en la que un subproceso de prioridad alta gira en un bucle mientras espera a que un subproceso de prioridad baja libere un bloqueo. Por último, si una llamada a procedimiento diferida o una rutina de servicio de interrupción intenta adquirir un bloqueo, puede obtener un interbloqueo.

A pesar de estos problemas, los primitivos de sincronización, como las secciones críticas, suelen ser la mejor manera de coordinar varios subprocesos. Si los primitivos de sincronización son demasiado lentos, la mejor solución suele usarse con menos frecuencia. Sin embargo, para aquellos que pueden permitir la complejidad adicional, otra opción es la programación sin bloqueos.

## <a name="lockless-programming"></a>Programación con bloqueo

La programación sin bloqueos, como sugiere el nombre, es una familia de técnicas para manipular de forma segura los datos compartidos sin utilizar bloqueos. Hay algoritmos de bloqueo disponibles para pasar mensajes, compartir listas y colas de datos, y otras tareas.

Al realizar la programación sin bloqueos, hay dos desafíos que debe abordar: operaciones no atómicas y reordenación.

## <a name="non-atomic-operations"></a>Operaciones no atómicas

Una operación atómica es la que es indivisible, una en la que se garantiza que otros subprocesos nunca verán la operación cuando esté a la mitad. Las operaciones atómicas son importantes para la programación sin bloqueos, porque sin ellos, otros subprocesos podrían ver valores de tipo medio o incoherentes.

En todos los procesadores modernos, puede suponer que las lecturas y escrituras de tipos nativos alineados de forma natural son atómicas. Siempre que el bus de memoria sea al menos tan ancho como el tipo que se lee o se escribe, la CPU Lee y escribe estos tipos en una única transacción de bus, lo que hace imposible que otros subprocesos los vean en un estado de finalización. En las ediciones x86 y x64, no hay ninguna garantía de que las lecturas y escrituras de más de ocho bytes sean atómicas. Esto significa que las lecturas y escrituras de 16 bytes de los registros de la extensión SIMD de streaming (SSE) y las operaciones de cadena podrían no ser atómicas.

No se garantiza que las lecturas y escrituras de tipos que no están alineados de forma natural (por ejemplo, escribiendo DWORDs que cruzan los límites de cuatro bytes) sean atómicos. Es posible que la CPU tenga que realizar estas lecturas y escrituras como transacciones de varios buses, lo que podría permitir que otro subproceso modificara o ver los datos en medio de la lectura o escritura.

Las operaciones compuestas, como la secuencia de lectura, modificación y escritura que se produce cuando se incrementa una variable compartida, no son atómicas. En Xbox 360, estas operaciones se implementan como varias instrucciones (lwz, Addi y STW) y el subproceso se puede intercambiar MSRC durante a través de la secuencia. En x86 y x64, hay una sola instrucción (Inc) que se puede usar para incrementar una variable en la memoria. Si utiliza esta instrucción, el incremento de una variable es atómico en sistemas de un solo procesador, pero todavía no es atómico en sistemas de varios procesadores. Hacer que Inc Atomic en sistemas de varios procesadores basados en x86 y x64 requiera el uso del prefijo de bloqueo, lo que impide que otro procesador realice su propia secuencia de lectura-modificación-escritura entre la lectura y la escritura de la instrucción Inc.

En el código siguiente se muestran algunos ejemplos:

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>Garantizar la atomicidad

Puede asegurarse de que está usando operaciones atómicas mediante una combinación de lo siguiente:

-   Operaciones atómicas naturales
-   Bloqueos para encapsular operaciones compuestas
-   Funciones del sistema operativo que implementan versiones atómicas de las operaciones compuestas populares

El incremento de una variable no es una operación atómica y el incremento puede provocar daños en los datos si se ejecutan en varios subprocesos.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 incluye una familia de funciones que ofrecen versiones atómicas de lectura-modificación-escritura de varias operaciones comunes. Se trata de la familia de funciones InterlockedXxx. Si todas las modificaciones de la variable compartida usan estas funciones, las modificaciones serán seguras para subprocesos.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Reordenación

Un problema más sutil es la reordenación. Las lecturas y escrituras no siempre se producen en el orden en el que se han escrito en el código y esto puede provocar problemas muy confusos. En muchos algoritmos multiproceso, un subproceso escribe algunos datos y, a continuación, escribe en una marca que indica a otros subprocesos que los datos están listos. Esto se conoce como versión de escritura. Si se reordenan las escrituras, otros subprocesos pueden ver que la marca se establece antes de que puedan ver los datos escritos.

Del mismo modo, en muchos casos, un subproceso Lee de una marca y, a continuación, Lee algunos datos compartidos si la marca indica que el subproceso ha adquirido el acceso a los datos compartidos. Esto se conoce como una adquisición de lectura. Si se reordenan las lecturas, se pueden leer los datos desde el almacenamiento compartido antes de la marca y es posible que los valores visibles no estén actualizados.

El compilador y el procesador pueden realizar la reordenación de las lecturas y escrituras. Los compiladores y los procesadores han hecho esta reordenación durante los años, pero en los equipos con un solo procesador se produjo un problema menor. Esto se debe a que la reorganización de lecturas y escrituras de la CPU es invisible en equipos de un solo procesador (para el código de controlador que no es de dispositivo y que no forma parte de un controlador de dispositivo) y es menos probable que la reorganización del compilador de lecturas y escrituras cause problemas en equipos de un solo procesador.

Si el compilador o la CPU reorganiza las escrituras que se muestran en el código siguiente, otro subproceso puede ver que la marca Alive está establecida mientras sigue viendo los valores antiguos para x o y. Se puede producir una reorganización similar al leer.

En este código, un subproceso agrega una nueva entrada a la matriz de Sprite:

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

En el siguiente bloque de código, otro subproceso Lee de la matriz de Sprite:

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Para que este sistema de Sprite sea seguro, necesitamos evitar la reordenación de las lecturas y escrituras de la CPU y del compilador.

### <a name="understanding-cpu-rearrangement-of-writes"></a>Descripción de la reorganización de escrituras de CPU

Algunas CPU reorganizan las escrituras para que sean visibles externamente para otros procesadores o dispositivos en orden no programa. Esta reorganización nunca es visible para el código de un solo subproceso que no sea de controlador, pero puede causar problemas en el código multiproceso.

### <a name="xbox-360"></a>Xbox 360

Aunque la CPU de Xbox 360 no reordena las instrucciones, se reorganizan las operaciones de escritura, que se completan después de las instrucciones. Esta reorganización de escrituras se permite específicamente en el modelo de memoria PowerPC.

Las operaciones de escritura en Xbox 360 no van directamente a la caché L2. En su lugar, para mejorar el ancho de banda de escritura de la caché L2, pasan por las colas de almacenamiento y, a continuación, para almacenar y recopilar búferes. Los búferes de almacenamiento y recopilación permiten escribir bloques de 64 bytes en la memoria caché L2 en una operación. Hay ocho búferes de almacenamiento y recopilación que permiten la escritura eficaz en varias áreas de memoria diferentes.

Los búferes de almacenamiento y recopilación se escriben normalmente en la memoria caché L2 en orden FIFO (el primero en salir es el primero en salir). Sin embargo, si la línea de caché de destino de una escritura no está en la memoria caché L2, esa escritura se puede retrasar mientras se captura la memoria caché de la memoria.

Incluso cuando los búferes de almacenamiento y recopilación se escriben en la memoria caché L2 en orden FIFO estricto, esto no garantiza que las escrituras individuales se escriban en la memoria caché L2 en orden. Por ejemplo, Imagine que la CPU escribe en la ubicación 0x1000, luego en la ubicación 0x2000 y, a continuación, en la ubicación 0x1004. La primera escritura asigna un búfer de almacenamiento y recopilación y lo coloca en la parte delantera de la cola. La segunda escritura asigna otro búfer de almacenamiento-recopilación y lo coloca junto en la cola. La tercera escritura agrega sus datos al primer búfer de almacenamiento y recopilación, que permanece en la parte delantera de la cola. Por lo tanto, la tercera escritura termina en la memoria caché L2 antes de la segunda escritura.

La reordenación provocada por los búferes de almacenamiento y recopilación es fundamentalmente imprevisible, especialmente porque ambos subprocesos de un núcleo comparten los búferes de almacenamiento y recopilación, lo que hace que la asignación y el vaciado de los búferes de recopilación de almacenes sean muy variables.

Este es un ejemplo de cómo se pueden reordenar las escrituras. Puede haber otras posibilidades.

### <a name="x86-and-x64"></a>x86 y x64

Aunque las CPU x86 y x64 reordenan las instrucciones, generalmente no reordenan las operaciones de escritura en relación con otras escrituras. Hay algunas excepciones para la memoria combinada de escritura. Además, las operaciones de cadena (MOVS y STOS) y las escrituras SSE de 16 bytes se pueden reordenar internamente, pero de lo contrario, las escrituras no se reordenan entre sí.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Descripción de la reorganización de lecturas de CPU

Algunas CPU reorganizan las lecturas para que provienen del almacenamiento compartido en orden no programa. Esta reorganización nunca es visible para el código que no es de un solo subproceso, pero puede causar problemas en el código multiproceso.

### <a name="xbox-360"></a>Xbox 360

Los errores de caché pueden provocar que se retrasen algunas lecturas, lo que hace que las lecturas provienen de la memoria compartida fuera de orden, y que la temporización de estos errores de caché no sea predecible fundamentalmente. La captura previa y la predicción de rama también pueden hacer que los datos provienen de la memoria compartida fuera de orden. Estos son solo algunos ejemplos de cómo se pueden reordenar las lecturas. Puede haber otras posibilidades. Esta reorganización de lecturas se permite específicamente en el modelo de memoria PowerPC.

### <a name="x86-and-x64"></a>x86 y x64

Aunque las CPU x86 y x64 reordenan las instrucciones, generalmente no reordenan las operaciones de lectura en relación con otras lecturas. Las operaciones de cadena (MOVS y STOS) y las lecturas SSE de 16 bytes se pueden reordenar internamente, pero de lo contrario, las lecturas no se reordenan entre sí.

### <a name="other-reordering"></a>Otra reordenación

Aunque las CPU x86 y x64 no reordenan las escrituras en relación con otras escrituras, o reordenan las lecturas en relación con otras lecturas, pueden reordenar las lecturas en relación con las escrituras. En concreto, si un programa escribe en una ubicación seguida de leer desde una ubicación diferente, los datos de lectura pueden provienen de la memoria compartida antes de que los datos escritos los realicen allí. Esta reordenación puede interrumpir algunos algoritmos, como los algoritmos de exclusión mutua de Dekker. En el algoritmo de Dekker, cada subproceso establece una marca para indicar que desea entrar en la región crítica y, a continuación, comprueba la marca del otro subproceso para ver si el otro subproceso está en la región crítica o intenta entrar en él. A continuación se muestra el código inicial.

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

El problema es que la lectura de F1 en P0Acquire puede leer desde el almacenamiento compartido antes de que la escritura en F0 lo haga en el almacenamiento compartido. Mientras tanto, la lectura de F0 en P1Acquire puede leer desde el almacenamiento compartido antes de que la escritura en F1 lo haga en el almacenamiento compartido. El efecto neto es que ambos subprocesos establecen sus marcas en TRUE y ambos subprocesos ven la marca del otro subproceso como FALSE, de modo que ambos entran en la región crítica. Por lo tanto, aunque los problemas con la reordenación en sistemas basados en x86 y x64 son menos comunes que en Xbox 360, se pueden seguir produciendo. El algoritmo de Dekker no funcionará sin barreras de memoria de hardware en ninguna de estas plataformas.

las CPU x86 y x64 no volverán a ordenar una escritura antes de una lectura anterior. las CPU x86 y x64 solo reordenan las lecturas por encima de las escrituras anteriores si se dirigen a ubicaciones diferentes.

Las CPU PowerPC pueden reordenar las lecturas con anterioridad a las escrituras y pueden reordenar las escrituras por encima de las lecturas, siempre y cuando estén en direcciones diferentes.

### <a name="reordering-summary"></a>Resumen de reordenación

La CPU de Xbox 360 reordena las operaciones de memoria de forma mucho más agresiva que las CPU x86 y x64, tal y como se muestra en la tabla siguiente. Para obtener más información, consulte la documentación del procesador.



| Reordenación de la actividad           | x86 y x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Lee el avance de las lecturas.   | No          | Sí      |
| Escribe el avance de las escrituras | No          | Sí      |
| La escritura avanza por las lecturas  | No          | Sí      |
| Lee el avance de las escrituras  | Sí         | Sí      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Read-Acquire y barreras de Write-Release

Las construcciones principales usadas para evitar la reordenación de las lecturas y escrituras se denominan barreras de lectura-adquisición y de versión de escritura. Read-acquire es una lectura de una marca u otra variable para obtener la propiedad de un recurso, junto con una barrera contra la reordenación. Del mismo modo, una versión de escritura es una escritura de una marca u otra variable para dar la propiedad de un recurso, junto con una barrera contra la reordenación.

Las definiciones formales, cortesía de hierba Sutter, son:

-   Read-adquire se ejecuta antes de todas las lecturas y escrituras realizadas por el mismo subproceso que la siguen en el orden del programa.
-   Una versión de escritura se ejecuta después de todas las lecturas y escrituras realizadas por el mismo subproceso que la precede en el orden del programa.

Cuando el código adquiere la propiedad de alguna memoria, ya sea mediante la adquisición de un bloqueo o la extracción de un elemento de una lista vinculada compartida (sin un bloqueo), siempre hay una lectura implicada: probar una marca o un puntero para ver si se ha adquirido la propiedad de la memoria. Esta lectura puede formar parte de una operación **InterlockedXxx** , en cuyo caso implica tanto lectura como escritura, pero es la lectura que indica si se ha obtenido la propiedad. Una vez adquirida la propiedad de la memoria, los valores normalmente se leen o se escriben en esa memoria, y es muy importante que estas lecturas y escrituras se ejecuten después de adquirir la propiedad. Una barrera de lectura-adquisición garantiza esto.

Cuando se libera la propiedad de alguna memoria, ya sea liberando un bloqueo o insertando un elemento en una lista de vínculos compartida, siempre hay una escritura implicada que notifica a otros subprocesos que la memoria está disponible. Aunque el código tenía la propiedad de la memoria, es probable que lea o escriba en él, y es muy importante que estas lecturas y escrituras se ejecuten antes de liberar la propiedad. Una barrera de versión de escritura garantiza esto.

Es más fácil pensar en las barreras de la adquisición de lectura y de escritura como operaciones únicas. Sin embargo, a veces tienen que construirse a partir de dos partes: una lectura o una escritura y una barrera que no permite que las lecturas o escrituras se muevan a través de ella. En este caso, la colocación de la barrera es crítica. En el caso de una barrera de lectura-adquisición, la lectura de la marca es la primera, la barrera y, a continuación, Lee y escribe los datos compartidos. En el caso de una barrera de versión de escritura, las lecturas y escrituras de los datos compartidos aparecen en primer lugar, la barrera y, a continuación, la escritura de la marca.

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

La única diferencia entre una lectura y una versión de escritura es la ubicación de la barrera de memoria. Una operación de lectura y adquisición tiene la barrera después de la operación de bloqueo, y una versión de escritura tiene la barrera antes. En ambos casos, la barrera está entre las referencias a la memoria bloqueada y las referencias al bloqueo.

Para comprender por qué se necesitan barreras al adquirir y al liberar datos, es mejor (y más preciso) pensar en estas barreras como garantizar la sincronización con la memoria compartida, no con otros procesadores. Si un procesador usa una versión de escritura para liberar una estructura de datos en la memoria compartida y otro procesador utiliza una lectura y adquisición para obtener acceso a esa estructura de datos desde la memoria compartida, el código funcionará correctamente. Si alguno de los procesadores no utiliza la barrera adecuada, se puede producir un error en el uso compartido de datos.

Es fundamental usar la barrera adecuada para evitar la reordenación del compilador y la CPU para la plataforma.

Una de las ventajas de usar los primitivos de sincronización proporcionados por el sistema operativo es que todos ellos incluyen las barreras de memoria adecuadas.

## <a name="preventing-compiler-reordering"></a>Evitar la reordenación del compilador

El trabajo de un compilador es optimizar agresivamente el código para mejorar el rendimiento. Esto incluye la reorganización de instrucciones siempre que sea útil y donde no cambie el comportamiento. Dado que el estándar de C++ nunca menciona el multithreading, y dado que el compilador no sabe qué código debe ser seguro para subprocesos, el compilador supone que el código es de subproceso único al decidir qué reorganización puede hacer con seguridad. Por lo tanto, debe indicar al compilador que no se le permite reordenar las lecturas y escrituras.

Con Visual C++ puede evitar la reordenación del compilador mediante el uso de la función intrínseca [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)del compilador. Cuando inserte **\_ ReadWriteBarrier** en el código, el compilador no moverá las lecturas y escrituras en él.

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

En el código siguiente, otro subproceso Lee de la matriz de Sprite:

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Es importante entender que [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) no inserta ninguna instrucción adicional y no impide que la CPU reorganice las lecturas y escrituras, solo impide que el compilador las reorganice. Por lo tanto, **\_ ReadWriteBarrier** es suficiente cuando se implementa una barrera de versión de escritura en x86 y x64 (porque x86 y x64 no reordenan las escrituras, y una escritura normal es suficiente para liberar un bloqueo), pero en la mayoría de los demás casos también es necesario impedir que la CPU reordene las lecturas y escrituras.

También puede usar [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) al escribir en memoria combinada de escritura no almacenable en caché para evitar la reordenación de las escrituras. En este caso, **\_ ReadWriteBarrier** ayuda a mejorar el rendimiento, ya que garantiza que las escrituras se producen en el orden lineal preferido del procesador.

También es posible usar las funciones intrínsecas [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) y [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) para un control más preciso de la reordenación del compilador. El compilador no moverá las lecturas a través de un **\_ ReadBarrier** y no moverá las Escrituras a través de un **\_ WriteBarrier**.

## <a name="preventing-cpu-reordering"></a>Impedir la reordenación de la CPU

La reordenación de la CPU es más sutil que la reordenación del compilador. Nunca puede ver que se produce directamente, solo verá errores de inexplicable. Con el fin de evitar la reordenación de la CPU de lecturas y escrituras, es necesario utilizar instrucciones de barrera de memoria en algunos procesadores. El nombre de todos los propósitos de una instrucción de barrera de memoria, en Xbox 360 y en Windows, es [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Esta macro se implementa correctamente para cada plataforma.

En Xbox 360, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se define como **lwsync** (sincronización ligera), también disponible a través de la función intrínseca **\_ \_ lwsync** , que se define en ppcintrinsics. h. **\_ \_ lwsync** también actúa como una barrera de memoria del compilador, lo que impide reorganizar las lecturas y escrituras realizadas por el compilador.

La instrucción **lwsync** es una barrera de memoria en Xbox 360 que sincroniza un núcleo de procesador con la memoria caché L2. Garantiza que todas las escrituras antes de **lwsync** se convierten en la memoria caché L2 antes de cualquier escritura que siga. También garantiza que las lecturas que siguen a **lwsync** no obtienen datos más antiguos de la versión L2 que las lecturas anteriores. El tipo de reordenación que no impide es una lectura por encima de una escritura en una dirección diferente. Por lo tanto, **lwsync** aplica la ordenación de memoria que coincide con la ordenación de memoria predeterminada en procesadores x86 y x64. Para obtener una ordenación de memoria completa, se requiere una instrucción de sincronización más costosa (también conocida como sincronización pesada), pero en la mayoría de los casos no es necesario. En la tabla siguiente se muestran las opciones de reordenación de memoria en Xbox 360.



| Reordenación de Xbox 360           | Sin sincronización | lwsync | sync |
|-------------------------------|---------|--------|------|
| Lee el avance de las lecturas.   | Sí     | No     | No   |
| Escribe el avance de las escrituras | Sí     | No     | No   |
| La escritura avanza por las lecturas  | Sí     | No     | No   |
| Lee el avance de las escrituras  | Sí     | Sí    | No   |



 

PowerPC también tiene las instrucciones de sincronización **iSync** y **eieio** (que se usa para controlar la reordenación de la memoria que impide el almacenamiento en caché). Estas instrucciones de sincronización no deben ser necesarias para fines de sincronización normales.

En Windows, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se define en Winnt. h y proporciona una instrucción de barrera de memoria diferente en función de si se está compilando para x86 o x64. La instrucción de barrera de memoria actúa como una barrera completa, lo que impide que se reordene las lecturas y escrituras a través de la barrera. Por lo tanto, **MemoryBarrier** en Windows proporciona una garantía de reordenación más fuerte que en la Xbox 360.

En la consola Xbox 360 y en muchas otras CPU, existe una manera adicional de evitar la reordenación de lectura por la CPU. Si lee un puntero y, a continuación, usa ese puntero para cargar otros datos, la CPU garantiza que las lecturas fuera del puntero no sean anteriores a la lectura del puntero. Si la marca de bloqueo es un puntero y todas las lecturas de datos compartidos están fuera del puntero, se puede omitir el [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) , lo que supone un ahorro de rendimiento modesto.

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

La instrucción [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) solo evita la reordenación de las lecturas y escrituras en la memoria caché. Si asigna memoria como PAGE \_ nocache o Page \_ WRITECOMBINE, una técnica común para los autores de controladores de dispositivos y para los desarrolladores de juegos en Xbox 360, **MemoryBarrier** no tiene ningún efecto en los accesos a esta memoria. La mayoría de los desarrolladores no necesitan la sincronización de memoria no almacenable en caché. Eso va más allá del ámbito de este artículo.

## <a name="interlocked-functions-and-cpu-reordering"></a>Funciones de bloqueo y reordenación de CPU

A veces, la lectura o escritura que adquiere o libera un recurso se realiza mediante una de las funciones de **InterlockedXxx** . En Windows, esto simplifica las cosas; Dado que en Windows, las funciones de **InterlockedXxx** son todas las barreras de memoria completa. En realidad, tienen una barrera de memoria de CPU antes y después de ellas, lo que significa que son una barrera completa de lectura/adquisición o de versión de escritura.

En Xbox 360, las funciones de **InterlockedXxx** no contienen barreras de memoria de la CPU. Impiden la reordenación del compilador de lecturas y escrituras, pero no de la reordenación de la CPU. Por lo tanto, en la mayoría de los casos, al usar las funciones de **InterlockedXxx** en Xbox 360, debe preceder o seguirlos con un **\_ \_ lwsync** para convertirlos en una barrera de lectura/adquisición o de versión de escritura. Para mayor comodidad y para facilitar la lectura, hay versiones de **adquisición** y **lanzamiento** de muchas de las funciones de **InterlockedXxx** . Esto incluye una barrera de memoria integrada. Por ejemplo, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) realiza un incremento entrelazado seguido de una barrera de memoria **\_ \_ lwsync** para proporcionar la funcionalidad completa de lectura y adquisición.

Se recomienda usar las versiones de **adquisición** y **lanzamiento** de las funciones de **InterlockedXxx** (la mayoría de las cuales están disponibles también en Windows, sin penalización de rendimiento) para que su intención sea más obvia y para que sea más fácil obtener las instrucciones de barrera de memoria en el lugar correcto. Cualquier uso de **InterlockedXxx** en Xbox 360 sin una barrera de memoria debe examinarse con cuidado, ya que a menudo se trata de un error.

Este ejemplo muestra cómo un subproceso puede pasar tareas u otros datos a otro subproceso mediante las versiones de **adquisición** y **lanzamiento** de las funciones de **InterlockedXxxSList** . Las funciones de **InterlockedXxxSList** son una familia de funciones para mantener una lista compartida de un solo vínculo sin un bloqueo. Tenga en cuenta que las variantes de **adquisición** y **liberación** de estas funciones no están disponibles en Windows, pero las versiones normales de estas funciones son una barrera de memoria completa en Windows.

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Variables volátiles y reordenación

El estándar de C++ indica que no se pueden almacenar en caché las lecturas de variables volátiles, no se pueden retrasar las escrituras volátiles y las lecturas y escrituras volátiles no se pueden moverse más allá de otras. Esto es suficiente para comunicarse con dispositivos de hardware, que es el propósito de la palabra clave volatile en el estándar de C++.

Sin embargo, las garantías del estándar no son suficientes para usar volatile para multithreading. El estándar de C++ no impide que el compilador reordene las lecturas y escrituras no volátiles con respecto a las lecturas y escrituras volátiles, y no indica nada sobre cómo evitar la reordenación de la CPU.

Visual C++ 2005 va más allá del estándar de C++ para definir la semántica compatible con varios subprocesos para el acceso de variables volátiles. A partir de Visual C++ 2005, las lecturas de variables volátiles se definen para tener semántica de adquisición y de lectura, y las escrituras en variables volátiles se definen para tener la semántica de versión de escritura. Esto significa que el compilador no reorganizará las lecturas y escrituras más allá y, en Windows, se asegurará de que la CPU no lo hace.

Es importante comprender que estas nuevas garantías solo se aplican a Visual C++ 2005 y versiones futuras de Visual C++. Los compiladores de otros proveedores generalmente implementarán semánticas diferentes, sin las garantías adicionales de Visual C++ 2005. Además, en Xbox 360, el compilador no inserta instrucciones para impedir que la CPU reordene las lecturas y escrituras.

## <a name="example-of-a-lock-free-data-pipe"></a>Ejemplo de una canalización de datos Lock-Free

Una canalización es una construcción que permite a uno o más subprocesos escribir datos que otros subprocesos leen. Una versión sin bloqueo de una canalización puede ser una forma elegante y eficaz de pasar el trabajo del subproceso al subproceso. El SDK de DirectX proporciona **LockFreePipe**, una canalización de un solo lector y un bloqueo de un solo escritor que está disponible en DXUTLockFreePipe. h. El mismo **LockFreePipe** está disponible en el SDK de Xbox 360 en AtgLockFreePipe. h.

**LockFreePipe** se puede usar cuando dos subprocesos tienen una relación productor/consumidor. El subproceso de productor puede escribir datos en la canalización para que el subproceso del consumidor los procese en una fecha posterior, sin ningún bloqueo. Si la canalización se llena, se producirá un error en las escrituras y el subproceso del productor tendrá que intentarlo de nuevo más tarde, pero esto solo ocurrirá si el subproceso del productor está por adelante. Si la canalización está vacía, se produce un error de lectura y el subproceso del consumidor tendrá que intentarlo de nuevo más tarde, pero esto solo ocurrirá si no hay ningún trabajo para que lo haga el subproceso del consumidor. Si los dos subprocesos están bien equilibrados y la canalización es lo suficientemente grande, la canalización les permite pasar datos sin problemas, además de retrasos o bloques.

## <a name="xbox-360-performance"></a>Rendimiento de Xbox 360

El rendimiento de las instrucciones de sincronización y de las funciones de Xbox 360 variará en función del código que se esté ejecutando. La adquisición de bloqueos tardará mucho más si otro subproceso posee actualmente el bloqueo. Las operaciones de [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) y sección crítica tardarán mucho más si otros subprocesos escriben en la misma línea de caché. El contenido de las colas de almacén también puede afectar al rendimiento. Por lo tanto, todos estos números son solo aproximaciones, generadas a partir de pruebas muy simples:

-   **lwsync** se midió con 33-48 ciclos.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) se midió con 225-260 ciclos.
-   La adquisición o liberación de una sección crítica se midió como la realización de unos 345 ciclos.
-   La adquisición o liberación de una exclusión mutua se midió como una toma de 2350 ciclos.

## <a name="windows-performance"></a>Rendimiento de Windows

El rendimiento de las instrucciones y las funciones de sincronización en Windows varía considerablemente según el tipo y la configuración del procesador, y en qué otro código se está ejecutando. Los sistemas de varios núcleos y varios Sockets suelen tardar más en ejecutar instrucciones de sincronización y la adquisición de bloqueos tarda mucho más tiempo si otro subproceso posee actualmente el bloqueo.

Sin embargo, incluso algunas mediciones generadas a partir de pruebas muy simples son útiles:

-   [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se midió con 20-90 ciclos.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) se midió con 36-90 ciclos.
-   La adquisición o liberación de una sección crítica se midió como una toma de 40-100 ciclos.
-   La adquisición o liberación de una exclusión mutua se midió como una toma de 750-2500 ciclos.

Estas pruebas se realizaron en Windows XP en una variedad de procesadores diferentes. Las horas cortas se encontraban en un equipo con un solo procesador y los tiempos más largos en un equipo con varios procesadores.

Aunque la adquisición y liberación de bloqueos es más costosa que el uso de la programación sin bloqueo, es aún mejor compartir datos con menos frecuencia, evitando así el costo por completo.

## <a name="performance-thoughts"></a>Consideraciones sobre el rendimiento

La adquisición o liberación de una sección crítica consiste en una barrera de memoria, una operación **InterlockedXxx** y alguna comprobación adicional para controlar la recursividad y revertir a una exclusión mutua, si es necesario. Debe tener cuidado al implementar su propia sección crítica, ya que el giro de un bucle en espera de que un bloqueo sea gratuito, sin recurrir a una exclusión mutua, puede desperdiciar un rendimiento considerable. En el caso de las secciones críticas que están muy dispones pero que no se conservan durante mucho tiempo, debería considerar el uso de [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) para que el sistema operativo gire durante mientras espera a que la sección crítica esté disponible en lugar de aplazarse inmediatamente a una exclusión mutua si la sección crítica es propiedad cuando intenta adquirirla. Con el fin de identificar las secciones críticas que pueden beneficiarse de un número de bucles, es necesario medir la longitud de la espera típica para un bloqueo determinado.

Si se utiliza un montón compartido para las asignaciones de memoria (el comportamiento predeterminado), cada asignación de memoria y Free implica la adquisición de un bloqueo. A medida que aumenta el número de subprocesos y el número de asignaciones, los niveles de rendimiento se desactivan y finalmente se inicia su disminución. El uso de montones por subproceso o la reducción del número de asignaciones puede evitar este cuello de botella de bloqueo.

Si un subproceso está generando datos y otro subproceso está consumiendo datos, pueden acabar compartiendo datos con frecuencia. Esto puede ocurrir si un subproceso está cargando recursos y otro subproceso está representando la escena. Si el subproceso de representación hace referencia a los datos compartidos en cada llamada a Draw, la sobrecarga de bloqueo será alta. Se puede obtener un rendimiento mucho mejor si cada subproceso tiene estructuras de datos privadas que después se sincronizan una vez por fotograma o menos.

No se garantiza que los algoritmos sin bloqueo sean más rápidos que los algoritmos que usan bloqueos. Debe comprobar si los bloqueos están causando realmente problemas antes de intentar evitarlos y debe medir para ver si el código sin bloqueo realmente mejora el rendimiento.

## <a name="platform-differences-summary"></a>Resumen de diferencias de plataforma

-   Las funciones de **InterlockedXxx** evitan la reordenación de lectura/escritura de la CPU en Windows, pero no en Xbox 360.
-   La lectura y escritura de variables volátiles con Visual Studio C++ 2005 impide la reordenación de lectura/escritura de la CPU en Windows, pero en Xbox 360 solo impide la reordenación de lectura/escritura del compilador.
-   Las escrituras se reordenan en la consola Xbox 360, pero no en x86 o x64.
-   Las lecturas se reordenan en la consola Xbox 360, pero en x86 o x64 solo se reordenan en relación con las escrituras y solo si las lecturas y escrituras se dirigen a ubicaciones diferentes.

## <a name="recommendations"></a>Recomendaciones

-   Use bloqueos cuando sea posible porque son más fáciles de usar correctamente.
-   Evite el bloqueo con demasiada frecuencia, de modo que los costos de bloqueo no sean significativos.
-   Evite mantener bloqueos durante demasiado tiempo, con el fin de evitar paradas largas.
-   Use la programación sin bloqueo cuando corresponda, pero asegúrese de que las ventajas justifiquen la complejidad.
-   Use la programación sin bloqueo o los bloqueos de giro en situaciones en las que se prohíben otros bloqueos, como cuando se comparten datos entre llamadas a procedimiento diferidas y código normal.
-   Use únicamente algoritmos de programación estándar de bloqueo que se hayan demostrado que son correctos.
-   Al realizar la programación con bloqueo, asegúrese de usar variables de marca volátil y instrucciones de barrera de memoria según sea necesario.
-   Al usar **InterlockedXxx** en Xbox 360, use las variantes de **adquisición** y **liberación** .

## <a name="references"></a>Referencias

-   Biblioteca de MSDN. "[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)". Referencia del lenguaje C++.
-   Saavedra Morrison. "[Comprenda el impacto de las técnicas de Low-Lock en aplicaciones multiproceso](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)". MSDN Magazine, 2005 de octubre.
-   Lyons, Michael. "[Modelo de almacenamiento PowerPC y programación de Aix](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)". IBM developerWorks, 16 de noviembre de 2005.
-   McKenney, Paul E. "[ordenación de memoria en microprocesadores modernos, parte II](https://www.linuxjournal.com/article/8212)". Diario de Linux, septiembre de 2005. \[Este artículo contiene algunos detalles de x86.\]
-   Intel Corporation. "[Clasificación de memoria de la arquitectura de Intel® 64](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)". 2007 de agosto. \[Se aplica a los procesadores IA-32 e Intel 64.\]
-   Niebler, Eric. "[Informe de viajes: reunión ad hoc en subprocesos en C++](https://www.artima.com/cppsource/threads_meeting.html)". Código fuente de C++, 17 de octubre de 2006.
-   Hart, Thomas E. 2006. "[Sincronización rápida de bloqueos: implicaciones de rendimiento de la recuperación de memoria](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)". Procedimientos del Symposium de procesamiento distribuido y paralelo 2006 Internacional (IPDPS 2006), Isla Rhodes, Grecia, abril de 2006.

 

 