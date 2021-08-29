---
title: Consideraciones de programación sin bloqueo para Xbox 360 y Microsoft Windows
description: En este artículo se proporciona información general sobre algunos de los problemas que se deben tener en cuenta al intentar usar técnicas de programación sin bloqueo.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ad19fa15d9f0dc2671e77c7fb2408c96362420ddd70d6e6ad7795ba5b5f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042565"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Consideraciones de programación sin bloqueo para Xbox 360 y Microsoft Windows

La programación sin bloqueo es una manera segura de compartir datos cambiantes entre varios subprocesos sin el costo de adquirir y liberar bloqueos. Esto suena como un proceso, pero la programación sin bloqueo es compleja y sutil, y a veces no ofrece las ventajas que ofrece. La programación sin bloqueo es especialmente compleja en Xbox 360.

La programación sin bloqueo es una técnica válida para la programación multiproceso, pero no debe usarse a la ligera. Antes de usarlo, debe comprender las complejidades y debe medir detenidamente para asegurarse de que realmente le está dando las ganancias que espera. En muchos casos, hay soluciones más sencillas y rápidas, como compartir datos con menos frecuencia, que se deben usar en su lugar.

El uso correcto y seguro de la programación sin bloqueo requiere un conocimiento significativo del hardware y del compilador. En este artículo se proporciona información general sobre algunos de los problemas que se deben tener en cuenta al intentar usar técnicas de programación sin bloqueo.

## <a name="programming-with-locks"></a>Programación con bloqueos

Al escribir código multiproceso, a menudo es necesario compartir datos entre subprocesos. Si varios subprocesos leen y escriben simultáneamente las estructuras de datos compartidos, pueden producirse daños en la memoria. La manera más sencilla de resolver este problema es usar bloqueos. Por ejemplo, si ManipulateSharedData solo debe ejecutarse por un subproceso a la vez, se puede usar una SECCIÓN CRÍTICA para garantizar esto, como en \_ el código siguiente:

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

Este código es bastante sencillo y sencillo, y es fácil saber que es correcto. Sin embargo, la programación con bloqueos presenta varias desventajas potenciales. Por ejemplo, si dos subprocesos intentan adquirir los mismos dos bloqueos pero los adquieren en un orden diferente, es posible que obtenga un interbloqueo. Si un programa mantiene un bloqueo durante demasiado tiempo (debido a un diseño deficiente o porque un subproceso de prioridad más alta ha intercambiado el subproceso), es posible que otros subprocesos se bloqueen durante mucho tiempo. Este riesgo es especialmente grande en Xbox 360 porque el desarrollador asigna un subproceso de hardware a los subprocesos de software y el sistema operativo no los moverá a otro subproceso de hardware, incluso si uno está inactivo. El Xbox 360 no tiene protección contra la inversión de prioridad, donde un subproceso de alta prioridad gira en un bucle mientras espera a que un subproceso de prioridad baja libere un bloqueo. Por último, si una llamada a procedimiento diferido o una rutina de servicio de interrupción intenta adquirir un bloqueo, es posible que reciba un interbloqueo.

A pesar de estos problemas, las primitivas de sincronización, como las secciones críticas, suelen ser la mejor manera de coordinar varios subprocesos. Si las primitivas de sincronización son demasiado lentas, la mejor solución suele ser usarlas con menos frecuencia. Sin embargo, para aquellos que pueden permitirse la complejidad adicional, otra opción es la programación sin bloqueo.

## <a name="lockless-programming"></a>Programación sin bloqueo

La programación sin bloqueo, como sugiere el nombre, es una familia de técnicas para manipular de forma segura los datos compartidos sin usar bloqueos. Hay algoritmos sin bloqueo disponibles para pasar mensajes, compartir listas y colas de datos y otras tareas.

Al realizar la programación sin bloqueos, hay dos desafíos que debe abordar: operaciones no atómicas y reordenación.

## <a name="non-atomic-operations"></a>Operaciones no atómicas

Una operación atómica es aquella que es indivisible, una en la que se garantiza que otros subprocesos nunca verán la operación cuando se realiza a la mitad. Las operaciones atómicas son importantes para la programación sin bloqueo, porque sin ellas, otros subprocesos podrían ver valores escritos a medias o un estado incoherente.

En todos los procesadores modernos, puede suponer que las lecturas y escrituras de tipos nativos alineados de forma natural son atómicas. Siempre que el bus de memoria sea al menos tan ancho como el tipo que se está leyendo o escribiendo, la CPU lee y escribe estos tipos en una única transacción de bus, lo que hace imposible que otros subprocesos los vean en un estado medio completado. En x86 y x64, no hay ninguna garantía de que las lecturas y escrituras de más de ocho bytes sean atómicas. Esto significa que es posible que las lecturas y escrituras de 16 bytes de registros de extensión SIMD de streaming (SSE) y operaciones de cadena no sean atómicas.

