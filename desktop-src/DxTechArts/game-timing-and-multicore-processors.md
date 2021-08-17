---
title: Control del tiempo de juego y procesadores de varios núcleos
description: En este artículo se sugiere una solución más precisa y confiable para obtener intervalos de CPU de alta resolución mediante las API de Windows QueryPerformanceCounter y QueryPerformanceFrequency.
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5e668e87a2645859838b1fdf9cfb35263381e9ce9c73fbe72232ad3d3a46cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649353"
---
# <a name="game-timing-and-multicore-processors"></a>Control del tiempo de juego y procesadores de varios núcleos

Con las tecnologías de administración de energía cada vez más comunes en los equipos actuales, es posible que un método usado habitualmente para obtener tiempos de CPU de alta resolución, la instrucción RDTSC, ya no funcione según lo previsto. En este artículo se sugiere una solución más precisa y confiable para obtener intervalos de CPU de alta resolución mediante las API de Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

-   [Información preliminar](#background)
-   [Recomendaciones](#recommendations)
-   [Compatibilidad de aplicaciones](#application-compatibility)

## <a name="background"></a>Información previa

Desde la introducción del conjunto de instrucciones X86 P5, muchos desarrolladores de juegos han hecho uso del contador de marca de tiempo de lectura, la instrucción RDTSC, para realizar un tiempo de alta resolución. Los temporizadores multimedia Windows son lo suficientemente precisos para el procesamiento de sonido y vídeo, pero con tiempos de fotogramas de una decenas de milisegundos o menos, no tienen una resolución suficiente para proporcionar información en tiempo delta. Muchos juegos siguen utilizando un temporizador multimedia en el inicio para establecer la frecuencia de la CPU y usan ese valor de frecuencia para escalar los resultados de RDTSC para obtener una hora precisa. Debido a las limitaciones de RDTSC, la API de Windows expone la manera más correcta de acceder a esta funcionalidad a través de las rutinas [**de QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

Este uso de RDTSC para el control de tiempo sufre estos problemas fundamentales:

-   Valores discontinuos. El uso directo de RDTSC supone que el subproceso siempre se ejecuta en el mismo procesador. Los sistemas de varios procesadores y de doble núcleo no garantizan la sincronización de sus contadores de ciclo entre núcleos. Esto se agrava cuando se combina con tecnologías modernas de administración de energía que inactivan y restauran varios núcleos en distintos momentos, lo que suele hacer que los núcleos no se sincronizarán. En el caso de una aplicación, esto suele producir problemas o posibles bloqueos a medida que el subproceso salta entre los procesadores y obtiene valores de tiempo que resultan en diferencias grandes, diferencias negativas o tiempo detenido.
-   Disponibilidad de hardware dedicado. RDTSC bloquea la información de control de tiempo que la aplicación solicita al contador de ciclos del procesador. Durante muchos años, esta era la mejor manera de obtener información de control de tiempo de alta precisión, pero ahora las placas base más recientes incluyen dispositivos de control de tiempo dedicados que proporcionan información de control de tiempo de alta resolución sin los inconvenientes de RDTSC.
-   Variabilidad de la frecuencia de la CPU. A menudo se supone que la frecuencia de la CPU se fija durante la vida del programa. Sin embargo, con las tecnologías modernas de administración de energía, se trata de una suposición incorrecta. Aunque inicialmente se limita a equipos portátiles y otros dispositivos móviles, la tecnología que cambia la frecuencia de la CPU está en uso en muchos equipos de escritorio de gama alta. Deshabilitar su función para mantener una frecuencia coherente no suele ser aceptable para los usuarios.

## <a name="recommendations"></a>Recomendaciones

Los juegos necesitan información de control de tiempo precisa, pero también debe implementar código de control de tiempo de una manera que evite los problemas asociados con el uso de RDTSC. Al implementar el tiempo de alta resolución, siga estos pasos:

1.  Use [**QueryPerformanceCounter y**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) [**QueryPerformanceFrequency en**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) lugar de RDTSC. Estas API pueden usar RDTSC, pero en su lugar pueden usar dispositivos de control de tiempo en la placa base o en otros servicios del sistema que proporcionan información de control de tiempo de alta resolución de alta calidad. Aunque RDTSC es mucho más rápido que **QueryPerformanceCounter**, puesto que este último es una llamada API, es una API a la que se puede llamar varios cientos de veces por fotograma sin ningún impacto perceptible. (No obstante, los desarrolladores deben intentar que sus juegos llamen a **QueryPerformanceCounter** lo menos posible para evitar cualquier penalización de rendimiento).
2.  Al calcular las diferencias, los valores deben fijarse para asegurarse de que los errores en los valores de control de tiempo no provocan bloqueos ni cálculos inestables relacionados con el tiempo. El intervalo de fijación debe ser de 0 (para evitar valores diferenciales negativos) a algún valor razonable en función de la velocidad de fotogramas más baja esperada. Es probable que la fijación sea útil en cualquier depuración de la aplicación, pero asegúrese de tenerla en cuenta si está realizando análisis de rendimiento o ejecutando el juego en algún modo no óptimo.
3.  Calcular todos los tiempos en un único subproceso. El cálculo del tiempo en varios subprocesos (por ejemplo, con cada subproceso asociado a un procesador específico) reduce en gran medida el rendimiento de los sistemas de varios núcleos.
4.  Establezca ese subproceso único para que permanezca en un solo procesador mediante el Windows API [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask). Normalmente, este es el subproceso principal del juego. Aunque [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) y [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) suelen ajustarse para varios procesadores, los errores en el BIOS o los controladores pueden dar lugar a que estas rutinas devuelvan valores diferentes a medida que el subproceso se mueve de un procesador a otro. Por lo tanto, es mejor mantener el subproceso en un solo procesador.

    Todos los demás subprocesos deben funcionar sin recopilar sus propios datos de temporizador. No se recomienda usar un subproceso de trabajo para calcular el tiempo, ya que se convertirá en un cuello de botella de sincronización. En su lugar, los subprocesos de trabajo deben leer las marcas de tiempo del subproceso principal y, dado que los subprocesos de trabajo solo leen marcas de tiempo, no es necesario usar secciones críticas.

5.  Llame [**a QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) solo una vez, ya que la frecuencia no cambiará mientras el sistema se esté ejecutando.

## <a name="application-compatibility"></a>Compatibilidad de aplicaciones

Muchos desarrolladores han realizado suposiciones sobre el comportamiento de RDTSC durante muchos años, por lo que es bastante probable que algunas aplicaciones existentes presenten problemas al ejecutarse en un sistema con varios procesadores o núcleos debido a la implementación de tiempo. Estos problemas normalmente se manifiestan como problemas o movimiento de movimiento lento. No hay ninguna solución fácil para las aplicaciones que no son conscientes de la administración de energía, pero hay una corrección de compatibilidad (shim) existente para forzar que una aplicación se ejecute siempre en un único procesador en un sistema de varios procesadores.

Para crear esta corrección de compatibilidad, descargue la compatibilidad de aplicaciones de Microsoft Toolkit desde [Windows Compatibilidad de aplicaciones](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10).

Con el administrador de compatibilidad, que forma parte del kit de herramientas, cree una base de datos de la aplicación y las correcciones asociadas. Cree un nuevo modo de compatibilidad para esta base de datos y seleccione la corrección de compatibilidad **SingleProcAffinity** para forzar que todos los subprocesos de la aplicación se ejecuten en un solo procesador o núcleo. Mediante el uso de la herramienta de línea de comandos Fixpack.exe (también parte del kit de herramientas), puede convertir esta base de datos en un paquete instalable para la instalación, las pruebas y la distribución.

Para obtener instrucciones sobre el uso del administrador de compatibilidad, consulte la documentación del kit de herramientas. Para obtener sintaxis de y ejemplos de Fixpack.exe, vea su ayuda de la línea de comandos.

Para obtener información orientada al cliente, consulte los siguientes artículos knowledge base ayuda y soporte técnico de Microsoft:

-   Los programas que usan la función [QueryPerformanceCounter](https://support.microsoft.com/kb/895980) pueden funcionar mal en Windows Server 2003 y en Windows XP (artículo 895980)
-   [El rendimiento del juego puede ser deficiente en un Windows](https://support.microsoft.com/kb/909944) basado en XP que usa un procesador de doble núcleo (artículo 909944)

 

 
