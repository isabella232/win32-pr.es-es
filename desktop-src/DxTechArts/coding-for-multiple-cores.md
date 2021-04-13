---
title: Codificación para varios núcleos en Xbox 360 y Windows
description: En este tema se proporcionan consejos sobre cómo empezar a trabajar con la programación multiproceso.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421603"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Codificación para varios núcleos en Xbox 360 y Windows

Durante años, el rendimiento de los procesadores ha aumentado de forma oportuna, y los juegos y otros programas han aprovechado las ventajas de este aumento de la capacidad sin tener que hacer nada especial.

Las reglas han cambiado. El rendimiento de los núcleos de procesador único ahora está aumentando muy lentamente, en caso de que haya. Sin embargo, la potencia de la informática disponible en un equipo o consola típicos sigue creciendo. La diferencia es que la mayor parte de esta mejora del rendimiento ahora proviene de tener varios núcleos de procesador en un solo equipo, a menudo en un solo chip. La CPU Xbox 360 tiene tres núcleos de procesador en un chip y, aproximadamente, el 70 por ciento de los procesadores de PC vendidos en 2006 eran de varios núcleos.

Los aumentos en la potencia de procesamiento disponible son tan drásticos como en el pasado, pero ahora los desarrolladores tienen que escribir código multiproceso para poder usar esta capacidad. La programación multiproceso aporta nuevos desafíos de diseño y programación. En este tema se proporcionan consejos sobre cómo empezar a trabajar con la programación multiproceso.

## <a name="the-importance-of-good-design"></a>La importancia de un buen diseño

Un buen diseño de programas multiproceso es fundamental, pero puede ser muy difícil. Si mueve sus principales sistemas de juegos a distintos subprocesos, probablemente encontrará que cada subproceso dedica la mayor parte del tiempo esperando a los demás subprocesos. Este tipo de diseño conduce a una mayor complejidad y a un esfuerzo de depuración importante, sin apenas aumento de rendimiento.

Cada vez que los subprocesos tienen que sincronizar o compartir datos, existe la posibilidad de daños en los datos, la sobrecarga de la sincronización, los interbloqueos y la complejidad. Por lo tanto, el diseño multiproceso debe documentar claramente cada sincronización y punto de comunicación, y debe minimizar estos puntos tanto como sea posible. Si los subprocesos necesitan comunicarse, el esfuerzo de codificación aumentará, lo que puede reducir la productividad si afecta demasiado código fuente.

El objetivo de diseño más sencillo para el multithreading es dividir el código en partes independientes grandes. Si, a continuación, restringe estas partes para que se comuniquen unas pocas veces por fotograma, verá un aumento significativo del multithreading, sin complejidad excesiva.

## <a name="typical-threaded-tasks"></a>Tareas de subprocesos típicas

Algunos tipos de tareas han demostrado someterse a la depuración de subprocesos independientes. La lista siguiente no pretende ser exhaustiva, pero debe aportar algunas ideas.

### <a name="rendering"></a>Representación

La representación, que puede incluir recorrer el gráfico de escena o, posiblemente, llamar solo a las funciones D3D, suele tener en cuenta un 50 por ciento o más de tiempo de CPU. Por lo tanto, el traslado de la representación a otro subproceso puede tener ventajas significativas. El subproceso de actualización puede rellenar algún tipo de búfer de descripción de representación, que puede procesar el subproceso de representación.

El subproceso de actualización del juego siempre es un fotograma por delante del subproceso de representación, lo que significa que toma dos fotogramas antes de que las acciones del usuario se muestren en la pantalla. Aunque esta mayor latencia puede ser un problema, la mayor velocidad de fotogramas de la división de la carga de trabajo generalmente mantiene la latencia total aceptable.

En la mayoría de los casos, toda la representación se realiza en un único subproceso, pero es un subproceso diferente de la actualización del juego.