No se garantiza que las lecturas y escrituras de tipos que no están alineados de forma natural (por ejemplo, la escritura de DWORD que cruzan límites de cuatro bytes) no sean atómicas. Es posible que la CPU tenga que realizar estas lecturas y escrituras como varias transacciones de bus, lo que podría permitir que otro subproceso modifique o vea los datos en medio de la lectura o escritura.

Las operaciones compuestas, como la secuencia de lectura,modificación y escritura que se produce al incrementar una variable compartida, no son atómicas. En Xbox 360, estas operaciones se implementan como varias instrucciones (lwz, addi y stw), y el subproceso se podría intercambiar de forma parcial a través de la secuencia. En x86 y x64, hay una sola instrucción (inc) que se puede usar para incrementar una variable en memoria. Si usa esta instrucción, el incremento de una variable es atómico en sistemas de un solo procesador, pero sigue sin ser atómico en sistemas de varios procesadores. La realización de inc atomic en sistemas de varios procesadores basados en x86 y x64 requiere el uso del prefijo de bloqueo, lo que impide que otro procesador haga su propia secuencia de lectura-modificación y escritura entre la lectura y la escritura de la instrucción inc.

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

## <a name="guaranteeing-atomicity"></a>Garantía de atomicidad

Puede estar seguro de que usa operaciones atómicas mediante una combinación de lo siguiente:

-   Operaciones atómicas naturales
-   Bloqueos para encapsular operaciones compuestas
-   Funciones del sistema operativo que implementan versiones atómicas de operaciones compuestas populares

El incremento de una variable no es una operación atómica y el incremento puede provocar daños en los datos si se ejecuta en varios subprocesos.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 incluye una familia de funciones que ofrecen versiones atómicas de lectura, modificación y escritura de varias operaciones comunes. Se trata de la familia de funciones InterlockedXxx. Si todas las modificaciones de la variable compartida usan estas funciones, las modificaciones serán seguras para subprocesos.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Reordenamiento

Un problema más sutil es la reordenación. Las lecturas y escrituras no siempre se hacen en el orden en que las ha escrito en el código, lo que puede dar lugar a problemas muy confusos. En muchos algoritmos multiproceso, un subproceso escribe algunos datos y, a continuación, escribe en una marca que indica a otros subprocesos que los datos están listos. Esto se conoce como versión de escritura. Si se reordena la escritura, es posible que otros subprocesos vean que la marca está establecida antes de que puedan ver los datos escritos.

De forma similar, en muchos casos, un subproceso lee desde una marca y, a continuación, lee algunos datos compartidos si la marca indica que el subproceso ha adquirido acceso a los datos compartidos. Esto se conoce como lectura y adquisición. Si se reordena la lectura, los datos se pueden leer desde el almacenamiento compartido antes de la marca y es posible que los valores vistos no estén actualizados.

El compilador y el procesador pueden reordenar las lecturas y escrituras. Los compiladores y procesadores han realizado esta reordenación durante años, pero en las máquinas de procesador único no se ha tenido un problema. Esto se debe a que la reorganización de la CPU de lecturas y escrituras es invisible en máquinas de un solo procesador (para el código de controlador que no es parte de un controlador de dispositivo) y la reorganización del compilador de lecturas y escrituras es menos probable que cause problemas en las máquinas de un solo procesador.

Si el compilador o la CPU reorganizan las escrituras que se muestran en el código siguiente, es posible que otro subproceso vea que la marca activo está establecida mientras sigue viendo los valores antiguos de x o y. Puede producirse una reorganización similar al leer.

En este código, un subproceso agrega una nueva entrada a la matriz sprite:

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

En este siguiente bloque de código, otro subproceso lee de la matriz sprite:

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

Para que este sistema sprite sea seguro, es necesario evitar la reordenación del compilador y la CPU de lecturas y escrituras.

### <a name="understanding-cpu-rearrangement-of-writes"></a>Descripción de la reorganización de la CPU de escrituras

Algunas CPU reorganizan las escrituras para que sean visibles externamente para otros procesadores o dispositivos en orden no program. Esta reorganización nunca es visible para el código que no es de un solo subproceso, pero puede causar problemas en el código multiproceso.

### <a name="xbox-360"></a>Xbox 360

Aunque el Xbox 360 CPU no reordena las instrucciones, reorganiza las operaciones de escritura, que se completan después de las propias instrucciones. Esta reorganización de escrituras está permitida específicamente por el modelo PowerPC memoria.

