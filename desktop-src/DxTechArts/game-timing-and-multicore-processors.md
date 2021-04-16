---
title: Control del tiempo de juego y procesadores de varios núcleos
description: En este artículo se sugiere una solución más precisa y confiable para obtener intervalos de CPU de alta resolución mediante las API de Windows QueryPerformanceCounter y QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5c511f558b59e94945e63c44db225f34ac2583
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685752"
---
# <a name="game-timing-and-multicore-processors"></a>Control del tiempo de juego y procesadores de varios núcleos

Con las tecnologías de administración de energía cada vez más habituales en los equipos de hoy en día, un método que se usa con frecuencia para obtener intervalos de CPU de alta resolución, la instrucción RDTSC, ya no funcionará según lo esperado. En este artículo se sugiere una solución más precisa y confiable para obtener intervalos de CPU de alta resolución mediante las API de Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Información preliminar](#background)
-   [Recomendaciones](#recommendations)
-   [Compatibilidad de aplicaciones](#application-compatibility)

## <a name="background"></a>Información previa

Desde la introducción del conjunto de instrucciones del P5 x86, muchos desarrolladores de juegos han utilizado el contador de marca de tiempo de lectura, la instrucción RDTSC, para realizar un tiempo de alta resolución. Los temporizadores multimedia de Windows son lo suficientemente precisos para el procesamiento de audio y vídeo, pero con tiempos de fotogramas de una docena de milisegundos o menos, no tienen suficiente resolución para proporcionar información de tiempo de diferencia. Muchos juegos siguen usando un temporizador multimedia en el inicio para establecer la frecuencia de la CPU y usan ese valor de frecuencia para escalar los resultados de RDTSC para obtener un tiempo preciso. Debido a las limitaciones de RDTSC, la API de Windows expone la manera más adecuada de acceder a esta funcionalidad a través de las rutinas de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Este uso de RDTSC para el tiempo se ve afectado por estos problemas fundamentales:

-   Valores discontinuos. El uso directo de RDTSC supone que el subproceso siempre se ejecuta en el mismo procesador. Los sistemas multiprocesador y de doble núcleo no garantizan la sincronización de sus contadores de ciclo entre núcleos. Esto se agrava al combinarse con tecnologías modernas de administración de energía que inactivan y restauran varios núcleos en momentos diferentes, lo que provoca que los núcleos no estén sincronizados. En el caso de una aplicación, esto suele dar lugar a errores o a posibles bloqueos, ya que el subproceso salta entre los procesadores y obtiene los valores de tiempo que dan como resultado diferencias grandes, diferencias negativas o tiempo de parada.
-   Disponibilidad de hardware dedicado. RDTSC bloquea la información de tiempo que la aplicación solicita al contador de ciclo del procesador. Durante muchos años, esta era la mejor manera de obtener información de tiempo de alta precisión, pero ahora las motherboards más recientes incluyen dispositivos de control de tiempo dedicados que proporcionan información de tiempo de alta resolución sin las desventajas de RDTSC.
-   Variabilidad de la frecuencia de la CPU. Se suele hacer que la frecuencia de la CPU sea fija para la vida del programa. Sin embargo, con las modernas tecnologías de administración de energía, es una suposición incorrecta. Aunque se limita inicialmente a equipos portátiles y otros dispositivos móviles, la tecnología que cambia la frecuencia de la CPU está en uso en muchos equipos de escritorio de alta gama. generalmente, la deshabilitación de su función para mantener una frecuencia coherente no es aceptable para los usuarios.

## <a name="recommendations"></a>Recomendaciones

Los juegos necesitan información precisa sobre el tiempo, pero también debe implementar el código de control de tiempo de forma que se eviten los problemas asociados con el uso de RDTSC. Cuando implemente el control de tiempo de alta resolución, realice los pasos siguientes:

1.  Use [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) en lugar de RDTSC. Estas API pueden usar RDTSC, pero en su lugar pueden usar dispositivos de control de tiempo en la placa base o en otros servicios de sistema que proporcionen información de tiempo de alta resolución de alta calidad. Aunque RDTSC es mucho más rápido que **QueryPerformanceCounter**, dado que la segunda es una llamada API, es una API que se puede llamar varias veces por fotograma sin ningún impacto perceptible. (Sin embargo, los desarrolladores deben intentar hacer que los juegos llamen a **QueryPerformanceCounter** lo menos posible para evitar cualquier penalización del rendimiento).
2.  Al calcular deltas, los valores se deben fijar para asegurarse de que los errores en los valores de tiempo no causan bloqueos ni cálculos relacionados con el tiempo inestables. El intervalo de Clamp debe ser de 0 (para evitar valores Delta negativos) a un valor razonable basado en la velocidad de fotogramas más baja esperada. Es probable que la compresión sea útil en cualquier depuración de la aplicación, pero asegúrese de tenerlo en cuenta si realiza el análisis de rendimiento o ejecuta el juego en algún modo no optimizado.
3.  Calcule todo el tiempo en un solo subproceso. El cálculo de temporización en varios subprocesos (por ejemplo, con cada subproceso asociado a un procesador específico) reduce en gran medida el rendimiento de los sistemas de varios núcleos.
4.  Establezca que un único subproceso permanezca en un solo procesador mediante la API de Windows [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). Normalmente, este es el subproceso principal del juego. Aunque [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) normalmente se ajustan para varios procesadores, los errores en el BIOS o los controladores pueden dar lugar a que estas rutinas devuelvan valores diferentes a medida que el subproceso se mueve de un procesador a otro. Por lo tanto, es mejor mantener el subproceso en un solo procesador.

    Todos los demás subprocesos deben funcionar sin recopilar sus propios datos del temporizador. No se recomienda usar un subproceso de trabajo para calcular el tiempo, ya que esto se convertirá en un cuello de botella de sincronización. En su lugar, los subprocesos de trabajo deben leer las marcas de tiempo del subproceso principal y, como los subprocesos de trabajo solo leen las marcas de tiempo, no es necesario usar secciones críticas.

5.  Llame a [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) solo una vez, ya que la frecuencia no cambiará mientras el sistema se esté ejecutando.

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

Muchos desarrolladores han realizado suposiciones sobre el comportamiento de RDTSC en varios años, por lo que es bastante probable que algunas aplicaciones existentes muestren problemas cuando se ejecutan en un sistema con varios procesadores o núcleos debido a la implementación de temporización. Normalmente, estos problemas se manifiestan como problemas o movimientos de movimiento lento. No hay ninguna solución fácil para las aplicaciones que no son conscientes de la administración de energía, pero existe una corrección de compatibilidad (shim) existente para forzar que una aplicación se ejecute siempre en un solo procesador en un sistema de varios procesadores.

Para crear esta corrección de compatibilidad, descargue el kit de herramientas de compatibilidad de aplicaciones de Microsoft de [compatibilidad de aplicaciones de Windows](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

Mediante el administrador de compatibilidad, parte del kit de herramientas, cree una base de datos de la aplicación y correcciones asociadas. Cree un nuevo modo de compatibilidad para esta base de datos y seleccione el **SingleProcAffinity** de corrección de compatibilidad para forzar que todos los subprocesos de la aplicación se ejecuten en un solo procesador o núcleo. Mediante el uso de la herramienta de línea de comandos Fixpack.exe (también parte del kit de herramientas), puede convertir esta base de datos en un paquete instalable para la instalación, prueba y distribución.

Para obtener instrucciones sobre cómo usar el administrador de compatibilidad, vea la documentación del kit de herramientas. Para obtener sintaxis y ejemplos de uso de Fixpack.exe, consulte la ayuda de la línea de comandos.

Para obtener información orientada a clientes, vea los siguientes artículos de Knowledge base de ayuda y soporte técnico de Microsoft:

-   [Los programas que el usuario de la función QueryPerformanceCounter pueden tener un rendimiento bajo en Windows Server 2003 y en Windows XP](https://support.microsoft.com/kb/895980) (artículo 895980)
-   Es [posible que el rendimiento del juego sea deficiente en un equipo basado en Windows XP que use un procesador de doble núcleo](https://support.microsoft.com/kb/909944) (artículo 909944).

 

 