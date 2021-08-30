---
title: Codificación para varios núcleos en Xbox 360 y Windows
description: En este tema se dan algunos consejos sobre cómo empezar a trabajar con la programación multiproceso.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7657a5177527f1c13bfb1f0fdd643963a4f670d72b774e4142413231e7e3c58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102383"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Codificación para varios núcleos en Xbox 360 y Windows

Durante años, el rendimiento de los procesadores ha aumentado constantemente y los juegos y otros programas han tenido las ventajas de esta potencia creciente sin tener que hacer nada especial.

Las reglas han cambiado. El rendimiento de los núcleos de un solo procesador está aumentando ahora muy lentamente, en caso de que sea posible. Sin embargo, la potencia informática disponible en un equipo o consola típicos sigue creciendo. La diferencia es que la mayor parte de esta ganancia de rendimiento procede ahora de tener varios núcleos de procesador en una sola máquina, a menudo en un solo chip. El Xbox 360 CPU tiene tres núcleos de procesador en un chip y aproximadamente el 70 % de los procesadores de PC vendidos en 2006 eran de varios núcleos.

Los aumentos de la potencia de procesamiento disponible son tan drásticos como en el pasado, pero ahora los desarrolladores tienen que escribir código multiproceso para poder usar esta potencia. La programación multiproceso aporta nuevos desafíos de diseño y programación. En este tema se dan algunos consejos sobre cómo empezar a trabajar con la programación multiproceso.

## <a name="the-importance-of-good-design"></a>La importancia del buen diseño

Un buen diseño de programas multiproceso es fundamental, pero puede ser muy difícil. Si mueve los principales sistemas de juego a subprocesos diferentes, es probable que cada subproceso pase la mayor parte del tiempo esperando a los demás subprocesos. Este tipo de diseño conduce a una mayor complejidad y un esfuerzo de depuración significativo, sin prácticamente ninguna ganancia de rendimiento.

Cada vez que los subprocesos tienen que sincronizar o compartir datos, existe la posibilidad de daños en los datos, la sobrecarga de sincronización, los interbloqueos y la complejidad. Por lo tanto, el diseño multiproceso debe documentar claramente cada punto de sincronización y comunicación, y debe minimizar esos puntos tanto como sea posible. Cuando los subprocesos necesitan comunicarse, aumentará el esfuerzo de codificación, lo que puede reducir la productividad si afecta a demasiado código fuente.

El objetivo de diseño más sencillo para multithreading es dividir el código en grandes partes independientes. Si, a continuación, restringe estas partes a la comunicación solo unas pocas veces por fotograma, verá una aceleración significativa del multithreading, sin una complejidad excesiva.

## <a name="typical-threaded-tasks"></a>Tareas típicas de subprocesos

Algunos tipos de tareas han demostrado ser amenables para colocarse en subprocesos independientes. La lista siguiente no pretende ser exhaustiva, pero debe proporcionar algunas ideas.

### <a name="rendering"></a>Representación

La representación , que puede incluir recorrer el gráfico de la escena o, posiblemente, llamar solo a funciones D3D, suele representar el 50 % o más del tiempo de CPU. Por lo tanto, mover la representación a otro subproceso puede tener ventajas significativas. El subproceso de actualización puede rellenar algún tipo de búfer de descripción de representación, que el subproceso de representación puede procesar.

El subproceso de actualización del juego siempre tiene un fotograma delante del subproceso de representación, lo que significa que tarda dos fotogramas antes de que las acciones del usuario se muestren en la pantalla. Aunque esta mayor latencia puede ser un problema, el aumento de la velocidad de fotogramas al dividir la carga de trabajo generalmente mantiene la latencia total aceptable.

En la mayoría de los casos, toda la representación se realiza en un único subproceso, pero es un subproceso diferente de la actualización del juego.

La marca D3DCREATE MULTITHREADED a veces se usa para permitir la representación en un subproceso y la creación de recursos en otros subprocesos; esta marca se omite en Xbox 360 y debe evitar su uso en \_ Windows. Al Windows, la especificación de esta marca obliga a D3D a dedicar una cantidad significativa de tiempo a la sincronización, lo que ralentiza el subproceso de representación.