Las escrituras Xbox 360 no van directamente a la caché L2. En su lugar, para mejorar el ancho de banda de escritura de caché L2, pasan por las colas del almacén y, a continuación, a los búferes de almacenamiento y recopilación. Los búferes de almacenamiento y recopilación permiten escribir bloques de 64 bytes en la memoria caché L2 en una sola operación. Hay ocho búferes de almacenamiento y recopilación, que permiten escribir de forma eficaz en varias áreas diferentes de memoria.

Normalmente, los búferes de almacenamiento-recopilación se escriben en la memoria caché L2 en orden de primero en salir (FIFO). Sin embargo, si la línea de caché de destino de una escritura no está en la caché L2, esa escritura puede retrasarse mientras la línea de caché se captura de la memoria.

Incluso cuando los búferes de recopilación de almacén se escriben en la caché L2 en orden FIFO estricto, esto no garantiza que las escrituras individuales se escriban en la caché L2 en orden. Por ejemplo, imagine que la CPU escribe en la ubicación 0x1000, después en la ubicación 0x2000 y, a continuación, en la ubicación 0x1004. La primera escritura asigna un búfer de recopilación de almacén y lo coloca al principio de la cola. La segunda escritura asigna otro búfer de recopilación de almacén y lo coloca a continuación en la cola. La tercera escritura agrega sus datos al primer búfer de almacenamiento y recopilación, que permanece al principio de la cola. Por lo tanto, la tercera escritura termina yendo a la caché L2 antes de la segunda escritura.

La reordenación causada por los búferes de recopilación de almacén es fundamentalmente imprevisible, especialmente porque ambos subprocesos de un núcleo comparten los búferes de recopilación de almacén, lo que hace que la asignación y el vaciado de los búferes de recopilación de almacén sea muy variable.

Este es un ejemplo de cómo se pueden reordenar las escrituras. Puede haber otras posibilidades.

### <a name="x86-and-x64"></a>x86 y x64

Aunque las CPU x86 y x64 reordenan las instrucciones, por lo general no reordenan las operaciones de escritura con respecto a otras escrituras. Hay algunas excepciones para la memoria combinada de escritura. Además, las operaciones de cadena (MOVS y STOS) y las escrituras SSE de 16 bytes se pueden reordenar internamente, pero de lo contrario, las escrituras no se reordenan entre sí.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Descripción de la reorganización de la CPU de lecturas

Algunas CPU reorganizan las lecturas para que proceden de forma eficaz del almacenamiento compartido en orden no program. Esta reorganización nunca es visible para el código de un solo subproceso que no es de controlador, pero puede causar problemas en el código multiproceso.

### <a name="xbox-360"></a>Xbox 360

Los problemas de caché pueden provocar que algunas lecturas se retrasen, lo que hace que las lecturas proceden de memoria compartida fuera de servicio, y el tiempo de estos problemas de caché es fundamentalmente imprevisible. La captura previa y la predicción de ramas también pueden hacer que los datos proceden de memoria compartida fuera de orden. Estos son solo algunos ejemplos de cómo se pueden reordenar las lecturas. Puede haber otras posibilidades. Esta reorganización de lecturas está permitida específicamente por el modelo PowerPC memoria.

### <a name="x86-and-x64"></a>x86 y x64

Aunque las CPU x86 y x64 reordenan las instrucciones, generalmente no reordenan las operaciones de lectura con respecto a otras lecturas. Las operaciones de cadena (MOVS y STOS) y las lecturas de SSE de 16 bytes se pueden reordenar internamente, pero de lo contrario, las lecturas no se reordenan entre sí.

### <a name="other-reordering"></a>Otra reordenación

Aunque las CPU x86 y x64 no reordenan las escrituras con respecto a otras escrituras o reordenan las lecturas con respecto a otras lecturas, pueden reordenar las lecturas en relación con las escrituras. En concreto, si un programa escribe en una ubicación seguida de la lectura desde otra ubicación, los datos leídos pueden proceder de la memoria compartida antes de que los datos escritos lo haga allí. Esta reordenación puede interrumpir algunos algoritmos, como los algoritmos de exclusión mutua de Dekker. En el algoritmo de Dekker, cada subproceso establece una marca para indicar que desea entrar en la región crítica y, a continuación, comprueba la marca del otro subproceso para ver si el otro subproceso está en la región crítica o intentando escribirlo. A continuación se muestra el código inicial.

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

El problema es que la lectura de f1 en P0Acquire puede leer desde el almacenamiento compartido antes de que la escritura en f0 lo haga en el almacenamiento compartido. Mientras tanto, la lectura de f0 en P1Acquire puede leer desde el almacenamiento compartido antes de que la escritura en f1 lo haga en el almacenamiento compartido. El efecto neto es que ambos subprocesos establecen sus marcas en TRUE y ambos subprocesos ven la marca del otro subproceso como FALSE, por lo que ambos entran en la región crítica. Por lo tanto, aunque los problemas con la reordenación en sistemas basados en x86 y x64 son menos comunes que en Xbox 360, pueden seguir ocurriendo. El algoritmo de Dekker no funcionará sin barreras de memoria de hardware en ninguna de estas plataformas.