La \_ marca multiproceso D3DCREATE se usa a veces para permitir la representación en un subproceso y la creación de recursos en otros subprocesos; esta marca se omite en Xbox 360 y debe evitar usarla en Windows. En Windows, la especificación de esta marca obliga a D3D a gastar una cantidad significativa de tiempo en la sincronización, lo que ralentiza el subproceso de representación.

### <a name="file-decompression"></a>Descompresión de archivos

Los tiempos de carga siempre son demasiado largos y el streaming de datos en memoria sin afectar a la velocidad de fotogramas puede ser desafiante. Si todos los datos se comprimen agresivamente en el disco, es menos probable que la velocidad de transferencia de datos del disco duro o del disco óptico sea un factor limitador. En un procesador de un solo subproceso, normalmente no hay suficiente tiempo de procesador disponible para la compresión a fin de ayudar a los tiempos de carga. Sin embargo, en un sistema con varios procesadores, la descompresión de archivos utiliza ciclos de CPU que de otro modo se desperdiciarían; mejora los tiempos de carga y el streaming; y ahorra espacio en el disco.

No utilice la descompresión de archivos como reemplazo de procesamiento que se debe realizar durante la producción. Por ejemplo, si se dedica un subproceso adicional al análisis de datos XML durante la carga de nivel, no se utiliza multithreading para mejorar la experiencia del jugador.

Al usar un subproceso de descompresión de archivos, debe seguir usando e/s asincrónica de archivos y lecturas grandes para maximizar la eficacia de la lectura de datos.

### <a name="graphics-fluff"></a>Gráficos desenfadados

Hay muchos niceties gráficos que mejoran el aspecto del juego pero no son estrictamente necesarios. Esto incluye cosas como animaciones en la nube generadas por procedimientos, simulaciones de tela y pelo, ondas de procedimiento, vegetación de procedimientos, más partículas o física sin juegos.

Dado que estos efectos no afectan al juego, no causan problemas de sincronización complicados; pueden sincronizarse con otros subprocesos una vez por fotograma o con menos frecuencia. Además, en juegos para Windows estos efectos pueden agregar valor para los jugadores con CPU de varios núcleos, mientras que se omiten de forma silenciosa en equipos de un solo núcleo, lo que proporciona una manera sencilla de escalar a través de una amplia gama de funcionalidades.

### <a name="physics"></a>Física

A menudo, no se puede colocar la física en un subproceso independiente para ejecutarse en paralelo con la actualización del juego, ya que la actualización del juego normalmente requiere inmediatamente los resultados de los cálculos físicos. La alternativa para la física multithreading es ejecutarla en varios procesadores. Aunque esto se puede hacer, es una tarea compleja que requiere un acceso frecuente a las estructuras de datos compartidas. Si puede mantener la carga de trabajo física lo suficientemente baja como para caber en el subproceso principal, el trabajo será más sencillo.

Están disponibles las bibliotecas que admiten la ejecución de física en varios subprocesos. Sin embargo, esto puede dar lugar a un problema: cuando el juego se está ejecutando física, usa muchos subprocesos, pero el resto del tiempo usa pocos. La ejecución de la física en varios subprocesos requerirá abordar esto para que la carga de trabajo se distribuya uniformemente a través del marco. Si escribe un motor físico multiproceso, debe prestar especial atención a todas las estructuras de datos, los puntos de sincronización y el equilibrio de carga.

## <a name="example-multithreaded-designs"></a>Diseños multiproceso de ejemplo

Los juegos para Windows deben ejecutarse en equipos con un número diferente de núcleos de CPU. La mayoría de las máquinas de juegos todavía tienen un solo núcleo, aunque el número de máquinas con dos núcleos crece rápidamente. Un juego típico para Windows podría interrumpir su carga de trabajo en un subproceso para su actualización y representación, con subprocesos de trabajo opcionales para agregar funcionalidad adicional. Además, es probable que se utilicen algunos subprocesos en segundo plano para realizar operaciones de e/s de archivos y redes. En la figura 1 se muestran los subprocesos, junto con los puntos de transferencia de datos principales.