### <a name="file-decompression"></a>Descompresión de archivos

Los tiempos de carga siempre son demasiado largos y transmitir datos a la memoria sin afectar a la velocidad de fotogramas puede ser complicado. Si todos los datos se comprimen agresivamente en el disco, es menos probable que la velocidad de transferencia de datos desde el disco duro o el disco óptico sea un factor de limitación. En un procesador de un solo subproceso, normalmente no hay suficiente tiempo de procesador disponible para la compresión para ayudar a los tiempos de carga. Sin embargo, en un sistema de varios procesadores, la descompresión de archivos usa ciclos de CPU que, de lo contrario, se desperdiciaría. mejora los tiempos de carga y el streaming; y ahorra espacio en el disco.

No use la descompresión de archivos como sustituto del procesamiento que se debe realizar durante la producción. Por ejemplo, si dedica un subproceso adicional al análisis de datos XML durante la carga de nivel, no usa multithreading para mejorar la experiencia del reproductor.

Al usar un subproceso de descompresión de archivos, debe seguir usando E/S de archivos asincrónicas y lecturas grandes para maximizar la eficacia de lectura de datos.

### <a name="graphics-fluff"></a>Fluff de gráficos

Hay muchas mejoras gráficas que mejoran el aspecto del juego, pero no son estrictamente necesarias. Esto incluye elementos como animaciones en la nube generadas por procedimientos, simulaciones de pesquete y vello, ondas de procedimientos, procedimientos, más partículas o física sin juego.

Dado que estos efectos no afectan al juego, no provocan problemas de sincronización complicados: pueden sincronizarse con los demás subprocesos una vez por fotograma o con menos frecuencia. Además, en juegos para Windows estos efectos pueden agregar valor a los jugadores con CPU de varios núcleos, a la vez que se omiten de forma silenciosa en equipos de un solo núcleo, lo que ofrece una manera sencilla de escalar a través de una amplia gama de funcionalidades.

### <a name="physics"></a>Física

La física a menudo no se puede colocar en un subproceso independiente para ejecutarse en paralelo con la actualización del juego porque la actualización del juego normalmente requiere los resultados de los cálculos físicos inmediatamente. La alternativa a la física multithreading es ejecutarla en varios procesadores. Aunque esto se puede hacer, se trata de una tarea compleja que requiere acceso frecuente a las estructuras de datos compartidos. Si puede mantener la carga de trabajo física lo suficientemente baja como para caber en el subproceso principal, el trabajo será más sencillo.

Hay disponibles bibliotecas que admiten la ejecución de la física en varios subprocesos. Sin embargo, esto puede dar lugar a un problema: cuando el juego ejecuta la física, usa muchos subprocesos, pero el resto del tiempo usa pocos. La ejecución de la física en varios subprocesos requerirá abordar esto para que la carga de trabajo se distribuye uniformemente sobre el marco. Si escribe un motor físico multiproceso, debe prestar mucha atención a todas las estructuras de datos, los puntos de sincronización y el equilibrio de carga.

## <a name="example-multithreaded-designs"></a>Diseños multiproceso de ejemplo

Los juegos Windows deben ejecutarse en equipos con diferentes números de núcleos de CPU. La mayoría de las máquinas de juegos siguen teniendo solo un núcleo, aunque el número de máquinas de dos núcleos está creciendo rápidamente. Un juego típico para Windows podría dividir su carga de trabajo en un subproceso para la actualización y representación, con subprocesos de trabajo opcionales para agregar funcionalidad adicional. Además, probablemente se usarían algunos subprocesos en segundo plano para realizar E/S de archivos y redes. En la figura 1 se muestran los subprocesos, junto con los puntos de transferencia de datos principales.

**Figura 1. Diseño de subprocesos en un juego para Windows**

![diseño de subprocesos en un juego para ventanas](images/coding-for-multiple-cores-1.gif)