Las CPU x86 y x64 no reordenarán una escritura antes de una lectura anterior. Las CPU x86 y x64 solo reordenan las lecturas antes de las escrituras anteriores si tienen como destino ubicaciones diferentes.

PowerPC Las CPU pueden reordenar las lecturas antes de las escrituras y pueden reordenar las escrituras antes de las lecturas, siempre que estén en direcciones diferentes.

### <a name="reordering-summary"></a>Resumen de reordenación

La Xbox 360 CPU reordena las operaciones de memoria de forma mucho más agresiva que las CPU x86 y x64, como se muestra en la tabla siguiente. Para más información, consulte la documentación del procesador.



| Actividad de reordenación           | x86 y x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Lecturas que avanzan por delante de las lecturas   | No          | Sí      |
| Escrituras que avanzan por delante de las escrituras | No          | Sí      |
| Escrituras que avanzan por delante de las lecturas  | No          | Sí      |
| Lecturas que avanzan en las escrituras  | Sí         | Sí      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Read-Acquire y Write-Release barreras

Las construcciones principales que se usan para evitar la reordenación de lecturas y escrituras se denominan barreras de lectura-adquisición y de versión de escritura. Una adquisición de lectura es una lectura de una marca u otra variable para obtener la propiedad de un recurso, junto con una barrera contra la reordenación. De forma similar, una versión de escritura es una escritura de una marca u otra variable para entregar la propiedad de un recurso, junto con una barrera contra la reordenación.

Las definiciones formales, por cortesía de Sutter, son:

-   Una adquisición de lectura se ejecuta antes de todas las lecturas y escrituras realizadas por el mismo subproceso que lo sigue en el orden del programa.
-   Una versión de escritura se ejecuta después de todas las lecturas y escrituras realizadas por el mismo subproceso que lo precede en el orden del programa.

Cuando el código adquiere la propiedad de parte de la memoria, ya sea mediante la adquisición de un bloqueo o mediante la extracción de un elemento de una lista vinculada compartida (sin bloqueo), siempre hay una lectura implicada, probar una marca o un puntero para ver si se ha adquirido la propiedad de la memoria. Esta lectura puede formar parte de una operación **InterlockedXxx,** en cuyo caso implica una lectura y una escritura, pero es la lectura la que indica si se ha adquirido la propiedad. Una vez adquirida la propiedad de la memoria, los valores normalmente se leen o se escriben en esa memoria, y es muy importante que estas lecturas y escrituras se ejecuten después de adquirir la propiedad. Una barrera de adquisición de lectura lo garantiza.

Cuando se libera la propiedad de parte de la memoria, ya sea mediante la liberación de un bloqueo o al insertar un elemento en una lista vinculada compartida, siempre hay una escritura implicada que notifica a otros subprocesos que la memoria ahora está disponible para ellos. Aunque el código tenía la propiedad de la memoria, probablemente leyó o escribió en ella, y es muy importante que estas lecturas y escrituras se ejecuten antes de liberar la propiedad. Una barrera de versión de escritura lo garantiza.

Es más sencillo pensar en las barreras de lectura-adquisición y de versión de escritura como operaciones únicas. Sin embargo, a veces tienen que construirse a partir de dos partes: una lectura o escritura y una barrera que no permite que las lecturas o escrituras se muevan por ella. En este caso, la colocación de la barrera es fundamental. En el caso de una barrera de lectura y adquisición, la lectura de la marca se produce primero, después la barrera y, después, las lecturas y escrituras de los datos compartidos. Para una barrera de versión de escritura, las lecturas y escrituras de los datos compartidos proceden primero, después la barrera y, después, la escritura de la marca.

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

La única diferencia entre una adquisición de lectura y una versión de escritura es la ubicación de la barrera de memoria. Una adquisición de lectura tiene la barrera después de la operación de bloqueo y una versión de escritura tiene la barrera antes. En ambos casos, la barrera está entre las referencias a la memoria bloqueada y las referencias al bloqueo.

Para comprender por qué se necesitan barreras tanto al adquirir como al liberar datos, es mejor (y más preciso) pensar en estas barreras como garantía de sincronización con memoria compartida, no con otros procesadores. Si un procesador usa una versión de escritura para liberar una estructura de datos en la memoria compartida y otro utiliza una adquisición de lectura para obtener acceso a esa estructura de datos desde la memoria compartida, el código funcionará correctamente. Si alguno de los procesadores no usa la barrera adecuada, puede producirse un error en el uso compartido de datos.