**Figura 1. Diseño de subprocesos en un juego para Windows**

![diseño de subprocesos en un juego para Windows](images/coding-for-multiple-cores-1.gif)

Un juego de Xbox 360 típico puede usar subprocesos de software intensivos de CPU adicionales, por lo que podría dividir su carga de trabajo en un subproceso de actualización, un subproceso de representación y tres subprocesos de trabajo, como se muestra en la figura 2.

**Figura 2. Diseño de subprocesos en un juego para Xbox 360**

![diseño de subprocesos en un juego para Xbox 360](images/coding-for-multiple-cores-2.gif)

A excepción de las operaciones de e/s de archivos y las redes, todas estas tareas tienen el potencial de ser lo suficientemente intensivo de la CPU como para beneficiarse de su propio subproceso de hardware. Estas tareas también tienen la posibilidad de ser lo suficientemente independientes como para que puedan ejecutarse en todo un marco sin comunicarse.

El subproceso de actualización del juego administra la entrada del controlador, AI y física, y prepara instrucciones para los otros cuatro subprocesos. Estas instrucciones se colocan en búferes propiedad del subproceso de actualización del juego, por lo que no se requiere ninguna sincronización a medida que se generan las instrucciones.

Al final del marco, el subproceso de actualización del juego entrega los búferes de instrucciones a los otros cuatro subprocesos y, a continuación, comienza a trabajar en el siguiente fotograma, rellenando otro conjunto de búferes de instrucciones.

Dado que los subprocesos de actualización y representación funcionan en lógico entre sí, sus búferes de comunicación son simplemente de doble búfer: en un momento dado, el subproceso de actualización está llenando un búfer mientras el subproceso de representación está leyendo desde el otro.

Los otros subprocesos de trabajo no están necesariamente asociados a la velocidad de fotogramas. La descompresión de un fragmento de datos puede tardar mucho menos que un fotograma o puede llevar muchos fotogramas. Incluso es posible que no sea necesario ejecutar la simulación de tela y pelo exactamente en la velocidad de fotogramas, ya que es posible que las actualizaciones menos frecuentes sean bastante aceptables. Por lo tanto, estos tres subprocesos necesitan estructuras de datos diferentes para comunicarse con el subproceso de actualización y el subproceso de representación. Cada una de ellas necesita una cola de entrada que puede contener solicitudes de trabajo y el subproceso de representación necesita una cola de datos que pueda contener los resultados generados por los subprocesos. Al final de cada fotograma, el subproceso de actualización agregará un bloque de solicitudes de trabajo a las colas de subprocesos de trabajo. La adición a la lista solo una vez por fotograma garantiza que el subproceso de actualización minimice la sobrecarga de sincronización. Cada uno de los subprocesos de trabajo extrae las asignaciones de la cola de trabajo lo más rápido posible, mediante un bucle que tiene un aspecto similar al siguiente:


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

Un diseño alternativo sería tener varios subprocesos de trabajo que dibujan desde la misma cola de trabajo. Esto daría un equilibrio de carga automático y haría más probable que todos los subprocesos de trabajo estuvieran ocupados.

El subproceso de actualización del juego debe tener cuidado de no dar demasiado trabajo a los subprocesos de trabajo o, de lo contrario, las colas de trabajo pueden crecer continuamente. La forma en que el subproceso de actualización administra esto depende del tipo de tareas que realicen los subprocesos de trabajo.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Multithreading simultáneo y número de subprocesos

Todos los subprocesos no se crean igual. Dos subprocesos de hardware pueden estar en chips independientes, en el mismo chip o incluso en el mismo núcleo. La configuración más importante para que los programadores de juegos conozcan es dos subprocesos de hardware en un núcleo: tecnología multithreading (SMT) simultánea o tecnología de Hyper-Threading (tecnología HT).

Los subprocesos de la tecnología SMT o HT comparten los recursos del núcleo de CPU. Dado que comparten las unidades de ejecución, la velocidad máxima desde la ejecución de dos subprocesos en lugar de uno suele ser de 10 a 20 por ciento, en lugar del 100 por ciento que es posible desde dos subprocesos de hardware independientes.