Un juego de Xbox 360 típico puede usar subprocesos de software adicionales que consumen mucha CPU, por lo que podría dividir su carga de trabajo en un subproceso de actualización, un subproceso de representación y tres subprocesos de trabajo, como se muestra en la figura 2.

**Figura 2. Diseño de subprocesos en un juego para Xbox 360**

![diseño de subprocesos en un juego para Xbox 360](images/coding-for-multiple-cores-2.gif)

A excepción de la E/S de archivos y las redes, todas estas tareas tienen el potencial de ser lo suficientemente intensivas en la CPU como para beneficiarse de estar en su propio subproceso de hardware. Estas tareas también tienen la posibilidad de ser lo suficientemente independientes como para que se puedan ejecutar durante un fotograma completo sin comunicarse.

El subproceso de actualización del juego administra la entrada del controlador, la inteligencia artificial y la física, y prepara instrucciones para los otros cuatro subprocesos. Estas instrucciones se colocan en búferes propiedad del subproceso de actualización del juego, por lo que no se requiere ninguna sincronización a medida que se generan las instrucciones.

Al final del fotograma, el subproceso de actualización del juego entrega los búferes de instrucciones a los otros cuatro subprocesos y, a continuación, comienza a trabajar en el siguiente fotograma, rellenando otro conjunto de búferes de instrucciones.

Dado que los subprocesos de actualización y representación funcionan en lockstep entre sí, sus búferes de comunicación simplemente tienen doble búfer: en un momento dado, el subproceso de actualización rellena un búfer mientras el subproceso de representación lee del otro.

Los demás subprocesos de trabajo no están necesariamente asociados a la velocidad de fotogramas. Descomprimir un fragmento de datos puede tardar mucho menos que un fotograma, o puede tardar muchos fotogramas. Incluso es posible que la simulación de peluquería y vello no tenga que ejecutarse exactamente a la velocidad de fotogramas, ya que las actualizaciones menos frecuentes pueden ser bastante aceptables. Por lo tanto, estos tres subprocesos necesitan estructuras de datos diferentes para comunicarse con el subproceso de actualización y el subproceso de representación. Cada uno de ellos necesita una cola de entrada que pueda contener solicitudes de trabajo y el subproceso de representación necesita una cola de datos que pueda contener los resultados generados por los subprocesos. Al final de cada fotograma, el subproceso de actualización agregará un bloque de solicitudes de trabajo a las colas de subprocesos de trabajo. Agregar a la lista una sola vez por fotograma garantiza que el subproceso de actualización minimiza la sobrecarga de sincronización. Cada uno de los subprocesos de trabajo extrae las asignaciones de la cola de trabajo lo más rápido posible, mediante un bucle similar al siguiente:


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



Dado que los datos van de los subprocesos de actualización a los subprocesos de trabajo y, a continuación, al subproceso de representación, puede haber un retraso de tres o más fotogramas antes de que algunas acciones lo hagan en la pantalla. Sin embargo, si asigna tareas tolerantes a la latencia a los subprocesos de trabajo, esto no debería ser un problema.

Un diseño alternativo sería tener varios subprocesos de trabajo que se dibujan desde la misma cola de trabajo. Esto daría equilibrio de carga automático y haría más probable que todos los subprocesos de trabajo permanezcan ocupados.

El subproceso de actualización del juego debe tener cuidado de no dar demasiado trabajo a los subprocesos de trabajo o, de lo contrario, las colas de trabajo pueden crecer continuamente. La forma en que el subproceso de actualización administra esto depende del tipo de tareas que están realizando los subprocesos de trabajo.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Multithreading simultáneo y número de subprocesos

Todos los subprocesos no se crean iguales. Dos subprocesos de hardware pueden estar en chips independientes, en el mismo chip o incluso en el mismo núcleo. La configuración más importante que deben tener en cuenta los programadores de juegos son dos subprocesos de hardware en un núcleo: multiproceso simultáneo (SMT) o tecnología de Hyper-Threading (tecnología HT).

Los subprocesos SMT o HT Technology comparten los recursos del núcleo de CPU. Dado que comparten las unidades de ejecución, la velocidad máxima de ejecución de dos subprocesos en lugar de uno suele ser del 10 al 20 por ciento, en lugar del 100 por ciento que es posible desde dos subprocesos de hardware independientes.