El uso de la barrera adecuada para evitar la reordenación del compilador y la CPU para la plataforma es fundamental.

Una de las ventajas de usar las primitivas de sincronización proporcionadas por el sistema operativo es que todas incluyen las barreras de memoria adecuadas.

## <a name="preventing-compiler-reordering"></a>Impedir la reordenación del compilador

El trabajo de un compilador es optimizar el código de forma agresiva para mejorar el rendimiento. Esto incluye reorganizar las instrucciones siempre que sea útil y donde no cambie el comportamiento. Dado que el estándar de C++ nunca menciona el multithreading y porque el compilador no sabe qué código debe ser seguro para subprocesos, el compilador asume que el código es de un solo subproceso al decidir qué reorganizaciones puede hacer de forma segura. Por lo tanto, debe decir al compilador cuándo no se permite reordenar las lecturas y escrituras.

Con Visual C++ puede evitar la reordenación del compilador mediante el uso del intrínseco del compilador [**\_ ReadWriteBarrite**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx). Cuando inserte **\_ ReadWriteBarrite en** el código, el compilador no moverá las lecturas y escrituras a través de él.

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

En el código siguiente, otro subproceso lee de la matriz sprite:

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

Es importante comprender que [**\_ ReadWriteBarrite no**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) inserta ninguna instrucción adicional y no impide que la CPU reordene las lecturas y escrituras, sino que solo impide que el compilador las reordene. Por lo tanto, **\_ ReadWriteBarrite** es suficiente cuando se implementa una barrera de versión de escritura en x86 y x64 (porque x86 y x64 no reordena las escrituras y una escritura normal es suficiente para liberar un bloqueo), pero en la mayoría de los demás casos, también es necesario evitar que la CPU reordene las lecturas y escrituras.

También puede usar [**\_ ReadWriteBarrite al**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) escribir en memoria combinada de escritura no almacenable en caché para evitar la reordenación de escrituras. En este **\_ caso, ReadWriteBarhz** ayuda a mejorar el rendimiento, ya que garantiza que las escrituras se realizarán en el orden lineal preferido del procesador.

También es posible usar los intrínsecos [**\_ ReadBarrín**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) y [**\_ WriteBarrín**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) para un control más preciso de la reordenación del compilador. El compilador no moverá las lecturas a través de **\_ readBarmoverse** y no moverá las escrituras a través de **\_ writeBarmoverse.**

## <a name="preventing-cpu-reordering"></a>Impedir la reordenación de CPU