Los subprocesos más importantes de la tecnología SMT o HT comparten la instrucción L1 y las cachés de datos. Si sus patrones de acceso a memoria son incompatibles, pueden acabar luchando en la memoria caché y producir muchos errores de caché. En el peor de los casos, el rendimiento total del núcleo de CPU se puede reducir realmente cuando se ejecuta un segundo subproceso. En Xbox 360, se trata de un problema bastante sencillo. La configuración de la consola Xbox 360 es conocida: tres núcleos de CPU, cada uno con dos subprocesos de hardware, y los desarrolladores asignan los subprocesos de software a subprocesos de CPU específicos y pueden medir para ver si su diseño de subprocesos les proporciona un rendimiento adicional.

En Windows, la situación es más complicada. El número de subprocesos y su configuración variarán de un equipo a un equipo, y la determinación de la configuración es complicada. La función [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) proporciona información acerca de la relación entre distintos subprocesos de hardware, y esta función está disponible en Windows Vista, Windows 7 y Windows XP SP3. Por lo tanto, por ahora tiene que usar la instrucción CPUID y los algoritmos proporcionados por Intel y AMD para decidir el número de subprocesos "reales" que tiene disponibles. Vea las referencias para obtener más información.

El ejemplo CoreDetection en el SDK de DirectX contiene código de ejemplo que usa la función [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) o la instrucción CPUID para devolver la topología de núcleo de CPU. La instrucción CPUID se utiliza si **GetLogicalProcessorInformation** no se admite en la plataforma actual. CoreDetection se puede encontrar en las siguientes ubicaciones:

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Fuentes
</dt> <dd>

Raíz del SDK de *DirectX* \\ Ejemplos de \\ C++ \\ varios \\ CoreDetection

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Ejecutable
</dt> <dd>

Raíz del SDK de *DirectX* \\ Ejemplos deCoreDetection.exe de \\ C++ \\ Misc \\ \\

</dd> </dl>

La suposición más segura es que no haya más de un subproceso con un uso intensivo de la CPU por núcleo de CPU. Tener más subprocesos con un uso intensivo de la CPU que los núcleos de CPU ofrece poca o ninguna ventaja, y aporta la sobrecarga y complejidad adicionales de los subprocesos adicionales.

## <a name="creating-threads"></a>Crear subprocesos

La creación de subprocesos es una operación bastante sencilla, pero hay muchos errores posibles. En el código siguiente se muestra la forma adecuada de crear un subproceso, esperar a que finalice y, a continuación, limpiar.


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



Al crear un subproceso, tiene la opción de especificar el tamaño de la pila para el subproceso secundario, o bien especificar cero, en cuyo caso el subproceso secundario heredará el tamaño de la pila del subproceso primario. En la consola Xbox 360, donde las pilas están confirmadas totalmente cuando se inicia el subproceso, si se especifica cero, se puede desperdiciar una cantidad considerable de memoria, ya que muchos subprocesos secundarios no necesitarán tanta pila como el elemento primario. En Xbox 360 también es importante que el tamaño de la pila sea un múltiplo de 64 KB.

Si usa la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para crear subprocesos, el tiempo de ejecución de C/C++ (CRT) no se inicializará correctamente en Windows. En su lugar, se recomienda usar la función [**\_ BEGINTHREADEX**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) de CRT.

El valor devuelto de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) es un identificador de subproceso. Este subproceso se puede usar para esperar a que el subproceso secundario finalice, lo que es mucho más sencillo y mucho más eficaz que girar en un bucle que comprueba el estado del subproceso. Para esperar a que el subproceso finalice, simplemente llame a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) con el identificador del subproceso.

Los recursos para el subproceso no se liberarán hasta que el subproceso haya finalizado y se haya cerrado el identificador del subproceso. Por lo tanto, es importante cerrar el identificador del subproceso con [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) cuando haya terminado. Si va a esperar a que el subproceso termine con [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), asegúrese de no cerrar el identificador hasta después de que se haya completado la espera.