Más significativamente, los subprocesos SMT o HT Technology comparten las memorias caché de datos y las instrucciones L1. Si sus patrones de acceso a la memoria son incompatibles, pueden acabar en la pugna por la memoria caché y provocar muchos error en la memoria caché. En el peor de los casos, el rendimiento total del núcleo de CPU puede reducirse realmente cuando se ejecuta un segundo subproceso. En Xbox 360, se trata de un problema bastante sencillo. Se conoce la configuración del Xbox 360 (tres núcleos de CPU cada uno con dos subprocesos de hardware) y los desarrolladores asignan sus subprocesos de software a subprocesos de CPU específicos y pueden medir para ver si su diseño de subprocesos les proporciona un rendimiento adicional.

En Windows, la situación es más complicada. El número de subprocesos y su configuración variará de un equipo a otro y determinar la configuración es complicado. La función [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) proporciona información sobre la relación entre los distintos subprocesos de hardware y esta función está disponible en Windows Vista, Windows 7 y Windows XP SP3. Por lo tanto, por ahora tiene que usar la instrucción CPUID y los algoritmos que proporciona Intel y AMD para decidir cuántos subprocesos "reales" tiene disponibles. Consulte las referencias para obtener más información.

El ejemplo CoreDetection del SDK de DirectX contiene código de ejemplo que usa la función [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) o la instrucción CPUID para devolver la topología de núcleo de CPU. La instrucción CPUID se usa si **GetLogicalProcessorInformation** no se admite en la plataforma actual. CoreDetection se puede encontrar en las siguientes ubicaciones:

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Fuente:
</dt> <dd>

*Raíz del SDK de* \\ DirectX Ejemplos \\ de C++ \\ Misc \\ CoreDetection

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Ejecutable:
</dt> <dd>

*Raíz del SDK de* \\ DirectX Ejemplos \\ de errores de C++ \\ \\ \\CoreDetection.exe

</dd> </dl>

La suposición más segura es no tener más de un subproceso que consume mucha CPU por núcleo de CPU. Tener más subprocesos con un uso intensivo de CPU que los núcleos de CPU ofrece pocas ventajas o ninguna, y aporta la sobrecarga adicional y la complejidad de subprocesos adicionales.

## <a name="creating-threads"></a>Crear subprocesos

La creación de subprocesos es una operación bastante sencilla, pero hay muchos errores potenciales. El código siguiente muestra la manera adecuada de crear un subproceso, esperar a que finalice y, a continuación, limpiarlo.


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



Al crear un subproceso, tiene la opción de especificar el tamaño de pila para el subproceso secundario, o bien especificar cero, en cuyo caso el subproceso secundario heredará el tamaño de pila del subproceso primario. En Xbox 360, donde las pilas se confirman por completo cuando se inicia el subproceso, la especificación de cero puede desperdiciar memoria significativa, ya que muchos subprocesos secundarios no necesitarán tanta pila como el elemento primario. En Xbox 360 también es importante que el tamaño de la pila sea un múltiplo de 64 KB.

Si usa la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para crear subprocesos, el tiempo de ejecución de C/C++ (CRT) no se inicializará correctamente en Windows. Se recomienda usar la función [**\_ beginthreadex de**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) CRT en su lugar.

El valor devuelto de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) es un identificador de subproceso. Este subproceso se puede usar para esperar a que finalice el subproceso secundario, lo que es mucho más sencillo y mucho más eficaz que girar en un bucle que comprueba el estado del subproceso. Para esperar a que finalice el subproceso, simplemente llame a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) con el identificador del subproceso.

Los recursos del subproceso no se liberarán hasta que el subproceso haya finalizado y se haya cerrado el identificador del subproceso. Por lo tanto, es importante cerrar el identificador de subproceso con [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) cuando haya terminado con él. Si va a esperar a que el subproceso finalice con [**WaitForSingleObject,**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)asegúrese de no cerrar el identificador hasta que se haya completado la espera.