La reordenación de CPU es más sutil que la reordenación del compilador. Nunca se puede ver que sucede directamente, simplemente se ven errores inexplicables. Para evitar la reordenación de la CPU de lecturas y escrituras, debe usar instrucciones de barrera de memoria en algunos procesadores. El nombre de uso completo de una instrucción de barrera de memoria, en Xbox 360 y en Windows, [**es MemoryBartruc**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Esta macro se implementa correctamente para cada plataforma.

En Xbox 360, [**MemoryBardex**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se define como **lwsync** (sincronización ligera), también disponible a través del intrínseco **\_ \_ lwsync,** que se define en ppcintrinsics.h. **\_ \_ lwsync también** actúa como una barrera de memoria del compilador, lo que impide la reorganización de lecturas y escrituras por parte del compilador.

La **instrucción lwsync** es una barrera de memoria Xbox 360 que sincroniza un núcleo de procesador con la memoria caché L2. Garantiza que todas las escrituras anteriores **a lwsync** se realicen en la caché L2 antes de las escrituras siguientes. También garantiza que las lecturas que siguen **a lwsync** no obtengan datos más antiguos de L2 que las lecturas anteriores. El único tipo de reordenación que no impide es una lectura que avanza antes de una escritura a una dirección diferente. Por lo tanto, **lwsync** exige una ordenación de memoria que coincida con la ordenación de memoria predeterminada en procesadores x86 y x64. Para obtener la ordenación de memoria completa se requiere la instrucción de sincronización más costosa (también conocida como sincronización pesada), pero en la mayoría de los casos, esto no es necesario. Las opciones de reordenación de memoria Xbox 360 se muestran en la tabla siguiente.



| Xbox 360 reordenación           | Sin sincronización | lwsync | sync |
|-------------------------------|---------|--------|------|
| Lecturas que se adelantan a las lecturas   | Sí     | No     | No   |
| Escrituras que se adelantan a las escrituras | Sí     | No     | No   |
| Escrituras que se adelantan a las lecturas  | Sí     | No     | No   |
| Lecturas que se adelantan a las escrituras  | Sí     | Sí    | No   |



 

PowerPC también tiene las instrucciones de sincronización **isync** y **eieio** (que se usan para controlar la reordenación a la memoria con inhibición de almacenamiento en caché). Estas instrucciones de sincronización no deben ser necesarias para fines de sincronización normales.

En Windows, [**MemoryBar adherer**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se define en Winnt.h y le proporciona una instrucción de barrera de memoria diferente en función de si está compilando para x86 o x64. La instrucción de barrera de memoria actúa como una barrera completa, lo que impide que se reordenen las lecturas y escrituras a través de la barrera. Por lo tanto, **MemoryBarrden** en Windows proporciona una garantía de reordenación más sólida que en Xbox 360.

En Xbox 360, y en muchas otras CPU, hay una manera adicional de evitar la reordenación de lectura por parte de la CPU. Si lee un puntero y, a continuación, usa ese puntero para cargar otros datos, la CPU garantiza que las lecturas fuera del puntero no sean anteriores a la lectura del puntero. Si la marca de bloqueo es un puntero y todas las lecturas de datos compartidos están fuera del puntero, [**memoryBaromisión**](/windows/win32/api/winnt/nf-winnt-memorybarrier) se puede omitir, para obtener un ahorro de rendimiento moderado.

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

La [**instrucción MemoryBarorder**](/windows/win32/api/winnt/nf-winnt-memorybarrier) solo impide la reordenación de lecturas y escrituras en memoria almacenable en caché. Si asigna memoria como PAGE NOCACHE o PAGE WRITECOMBINE, una técnica común para los autores de controladores de dispositivos y para los desarrolladores de juegos \_ \_ en Xbox 360, **MemoryBar odbc** no tiene ningún efecto en los accesos a esta memoria. La mayoría de los desarrolladores no necesitan sincronización de memoria no almacenable en caché. Eso va más allá del ámbito de este artículo.

## <a name="interlocked-functions-and-cpu-reordering"></a>Funciones entrelazado y reordenación de CPU

A veces, la lectura o escritura que adquiere o libera un recurso se realiza mediante una de las **funciones InterlockedXxx.** En Windows, esto simplifica las cosas; porque en Windows, las **funciones InterlockedXxx** son barreras de memoria completa. De hecho, tienen una barrera de memoria de CPU antes y después de ellas, lo que significa que son una barrera completa de lectura,adquisición o liberación de escritura por sí mismos.

En Xbox 360, las **funciones InterlockedXxx** no contienen barreras de memoria de CPU. Impiden la reordenación del compilador de lecturas y escrituras, pero no la reordenación de CPU. Por lo tanto, en la mayoría de los casos cuando se usan funciones **InterlockedXxx** en Xbox 360, debe precederlas o seguirlas con **\_ \_ un lwsync** para convertirlas en una barrera de lectura-adquisición o de liberación de escritura. Para mayor comodidad y facilidad de lectura, hay versiones **acquire** **y release** de muchas de las **funciones InterlockedXxx.** Incluyen una barrera de memoria integrada. Por ejemplo, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) realiza un incremento entrelazado seguido de una barrera de memoria **\_ \_ lwsync** para proporcionar la funcionalidad completa de lectura y adquisición.

Se recomienda usar las  versiones Acquire y **Release** de las funciones **InterlockedXxx** (la mayoría de las cuales también están disponibles en Windows, sin ninguna penalización de rendimiento) para que su intención sea más obvia y facilitar la ejecución de las instrucciones de barrera de memoria en el lugar correcto. Cualquier uso de **InterlockedXxx** en Xbox 360 sin una barrera de memoria debe examinarse con mucho cuidado, ya que suele ser un error.

En este ejemplo se muestra cómo un subproceso puede pasar tareas u otros datos a otro subproceso mediante las versiones **Acquire** y **Release** de las **funciones InterlockedXxxSList.** Las **funciones InterlockedXxxSList** son una familia de funciones para mantener una lista vinculada de forma singly compartida sin bloqueo. Tenga en  cuenta **que** las variantes Adquirir y Liberar de estas funciones no están disponibles en Windows, pero las versiones normales de estas funciones son una barrera de memoria completa en Windows.

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

El estándar de C++ indica que las lecturas de variables volátiles no se pueden almacenar en caché, que las escrituras volátiles no se pueden retrasar y que las lecturas y escrituras volátiles no se pueden mover entre sí. Esto es suficiente para comunicarse con dispositivos de hardware, que es el propósito de la palabra clave volatile en el estándar de C++.

Sin embargo, las garantías del estándar no son suficientes para usar volatile para multiproceso. El estándar de C++ no impide que el compilador reordene las lecturas y escrituras no volátiles en relación con las lecturas y escrituras volátiles, y no indica nada sobre cómo evitar la reordenación de la CPU.

Visual C++ 2005 va más allá de C++ estándar para definir semánticas que admiten multiproceso para el acceso variable volátil. A partir de Visual C++ 2005, las lecturas de variables volátiles se definen para tener semántica de lectura y adquisición, y las escrituras en variables volátiles se definen para tener semántica de versión de escritura. Esto significa que el compilador no reorganizará las lecturas y escrituras pasadas, y en Windows se asegurará de que la CPU tampoco lo haga.

Es importante comprender que estas nuevas garantías solo se aplican a Visual C++ 2005 y versiones futuras de Visual C++. Por lo general, los compiladores de otros proveedores implementarán una semántica diferente, sin las garantías adicionales Visual C++ 2005. Además, en Xbox 360, el compilador no inserta ninguna instrucción para evitar que la CPU reordene las lecturas y escrituras.

## <a name="example-of-a-lock-free-data-pipe"></a>Ejemplo de una canalización Lock-Free datos

Una canalización es una construcción que permite a uno o varios subprocesos escribir datos que luego otros subprocesos leen. Una versión sin bloqueo de una canalización puede ser una manera elegante y eficaz de pasar trabajo de subproceso a subproceso. El SDK de DirectX proporciona **LockFreePipe,** una canalización sin bloqueo de un solo lector y un único escritor que está disponible en DXUTLockFreePipe.h. El mismo **LockFreePipe** está disponible en el SDK Xbox 360 en AtgLockFreePipe.h.

**LockFreePipe se** puede usar cuando dos subprocesos tienen una relación productor-consumidor. El subproceso de productor puede escribir datos en la canalización para que el subproceso del consumidor se procese en una fecha posterior, sin ningún bloqueo. Si la canalización se llena, se producirá un error en las escrituras y el subproceso del productor tendrá que intentarlo de nuevo más adelante, pero esto solo sucedería si el subproceso del productor está por delante. Si la canalización se vacía, se producirá un error en las lecturas y el subproceso de consumidor tendrá que intentarlo de nuevo más adelante, pero esto solo sucedería si no hay ningún trabajo para que el subproceso de consumidor lo haga. Si los dos subprocesos están bien equilibrados y la canalización es lo suficientemente grande, la canalización les permite pasar datos sin problemas junto con ningún retraso o bloque.

## <a name="xbox-360-performance"></a>Xbox 360 rendimiento

El rendimiento de las instrucciones y funciones de sincronización Xbox 360 variará en función del otro código que se esté ejecutando. La adquisición de bloqueos llevará mucho más tiempo si otro subproceso posee actualmente el bloqueo. [**Las operaciones de sección interlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) y critical tardan mucho más si otros subprocesos escriben en la misma línea de caché. El contenido de las colas del almacén también puede afectar al rendimiento. Por lo tanto, todos estos números son solo aproximaciones, generadas a partir de pruebas muy sencillas:

-   **lwsync** se midó como si tomara entre 33 y 48 ciclos.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) se midó como si tomara entre 225 y 260 ciclos.
-   La adquisición o liberación de una sección crítica se midó como que tardaba unos 345 ciclos.
-   La adquisición o liberación de una exclusión mutua se midó como que tardaba aproximadamente 2350 ciclos.

## <a name="windows-performance"></a>Rendimiento de Windows

El rendimiento de las instrucciones y funciones de sincronización en Windows varía ampliamente en función del tipo de procesador y la configuración, y de qué otro código se está ejecutando. Los sistemas de varios núcleos y de varios sockets suelen tardar más tiempo en ejecutar instrucciones de sincronización y la adquisición de bloqueos tarda mucho más tiempo si otro subproceso posee actualmente el bloqueo.

Sin embargo, incluso algunas medidas generadas a partir de pruebas muy sencillas son útiles:

-   [**MemoryBar was**](/windows/win32/api/winnt/nf-winnt-memorybarrier) measured as taking 20-90 cycles.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) se midó como si tomara entre 36 y 90 ciclos.
-   La adquisición o liberación de una sección crítica se midó de 40 a 100 ciclos.
-   La adquisición o liberación de una exclusión mutua se midó como si tomara entre 750 y 2500 ciclos.