En Xbox 360, debe asignar de forma explícita los subprocesos de software a un subproceso de hardware determinado mediante **XSetThreadProcessor**. De lo contrario, todos los subprocesos secundarios permanecerán en el mismo subproceso de hardware que el elemento primario. En Windows, puede usar [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) para recomendar al sistema operativo en qué subprocesos de hardware se debe ejecutar el subproceso. Por lo general, esta técnica debe evitarse en Windows, ya que no sabe qué otros procesos podrían estar en ejecución en el sistema. Normalmente es mejor permitir que el programador de Windows asigne los subprocesos a los subprocesos de hardware inactivos.

La creación de subprocesos es una operación costosa. Los subprocesos deben crearse y destruirse con poca frecuencia. Si desea crear y destruir subprocesos con frecuencia, use un grupo de subprocesos que esperan trabajo en su lugar.

## <a name="synchronizing-threads"></a>Sincronizar subprocesos

Para que varios subprocesos funcionen juntos, debe ser capaz de sincronizar los subprocesos, pasar mensajes y solicitar acceso exclusivo a los recursos. Windows y Xbox 360 disponen de un amplio conjunto de primitivas de sincronización. Para obtener detalles completos sobre estas primitivas de sincronización, consulte la documentación de la plataforma.

### <a name="exclusive-access"></a>Acceso exclusivo

Obtener acceso exclusivo a un recurso, una estructura de datos o una ruta de código es una necesidad común. Una opción para obtener acceso exclusivo es una exclusión mutua, cuyo uso típico se muestra aquí.


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

### <a name="events"></a>Events

Si dos subprocesos (quizás un subproceso de actualización y un subproceso de representación) toman turnos usando un par de búferes de descripción de representación, necesitan una manera de indicar cuándo se realizan con su búfer determinado. Esto puede realizarse asociando un evento (asignado con [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) con cada búfer. Cuando un subproceso se realiza con un búfer, puede usar [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) para indicar Esto y, a continuación, puede llamar a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) en el evento de otro búfer. Esta técnica extrapola con facilidad al almacenamiento en búfer triple de los recursos.

### <a name="semaphores"></a>Semáforos