En Xbox 360, debe asignar explícitamente subprocesos de software a un subproceso de hardware determinado mediante **XSetThreadProcessor**. De lo contrario, todos los subprocesos secundarios permanecerán en el mismo subproceso de hardware que el primario. En Windows, puede usar [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) para sugerir al sistema operativo en qué subprocesos de hardware debe ejecutarse el subproceso. Por lo general, esta técnica debe evitarse en Windows, ya que no se sabe qué otros procesos podrían estar ejecutándose en el sistema. Normalmente es mejor dejar que el programador de Windows asigne los subprocesos a subprocesos de hardware inactivos.

La creación de subprocesos es una operación costosa. Los subprocesos se deben crear y destruir rara vez. Si desea crear y destruir subprocesos con frecuencia, use un grupo de subprocesos que esperen por el trabajo en su lugar.

## <a name="synchronizing-threads"></a>Sincronizar subprocesos

Para que varios subprocesos funcionen juntos, debe ser capaz de sincronizar subprocesos, pasar mensajes y solicitar acceso exclusivo a los recursos. Windows y Xbox 360 incluyen un amplio conjunto de primitivas de sincronización. Para obtener detalles completos sobre estas primitivas de sincronización, consulte la documentación de la plataforma.

### <a name="exclusive-access"></a>Acceso exclusivo

La obtención de acceso exclusivo a un recurso, una estructura de datos o una ruta de acceso de código es una necesidad común. Una opción para obtener acceso exclusivo es una exclusión mutua, cuyo uso típico se muestra aquí.


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



Las secciones críticas tienen una semántica similar a las exclusiones mutuas, pero se pueden usar para sincronizar solo dentro de un proceso, no entre procesos. Su principal ventaja es que se ejecutan aproximadamente veinte veces más rápido que las exclusiones mutuas.

### <a name="events"></a>Eventos

Si dos subprocesos(quizás un subproceso de actualización y un subproceso de representación) están tomando turnos con un par de búferes de descripción de representación, necesitan una manera de indicar cuándo han terminado con su búfer determinado. Para ello, asocie un evento (asignado con [**CreateEvent)**](/windows/win32/api/synchapi/nf-synchapi-createeventa)a cada búfer. Cuando un subproceso se realiza con un búfer, puede usar [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) para indicarlo y, a continuación, puede llamar a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) en el evento del otro búfer. Esta técnica se extrapola fácilmente para triplicar el almacenamiento en búfer de los recursos.

### <a name="semaphores"></a>Semáforos

Un semáforo se usa para controlar cuántos subprocesos se pueden ejecutar y se usa normalmente para implementar colas de trabajo. Un subproceso agrega trabajo a una cola y usa [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) cada vez que agrega un nuevo elemento a la cola. Esto permite liberar un subproceso de trabajo del grupo de subprocesos en espera. Los subprocesos de trabajo simplemente llaman a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)y, cuando devuelve , saben que hay un elemento de trabajo en la cola para ellos. Además, se debe usar una sección crítica u otra técnica de sincronización para garantizar el acceso seguro a la cola de trabajo compartida.

### <a name="avoid-suspendthread"></a>Evitar SuspendThread

A veces, cuando se desea que un subproceso detenga lo que está haciendo, es tentador usar [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) en lugar de las primitivas de sincronización correctas. Esto siempre es una mala idea y puede provocar fácilmente interbloqueos y otros problemas. **SuspendThread** también interactúa mal con el depurador de Visual Studio. Evite **SuspendThread.** Use [**WaitForSingleObject en su**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) lugar.

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject y WaitForMultipleObjects