Estas pruebas se realizaron Windows XP en una variedad de procesadores diferentes. Los tiempos cortos se encontraban en una máquina de un solo procesador y los tiempos más largos se encontraban en una máquina de varios procesadores.

Aunque adquirir y liberar bloqueos es más costoso que usar la programación sin bloqueos, es incluso mejor compartir datos con menos frecuencia, lo que evita el costo total.

## <a name="performance-thoughts"></a>Ideas de rendimiento

La adquisición o liberación de una sección crítica consta de una barrera de memoria, una operación **InterlockedXxx** y una comprobación adicional para controlar la recursividad y volver a una exclusión mutua, si es necesario. Debe tener cuidado con la implementación de su propia sección crítica, ya que girar en un bucle que espera a que un bloqueo sea libre, sin volver a una exclusión mutua, puede perder un rendimiento considerable. En el caso de las secciones críticas que tienen una gran contienda, pero que no se mantienen durante mucho tiempo, debe considerar el uso de [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) para que el sistema operativo gire durante un tiempo a la espera de que la sección crítica esté disponible en lugar de aplazarse inmediatamente a una exclusión mutua si la sección crítica es propiedad al intentar adquirirla. Para identificar las secciones críticas que pueden beneficiarse de un recuento de número, es necesario medir la longitud de la espera típica de un bloqueo determinado.