Un semáforo se utiliza para controlar el número de subprocesos que se pueden ejecutar y se utiliza normalmente para implementar colas de trabajo. Un subproceso agrega trabajo a una cola y usa [**ReleaseSemaphore (**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) cada vez que agrega un nuevo elemento a la cola. Esto permite liberar un subproceso de trabajo del grupo de subprocesos en espera. Los subprocesos de trabajo simplemente llaman a [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)y cuando devuelven que saben que hay un elemento de trabajo en la cola para ellos. Además, se debe usar una sección crítica u otra técnica de sincronización para garantizar el acceso seguro a la cola de trabajo compartida.

### <a name="avoid-suspendthread"></a>Evitar SuspendThread

A veces, cuando desea que un subproceso detenga lo que está haciendo, es tentador usar [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) en lugar de los primitivos de sincronización correctos. Esta es siempre mala idea y puede conducir fácilmente a interbloqueos y otros problemas. **SuspendThread** también interactúa incorrectamente con el depurador de Visual Studio. Evite **SuspendThread**. En su lugar, use [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) .

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject y WaitForMultipleObjects

La función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) es la función de sincronización que se usa con más frecuencia. Sin embargo, a veces desea que un subproceso espere hasta que se cumplan varias condiciones simultáneamente o hasta que se cumpla una de las condiciones. En este caso, debe usar [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

### <a name="interlocked-functions-and-lockless-programming"></a>Funciones interbloqueadas y programación de bloqueos

Existe una familia de funciones para realizar operaciones sencillas seguras para subprocesos sin usar bloqueos. Se trata de la familia de funciones entrelazada, como [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement). Estas funciones, además de otras técnicas con una configuración cuidadosa de marcas, se conocen como programación no bloqueada. La programación con bloqueo puede ser muy difícil de hacer correctamente y es mucho más difícil en Xbox 360 que en Windows.

Para obtener más información sobre la programación sin bloqueos, consulte consideraciones sobre la [programación sin bloqueos para Xbox 360 y Microsoft Windows](./lockless-programming.md).

### <a name="minimizing-synchronization"></a>Minimizar la sincronización

Algunos métodos de sincronización son más rápidos que otros. Sin embargo, en lugar de optimizar el código mediante la elección de las técnicas de sincronización más rápidas posibles, suele ser mejor sincronizar con menos frecuencia. Esto es más rápido que la sincronización con demasiada frecuencia y hace que sea más fácil de depurar código más sencillo.

Algunas operaciones, como la asignación de memoria, pueden tener que usar primitivas de sincronización para que funcionen correctamente. Por lo tanto, el hecho de realizar asignaciones frecuentes desde el montón compartido predeterminado producirá una sincronización frecuente, lo que eliminará algún rendimiento. Evitar las asignaciones frecuentes o el uso de montones por subproceso (mediante \_ el montón no \_ SERIALIZE si usa HeapCreate) puede evitar esta sincronización oculta.

Otra causa de la sincronización oculta es D3DCREATE \_ MULTIthreaded, lo que hace que D3D en Windows use la sincronización en muchas operaciones. (La marca se omite en la consola Xbox 360).

Los datos por subproceso, también conocidos como almacenamiento local de subprocesos, pueden ser una forma importante de evitar la sincronización. Visual C++ permite declarar variables globales como por subproceso con la sintaxis de **\_ \_ declspec (Thread)** .


```C++
__declspec( thread ) int tls_i = 1;
```



Esto proporciona a cada subproceso del proceso su propia copia de TLS \_ i, a la que se puede hacer referencia de forma segura y eficaz sin necesidad de sincronización.

La técnica **\_ \_ declspec (Thread)** no funciona con archivos dll cargados dinámicamente. Si usa archivos dll cargados dinámicamente, tendrá que usar la familia de funciones TLSAlloc para implementar el almacenamiento local de subprocesos.

## <a name="destroying-threads"></a>Destruir subprocesos

La única manera segura de destruir un subproceso es hacer que el propio subproceso salga, ya sea devolviendo desde la función de subproceso principal o haciendo que el subproceso llame a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx). Si se crea un subproceso con [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), debe usar **\_ endthreadex** o volver de la función de subproceso principal, ya que el uso de **ExitThread** no liberará correctamente los recursos de CRT. Nunca llame a la función [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) , porque el subproceso no se limpiará correctamente. Los subprocesos siempre deben confirmar Suicide; nunca deben ser murdered.

## <a name="openmp"></a>OpenMP