La función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) es la función de sincronización que se usa con más frecuencia. Sin embargo, a veces desea que un subproceso espere hasta que se cumplen varias condiciones simultáneamente o hasta que se cumple uno de un conjunto de condiciones. En este caso, debe usar [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

### <a name="interlocked-functions-and-lockless-programming"></a>Funciones interbloqueadas y programación sin bloqueo

Hay una familia de funciones para realizar operaciones sencillas y seguras para subprocesos sin usar bloqueos. Se trata de la familia de funciones Interlocked, como [**InterlockedIncrement.**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) Estas funciones, además de otras técnicas que usan una cuidadosa configuración de marcas, se conocen conjuntamente como programación sin bloqueo. La programación sin bloqueo puede ser muy difícil de hacer correctamente y es mucho más difícil en Xbox 360 que en Windows.

Para obtener más información sobre la programación sin bloqueos, vea [Consideraciones](./lockless-programming.md)de programación sin bloqueo para Xbox 360 y Microsoft Windows .

### <a name="minimizing-synchronization"></a>Minimizar la sincronización

Algunos métodos de sincronización son más rápidos que otros. Sin embargo, en lugar de optimizar el código eligiendo las técnicas de sincronización más rápidas posibles, suele ser mejor sincronizar con menos frecuencia. Esto es más rápido que sincronizar con demasiada frecuencia y facilita la depuración del código.

Algunas operaciones, como la asignación de memoria, pueden tener que usar primitivas de sincronización para funcionar correctamente. Por lo tanto, realizar asignaciones frecuentes desde el montón compartido predeterminado dará lugar a una sincronización frecuente, lo que desperdiciará cierto rendimiento. Evitar asignaciones frecuentes o usar montones por subproceso (mediante HEAP NO SERIALIZE si usa HeapCreate) puede evitar \_ \_ esta sincronización oculta.

Otra causa de la sincronización oculta es D3DCREATE MULTITHREADED, que hace que D3D en Windows use la sincronización \_ en muchas operaciones. (La marca se omite en Xbox 360).

Los datos por subproceso, también conocidos como almacenamiento local de subprocesos, pueden ser una manera importante de evitar la sincronización. Visual C++ permite declarar variables globales como por subproceso con la **\_ \_ sintaxis declspec(thread).**


```C++
__declspec( thread ) int tls_i = 1;
```



Esto proporciona a cada subproceso del proceso su propia copia de tls i, a la que se puede hacer referencia de forma segura y eficaz \_ sin necesidad de sincronización.

La **\_ \_ técnica declspec(thread)** no funciona con archivos DLL cargados dinámicamente. Si usa archivos DLL cargados dinámicamente, deberá usar la familia de funciones TLSAlloc para implementar el almacenamiento local de subprocesos.

## <a name="destroying-threads"></a>Destruir subprocesos

La única manera segura de destruir un subproceso es hacer que el propio subproceso se cierre, ya sea devolviendo desde la función de subproceso principal o haciendo que el subproceso llame a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx). Si se crea un subproceso con [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), debe usar **\_ endthreadex** o devolver desde la función de subproceso principal, ya que el uso de **ExitThread** no liberará correctamente los recursos de CRT. No llame nunca [**a la función TerminateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) porque el subproceso no se limpiará correctamente. Los subprocesos siempre deben confirmar la confirmación, ya que nunca se deben volver a usar.

## <a name="openmp"></a>OpenMP