Si se usa un montón compartido para las asignaciones de memoria (el comportamiento predeterminado), cada asignación de memoria y gratis implica adquirir un bloqueo. A medida que aumenta el número de subprocesos y el número de asignaciones, los niveles de rendimiento disminuyen y, finalmente, comienzan a disminuir. El uso de montones por subproceso o la reducción del número de asignaciones puede evitar este cuello de botella de bloqueo.

Si un subproceso genera datos y otro subproceso está consumiendo datos, es posible que terminen compartiendo datos con frecuencia. Esto puede ocurrir si un subproceso carga recursos y otro subproceso representa la escena. Si el subproceso de representación hace referencia a los datos compartidos en cada llamada a draw, la sobrecarga de bloqueo será alta. Se puede obtener un rendimiento mucho mejor si cada subproceso tiene estructuras de datos privadas que luego se sincronizan una vez por fotograma o menos.

No se garantiza que los algoritmos sin bloqueo sean más rápidos que los algoritmos que usan bloqueos. Debe comprobar si los bloqueos realmente están causando problemas antes de intentar evitarlos, y debe medir para ver si el código sin bloqueo mejora realmente el rendimiento.

## <a name="platform-differences-summary"></a>Resumen de diferencias de plataforma

-   **Las funciones InterlockedXxx** impiden la reordenación de lectura y escritura de la CPU Windows, pero no en Xbox 360.
-   La lectura y escritura de variables volátiles mediante Visual Studio C++ 2005 impide la reordenación de lectura y escritura de la CPU en Windows, pero en Xbox 360, solo impide la reordenación de lectura y escritura del compilador.
-   Las escrituras se reordena en Xbox 360, pero no en x86 o x64.
-   Las lecturas se reordena en Xbox 360, pero en x86 o x64 solo se reordena con respecto a las escrituras y solo si las lecturas y escrituras tienen como destino ubicaciones diferentes.

## <a name="recommendations"></a>Recomendaciones

-   Use bloqueos cuando sea posible porque son más fáciles de usar correctamente.
-   Evite el bloqueo con demasiada frecuencia, para que los costos de bloqueo no se vuelvan significativos.
-   Evite mantener los bloqueos demasiado largos para evitar largas detenciones.
-   Use la programación sin bloqueo cuando corresponda, pero asegúrese de que las ganancias justifican la complejidad.
-   Use la programación sin bloqueos o bloqueos de giro en situaciones en las que se prohíben otros bloqueos, como cuando se comparten datos entre llamadas a procedimientos aplazados y código normal.
-   Use solo algoritmos de programación sin bloqueo estándar que se hayan demostrado que son correctos.
-   Al realizar la programación sin bloqueo, asegúrese de usar variables de marca volátil e instrucciones de barrera de memoria según sea necesario.
-   Al usar **InterlockedXxx en** Xbox 360, use las variantes **Adquirir** **y** Liberar.

## <a name="references"></a>Referencias

-   MSDN Library. "[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)." Referencia del lenguaje C++.
-   VanceMenteon. "Comprender[el impacto de las Low-Lock en aplicaciones multiproceso".](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps) MSDN Magazine, octubre de 2005.
-   Tantos, Michael. "[PowerPC Storage modelo y programación de AIX."](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl) IBM developerWorks, 16 de noviembre de 2005.
-   McKenney, Paul E.["Ordenación de memoria en microprocesadores modernos, parte II".](https://www.linuxjournal.com/article/8212) Diario de Linux, septiembre de 2005. \[En este artículo se detallan algunos detalles de x86.\]
-   Intel Corporation. "[Intel® 64 Architecture Memory Ordering](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)." Agosto de 2007. \[Se aplica a los procesadores IA-32 e Intel 64.\]
-   Niebler, Eric. "[Trip Report: Ad Hoc Meeting on Threads in C++](https://www.artima.com/cppsource/threads_meeting.html)." Origen de C++, 17 de octubre de 2006.
-   Thomas E. 2006. "Hacer[que la sincronización sin bloqueo sea rápida: implicaciones de rendimiento de la recuperación de memoria".](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf) Proceedings of the 2006 International Parallel and Distributed Processing Symposium (IPDPS 2006), Island, April 2006.

 

 