OpenMP es una extensión de lenguaje para agregar multithreading al programa mediante el uso de pragmas para guiar al compilador en ejecutar bucles en paralelo. OpenMP es compatible con Visual C++ 2005 en Windows y Xbox 360 y se puede usar junto con la administración de subprocesos manual. OpenMP puede ser una manera cómoda de subprocesos de parte del código, pero no es probable que sea la solución ideal, especialmente en el caso de juegos. OpenMP puede ser más aplicable a tareas de producción de ejecución más prolongada, como el procesamiento de material gráfico y otros recursos. Para obtener más información, consulte la documentación de Visual C++ o vaya al [sitio web](https://www.openmp.org/)de OpenMP.

## <a name="profiling"></a>Generación de perfiles

La generación de perfiles multiproceso es importante. Es fácil terminar con paradas largas en las que los subprocesos están esperando entre sí. Estas paradas pueden ser difíciles de encontrar y diagnosticar. Para ayudar a identificarlos, considere la posibilidad de agregar instrumentación a las llamadas de sincronización. Un generador de perfiles de muestreo también puede ayudar a identificar estos problemas, ya que puede registrar información de temporización sin modificarlo sustancialmente.

## <a name="timing"></a>Control de tiempo

La instrucción RDTSC es una manera de obtener información de tiempo precisa en Windows. Desafortunadamente, RDTSC tiene varios problemas que lo convierten en una buena opción para su título de envío. Los contadores de RDTSC no se sincronizan necesariamente entre las CPU, por lo que cuando el subproceso se mueve entre subprocesos de hardware, puede obtener grandes diferencias positivas o negativas. En función de la configuración de administración de energía, la frecuencia con la que se incrementa el contador de RDTSC también puede cambiar mientras se ejecuta el juego. Para evitar estas dificultades, debe preferir [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para la temporización de alta precisión en el juego de envío. Para obtener más información sobre el tiempo, vea [procesadores de control de tiempo y multinúcleo](./game-timing-and-multicore-processors.md).

## <a name="debugging"></a>Depuración

Visual Studio es totalmente compatible con la depuración multiproceso para Windows y Xbox 360. La ventana subprocesos de Visual Studio permite cambiar entre subprocesos para ver las diferentes pilas de llamadas y variables locales. La ventana subprocesos también permite inmovilizar y reanudar subprocesos concretos.

En Xbox 360, puede usar la metavariable **\@ hwthread** en la ventana Inspección para mostrar el subproceso de hardware en el que se está ejecutando el subproceso de software seleccionado actualmente.

La ventana subprocesos es más fácil de usar si se denominan los subprocesos de forma significativa. Visual Studio y otros depuradores de Microsoft le permiten asignar nombres a los subprocesos. Implemente la siguiente función **SetThreadName** y llámela desde cada subproceso a medida que se inicia.


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

La programación multiproceso puede ser complicada y algunos errores multiproceso solo se muestran con poca frecuencia, lo que dificulta la búsqueda y la corrección. Una de las mejores formas de vaciarlas es realizar pruebas en una amplia gama de equipos, especialmente en aquellos con cuatro o más procesadores. El código multiproceso que funciona perfectamente en un equipo con un solo subproceso puede producir un error al instante en un equipo con cuatro procesadores. Las características de rendimiento y temporización de las CPU AMD e Intel pueden variar considerablemente, por lo que debe asegurarse de realizar pruebas en equipos con varios procesadores basados en CPU de ambos proveedores.

## <a name="windows-vista-and-windows-7-improvements"></a>Mejoras en Windows Vista y Windows 7

En el caso de los juegos que tienen como destino las versiones más recientes de Windows, hay una serie de API que pueden simplificar la creación de aplicaciones multiproceso escalables. Esto es especialmente cierto con la nueva API ThreadPool y algunas primitivas syncrhonziation adicionales (variables de condición, el bloqueo ligero de lectura/escritura y una inicialización única). Puede encontrar información general sobre estas tecnologías en los siguientes artículos de MSDN Magazine:

-   [Mejorar la escalabilidad con las nuevas API de grupo de subprocesos](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Primitivas de sincronización nuevas en Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Las aplicaciones que usan [las características de Direct3D 11](../direct3d11/direct3d-11-features.md) en estos sistemas operativos también pueden aprovechar las ventajas del nuevo diseño para la creación de objetos simultáneos y las listas de comandos de contexto diferidos para una mejor escalabilidad para la representación multiproceso.

## <a name="summary"></a>Resumen

Con un diseño cuidadoso que minimiza las interacciones entre los subprocesos, puede obtener mejoras de rendimiento importantes de la programación multiproceso sin agregar una complejidad excesiva al código. Esto permitirá que el código de juego se ponga en marcha la siguiente ola de mejoras del procesador y ofrezca experiencias de juego cada vez más atractivas.

## <a name="references"></a>Referencias

-   Jim Beveridge & Robert Weiner, *aplicaciones multithreading en Win32*, Addison-Wesley, 1997
-   Chuck Walbourn, [procesadores de temporización y varios núcleos](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   Biblioteca de MSDN: [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 