OpenMP es una extensión de lenguaje para agregar multithreading al programa mediante pragmas para guiar al compilador en la paralelización de bucles. OpenMP es compatible con Visual C++ 2005 en Windows y Xbox 360 y se puede usar junto con la administración manual de subprocesos. OpenMP puede ser una manera cómoda de usar elementos multiproceso del código, pero es poco probable que sea la solución ideal, especialmente para juegos. OpenMP puede ser más aplicable a tareas de producción de ejecución más larga, como el procesamiento de arte y otros recursos. Para más información, consulte la documentación Visual C++ o vaya al sitio web [de](https://www.openmp.org/)OpenMP.

## <a name="profiling"></a>Generación de perfiles

La generación de perfiles multiproceso es importante. Es fácil acabar con tiempos de espera largos en los que los subprocesos se esperan entre sí. Estos puestos pueden ser difíciles de encontrar y diagnosticar. Para ayudar a identificarlos, considere la posibilidad de agregar instrumentación a las llamadas de sincronización. Un profiler de muestreo también puede ayudar a identificar estos problemas porque puede registrar información de tiempo sin modificarla considerablemente.

## <a name="timing"></a>Control de tiempo

La instrucción rdtsc es una manera de obtener información de tiempo precisa sobre Windows. Desafortunadamente, rdtsc tiene varios problemas que lo convierten en una mala opción para el título de envío. Los contadores rdtsc no se sincronizan necesariamente entre CPU, por lo que cuando el subproceso se mueve entre subprocesos de hardware, puede obtener grandes diferencias positivas o negativas. En función de la configuración de administración de energía, la frecuencia con la que se incrementa el contador rdtsc también puede cambiar a medida que se ejecuta el juego. Para evitar estas dificultades, debe preferir [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para un tiempo de alta precisión en el juego de envío. Para obtener más información sobre el control de tiempo, vea Game Timing and Multicore Processors (Control de tiempo de juego [y procesadores multinúcleo).](./game-timing-and-multicore-processors.md)

## <a name="debugging"></a>Depuración

Visual Studio la depuración multiproceso para Windows y Xbox 360. La Visual Studio subprocesos de llamada permite cambiar entre subprocesos para ver las diferentes pilas de llamadas y variables locales. La ventana subprocesos también permite inmovilizar y descongelar subprocesos concretos.

En Xbox 360, puede usar la meta variable **\@ hwthread** en la ventana de reloj para mostrar el subproceso de hardware en el que se ejecuta el subproceso de software seleccionado actualmente.

La ventana subprocesos es más fácil de usar si se le asigne un nombre significativo a los subprocesos. Visual Studio y otros depuradores de Microsoft permiten nombrar los subprocesos. Implemente la **siguiente función SetThreadName** y llámela desde cada subproceso a medida que se inicia.


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



El depurador de kernel (KD) y WinDBG también admiten la depuración multiproceso.

## <a name="testing"></a>Prueba

La programación multiproceso puede ser complicada y algunos errores multiproceso solo se muestran en raras ocasiones, lo que hace que sean difíciles de encontrar y corregir. Una de las mejores maneras de vaciarlos es probar en una amplia gama de equipos, especialmente en aquellos con cuatro o más procesadores. El código multiproceso que funciona perfectamente en un equipo de un solo subproceso puede producir un error al instante en un equipo de cuatro procesadores. Las características de rendimiento y control de tiempo de LAS CPU de AMD e Intel pueden variar considerablemente, por lo que debe asegurarse de realizar pruebas en equipos con varios procesadores en función de las CPU de ambos proveedores.

## <a name="windows-vista-and-windows-7-improvements"></a>Windows Vista y Windows 7 Mejoras

Para los juegos que tienen como destino las versiones más recientes de Windows, hay una serie de API que pueden simplificar la creación de aplicaciones multiproceso escalables. Esto es especialmente cierto con la nueva API ThreadPool y algunas primitivas de sincronización adicionales (variables de condición, el bloqueo de lectura/escritura más fino y la inicialización de un solo uso). Puede encontrar información general sobre estas tecnologías en los siguientes artículos de MSDN Magazine:

-   [Mejora de la escalabilidad con nuevas API de grupo de subprocesos](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Primitivas de sincronización nuevas para Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Las aplicaciones que usan características de [Direct3D 11](../direct3d11/direct3d-11-features.md) en estos sistemas operativos también pueden aprovechar el nuevo diseño para la creación simultánea de objetos y las listas de comandos de contexto diferido para mejorar la escalabilidad de la representación multiproceso.

## <a name="summary"></a>Resumen

Con un diseño cuidadoso que minimiza las interacciones entre subprocesos, puede obtener mejoras sustanciales de rendimiento de la programación multiproceso sin agregar una complejidad excesiva al código. Esto permitirá que el código del juego pase a la siguiente ola de mejoras del procesador y ofrezca experiencias de juego cada vez más atractivas.

## <a name="references"></a>Referencias

-   Jim Bevethread & Robert Weiner, *Multithreading Applications in Win32*, Addison-Gran, 1997
-   Walbourn, [Game Timing y procesadores multinúcleo](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   MSDN Library: [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 