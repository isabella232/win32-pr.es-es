---
title: Principales problemas de los títulos de Windows
description: En este artículo se resaltan muchos de los problemas comunes que se han visto en los juegos de PC de la generación actual.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547c977f7d8e4895ef73ba229a9012854a7c6d27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665861"
---
# <a name="top-issues-for-windows-titles"></a>Principales problemas de los títulos de Windows

El grupo de relaciones para desarrolladores de tecnologías de juegos y gráficos de Microsoft Windows realiza el análisis de rendimiento de muchos juegos de Windows cada año. Durante estas sesiones, obtenemos experiencia práctica para relacionar los comentarios de los desarrolladores y las consultas que recibimos diariamente. En ocasiones, le ayudamos a realizar un seguimiento de un bloqueo misterioso u otro problema en un título, que nos proporciona más información sobre los problemas que se encuentran en los desarrolladores.

En este artículo se resaltan muchos de los problemas comunes que se han visto en los juegos de PC de la generación actual.

-   [Rendimiento limitado por CPU](#cpu-limited-performance)
-   [Administración de lotes deficiente](#poor-batch-management)
-   [Copia excesiva de memoria](#excessive-memory-copying)
-   [Uso excesivo del envío dinámico de Draw](#excessive-use-of-dynamic-draw-submission)
-   [Gran sobrecarga en el procesamiento de archivos](#high-overhead-in-file-processing)
-   [Instalación lenta y frustrante](#slow-and-frustrating-installation)
-   [Falta de consideración de la memoria física](#lack-of-consideration-of-physical-memory)
-   [Exceso de dependencia en la conversión de la frecuencia de muestreo de Real-Time audio](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragmentación de la memoria virtual](#fragmention-of-virtual-memory)
-   [Manipulación de la palabra de control Floating-Point](#manipulation-of-the-floating-point-control-word)
-   [Instalación opcional del tiempo de ejecución de DirectX](#optional-installation-of-the-directx-runtime)
-   [Uso excesivo de la sincronización de subprocesos](#excessive-use-of-thread-synchronization)
-   [Uso de RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>Rendimiento de CPU-Limited

La gran mayoría de los juegos están limitados por el rendimiento de la CPU en sistemas con unidades de procesamiento de gráficos (GPU) de alto rendimiento. En ocasiones, esto se debe a un uso deficiente del procesamiento por lotes para el envío de tablas, pero lo más habitual es que otros sistemas de juegos consuman una gran parte de los ciclos de CPU disponibles. En los pocos casos en los que hemos detectado que la GPU es la limitación, la causa es una velocidad de relleno muy alta o una demanda del sombreador de píxeles, en la configuración de alta resolución o en el rendimiento del sombreador de vértices bajo una tarjeta de vídeo.

Dado que la mayoría de los títulos están limitados por la CPU, el mayor rendimiento gana de la optimización de los sistemas de juegos con un uso intensivo de la CPU. Normalmente, los sistemas de inteligencia artificial o de física y la lógica de detección de colisiones asociada son los consumidores principales de los ciclos de la CPU en las aplicaciones de Microsoft Direct3D. Cualquier trabajo para mejorar estos sistemas puede mejorar el rendimiento general del juego.

## <a name="poor-batch-management"></a>Administración de lotes deficiente

Para lograr un buen paralelismo con la GPU, es necesario que los lotes de Draw contengan una geometría suficiente, y que los sombreadores tengan la complejidad adecuada, para mantener la tarjeta de vídeo ocupada, aunque no se use el mismo número de lotes que el búfer de comandos esté inundado. En el hardware de generación actual, se recomiendan aproximadamente 300 o menos envíos de Draw batch por fotograma (menos en CPU de menor rendimiento) para evitar que el procesamiento del controlador del búfer de comandos se convierta en un cuello de botella de rendimiento. Algunas otras llamadas de estado de API y combinaciones de controladores pueden dar lugar a un costo de procesamiento de la CPU (por ejemplo, la compilación de controladores de los sombreadores), por lo que se recomienda encarecidamente un análisis de rendimiento rutinario.

## <a name="excessive-memory-copying"></a>Copia excesiva de memoria

Durante el desarrollo de la mayoría de los títulos de PC, los desarrolladores usan estructuras y cadenas de datos útiles para la administración de contenido. El trabajo de CPU necesario para la comparación de cadenas, la copia y otras manipulaciones a menudo tiene una sobrecarga mensurable, especialmente cuando se tienen en cuenta los resultados de rendimiento asociados a la memoria caché y al subsistema de memoria. Los planes deben realizarse al desarrollar estos sistemas para quitar o minimizar la dependencia del procesamiento de cadenas una vez que el producto entra en las fases principales de pruebas y versiones.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Uso excesivo del envío dinámico de Draw

El hardware de vídeo moderno funciona bien cuando se trabaja con datos estáticos. Los adaptadores de gama alta suelen tener una gran cantidad de memoria de vídeo, pero los datos dinámicos no pueden utilizar esta memoria de forma eficaz.

Aunque se pueden implementar patrones de uso que sean razonablemente eficientes de búferes de vértices dinámicos o búferes de índice para el contenido dinámico, muchos títulos no sobrepasan esta expresión para lo que de otro modo es contenido estático. Lo más frecuente es que esto se vea con árboles de particiones de espacio binario (BSP) y sistemas basados en el portal que almacenan geometría en una estructura de datos que no se asigna al hardware y se deben procesar en búferes para cada fotograma. Poner todo el contenido en los recursos estáticos como sea posible puede reducir en gran medida la sobrecarga de ancho de banda que supone la transferencia de datos a la tarjeta de vídeo, hacer un mejor uso de VRAM incorporada y reducir la sobrecarga de CPU/caché que conlleva el procesamiento de este contenido.

## <a name="high-overhead-in-file-processing"></a>Gran sobrecarga en el procesamiento de archivos

Los juegos de PC han obtenido la reputación de tiempos de carga prolongados, en particular cuando se comparan con los títulos de la consola con requisitos estrictos en tiempo de carga. Nuestro análisis de la forma en que muchos títulos hacen uso del subsistema de archivos revela algunos problemas comunes.

La sobrecarga de abrir un archivo suele ser mucho mayor de lo que los desarrolladores esperan. Con los escáneres de virus a petición en uso generalizado y la funcionalidad adicional de NTFS, la apertura de un archivo es una operación bastante costosa. Abrir muchos archivos al mismo tiempo o abrir y cerrar el mismo archivo repetidamente es, por lo tanto, un método pobre de tratar con la administración de archivos. Algunos juegos han intentado mitigar este costo de rendimiento comprobando la existencia de un archivo antes de abrirlo. La realidad es que comprobar la existencia de un archivo en NTFS requiere abrir el archivo, por lo que realizar pruebas antes de abrir los resultados es pagar el costo dos veces.

Los juegos que permiten modificaciones de complementos, o mods, o que todavía incluyen scaffolding de desarrollo para comprobar los archivos de datos de invalidación, pueden tener retrasos significativos en la carga del juego debido a la comprobación de estos archivos, incluso cuando esos archivos no están presentes. Se recomienda que los juegos solo comprueben estos archivos cuando se ejecuten con un modificador de línea de comandos especial u otro indicador de modo, de modo que solo los usuarios que usan esta funcionalidad paguen realmente el costo de rendimiento de estas comprobaciones (a menudo amplias).

Puede obtener un rendimiento adicional del sistema de archivos de la siguiente manera:

-   Uso apropiado de la marca de archivo de sugerencias de sistema de archivos \_ \_ \_ acceso aleatorio y el \_ \_ examen secuencial del indicador de archivo \_
-   Cambiar el tamaño de los búferes para evitar una gran cantidad de llamadas a las API de lectura y escritura del sistema operativo
-   Obtener acceso a los archivos de forma asincrónica
-   Carga de subprocesos en segundo plano

También recomendamos encarecidamente convertir los datos sin conexión (en el momento de la compilación o la instalación) en lugar de basarse en la conversión cuando el juego se ejecuta por primera vez, ya que esto impone un importante impuesto de rendimiento para todos los usuarios.

## <a name="slow-and-frustrating-installation"></a>Instalación lenta y frustrante

Otro problema común que hemos visto es tiempos de instalación muy largos necesarios para muchos juegos de PC modernos. Los instaladores solicitan al usuario muchas veces, a veces simplemente para indicar al usuario, por ejemplo, "no necesita DirectX instalado". Por lo general, estos instaladores infractores requieren que el usuario seleccione **siguiente** o **Aceptar** muchas veces antes de que se inicie realmente la instalación del juego. Una vez que comience, hemos visto que algunos títulos tardan una hora o más antes de que el usuario obtenga la oportunidad de jugar. Creemos que la primera hora de la experiencia de juego no debe ser la instalación.

Se recomiendan varios enfoques para tratar con la instalación de. En primer lugar, mantenga los mensajes sencillos y como mínimo. En segundo lugar, diseñe los datos del juego de modo que algunos o todos los archivos de datos se puedan usar directamente desde el disco de distribución, siempre que sea posible: las unidades de DVD modernas tienen un ancho de banda muy alto. En tercer lugar, considere la posibilidad de implementar la instalación a petición en sus títulos para reducir o eliminar el proceso de instalación y permitir a los usuarios entrar en el juego lo más rápido posible. (Para obtener más información sobre la instalación a petición, vea [instalación a petición para juegos](/windows/desktop/DxTechArts/install-on-demand-for-games)).

Para obtener más recomendaciones sobre la instalación de juegos, consulte [simplificar la instalación de juegos](/windows/desktop/DxTechArts/simplifying-game-installation).

## <a name="lack-of-consideration-of-physical-memory"></a>Falta de consideración de la memoria física

Debido a la amplia variabilidad del hardware de PC en el mercado, los títulos suelen usar las pruebas de configuración ad hoc para seleccionar la configuración predeterminada para el nivel de detalle gráfico. Algunos de los títulos que hemos visto están usando el tamaño de la memoria de vídeo en estas pruebas, pero no se pueden poner en correlación con el tamaño de la memoria física. Con el fin de controlar las situaciones de dispositivo perdido, la mayor parte de la memoria de vídeo (tanto la VRAM local en la tarjeta como la abertura de memoria AGP no local) debe estar respaldada por la memoria física, ya sea mediante el uso de recursos administrados o estructuras de datos personalizadas. Algunas tarjetas de vídeo de gama alta tienen tamaños de VRAM que tienen un tamaño mayor que el de memorias de CPU de bajo nivel. En situaciones en las que el sistema tiene una memoria física limitada en comparación con la tarjeta de vídeo, la mayor parte de esa VRAM no se puede usar de forma eficaz y se debe configurar una configuración de detalle inferior.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance en Real-Time conversión de velocidad de muestra de audio

Otro origen común de la grabación del ciclo de la CPU que hemos visto tiene lugar cuando se necesita el sistema de audio para convertir la velocidad de reproducción durante la combinación en el búfer de hardware. Con los controladores de Modelo de controlador de Windows (WDM), el formato de búfer de hardware no está bajo el control de aplicaciones directo, ya que se trata de un recurso de nivel de kernel. en su lugar, se selecciona el formato en función del formato de mayor calidad de todos los orígenes y de las capacidades del hardware. De forma predeterminada, Windows XP usa una conversión de velocidad de muestra de alta calidad para este proceso y, si la mayoría de las muestras de audio requiere una conversión de velocidad, se consumirá una parte significativa de los ciclos de la CPU.

Se recomienda crear todos los búferes de DirectSound con la misma velocidad de muestra. Si realiza cualquier uso de las funciones de Microsoft Win32 **WaveOut** , debe usar también una velocidad de muestra coherente. Con los controladores WDM, el kernel combinará todos los búferes y, si usa una frecuencia de muestreo superior en algunos de ellos, se convertirán las velocidades de muestra de todo el resto para que coincidan. Tenga en cuenta que esto implica el uso de la misma velocidad de reproducción para todas las muestras de audio, incluido cualquier búfer de descompresión de audio de streaming. La configuración de la tasa de búfer principal no tiene ningún efecto a menos que el destino sea Windows 98 o Windows Millennium Edition.

> [!Note]  
> En Windows Vista y versiones posteriores del sistema operativo, DirectSound y **WaveOut** usan la [API de sesión de audio de Windows (WASAPI)](/windows/desktop/CoreAudio/wasapi) para todas las salidas de audio.

 

## <a name="fragmention-of-virtual-memory"></a>Fragmentación de la memoria virtual

Hemos visto varios problemas recientes relacionados con el límite de 32 bits en el espacio de memoria de proceso. Aunque 2 GB de espacio de direcciones virtuales para los procesos de modo de usuario ha sido más adecuado históricamente, el mayor uso de archivos asignados a memoria de gran tamaño, asignadores de memoria personalizados y un aumento del tamaño de VRAM (que debe asignarse en el espacio de proceso) ha empezado a producir situaciones en las que se producen errores en las asignaciones de espacio de memoria virtual. Algunos archivos DLL que no son de Microsoft usan ubicaciones de inicio fijo en medio del espacio de direcciones virtuales, lo que provoca la fragmentación que da como resultado asignaciones con errores.

Estos problemas suelen aparecer cuando el juego hace uso de un esquema de asignación de memoria personalizado que intenta asignar un gran fragmento continuo de espacio de memoria virtual. Nuestra recomendación es escribir asignadores de modo que soliciten partes más razonables del espacio de direcciones virtuales según sea necesario. Por ejemplo, al solicitar 64 o 256 MB a la vez, pero no 1 GB. Sin embargo, se debe tener cuidado de no producir más fragmentación. La llegada de los sistemas operativos y el hardware de 64 bits ayudará en gran medida a estos problemas en el futuro, pero debe tener cuidado en los sistemas de 32 bits de generación actual.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipulación de la palabra de control Floating-Point

Como ayuda para la depuración, algunos desarrolladores han habilitado las excepciones en la unidad de punto flotante (FPU) a través de manipulaciones de la palabra de control de punto flotante. Hacer esto es muy problemático y probablemente hará que se bloquee el proceso. Del mismo modo que la Convención de llamada requiere que se conserve el registro EBX, la mayoría del sistema asume que FPU está en un estado predeterminado, proporcionará resultados razonables y no generará excepciones. Los controladores y otros componentes del sistema suelen calcular los resultados en función de la suposición de que los valores de error estándar aparecerán en los registros de condiciones incorrectas, pero si las excepciones están habilitadas, no se controlarán y se producirán bloqueos.

Direct3D establecerá la unidad de punto flotante en una sola precisión y de un extremo a más cercano como parte de la inicialización para el subproceso que realiza la llamada, a menos que se use la marca de D3DCREATE FPU de la \_ \_ función preserve, en cuyo caso no se toca la palabra de control de punto flotante. Dado que la palabra de control es una configuración por subproceso, asegurarse de que todos los subprocesos de la aplicación estén establecidos en el modo de precisión sencilla puede optimizar el rendimiento. Recuerde que la llamada a [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) no es válida para la codificación x64-Native, que usa SSE exclusivamente en su lugar, y es muy costosa en la arquitectura basada en POWERPC de la CPU Xbox 360.

> [!Note]  
> Si modifica la palabra de control, use [**\_ controlfp \_ s**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) y tenga en cuenta que para plataformas x64 no puede cambiar la precisión de punto flotante a través de la palabra de control.

 

En cualquier biblioteca en la que sea necesario tener diferentes reglas de redondeo u otro comportamiento, como el tratamiento de los sombreadores de vértices de software o la compilación, se guarda y se restaura la palabra de control. Si un juego necesita usar excepciones de redondeo o de FPU no estándar, debe guardar y restaurar la palabra de control de punto flotante, y debe asegurarse de que no llama a ningún código externo que no se haya demostrado que sea seguro de estos problemas, incluidas las API del sistema.

## <a name="optional-installation-of-the-directx-runtime"></a>Instalación opcional del tiempo de ejecución de DirectX

Una serie de juegos pregunte al usuario si desea instalar DirectX. Esto puede causar problemas si el usuario asume que el sistema tiene la versión más reciente de DirectX redistribuible instalada, omite la instalación y, posteriormente, la instalación continúa correctamente. Si el juego requiere una versión específica de D3DX, u otra funcionalidad actualizada que no se haya instalado, el juego no funcionará y el usuario se verá muy frustrado.

Se recomienda encarecidamente que el instalador del juego Instale de forma silenciosa el paquete redistribuible de DirectX con el que se compiló el juego. El proceso de instalación de DirectX está diseñado de modo que compruebe si es necesario actualizar algo y devuelve rápidamente si no lo hace. Por lo tanto, no es necesario preguntar al usuario sobre la instalación de DirectX.

Para realizar una instalación silenciosa de DirectX, ejecute este comando desde el paquete de instalación: **dxsetup.exe/Silent**

Además, el tamaño real de la carpeta redistribuible se puede configurar para incluir solo los archivos. cab que realmente se necesitan para las plataformas de destino y el uso del juego.

> [!Note]  
> Antes de usar **DxSetup**, lea [no para la configuración directa](https://walbourn.github.io/).

 

## <a name="excessive-use-of-thread-synchronization"></a>Uso excesivo de la sincronización de subprocesos

Al generar perfiles de juegos, a menudo se encuentran las zonas activas principales relacionadas con la entrada y la salida de secciones críticas. Con la prevalencia de CPU de varios núcleos, el uso de multithreading en los juegos ha aumentado drásticamente y muchas implementaciones se basan en el uso intensivo de la sincronización de subprocesos. El tiempo de CPU para tomar una sección crítica incluso sin contención es bastante significativo y todas las demás formas de sincronización de subprocesos son incluso más costosas. Por lo tanto, debe tener cuidado para minimizar el uso de estas primitivas.

Un origen común de la sincronización excesiva en los juegos es el uso de [D3DCREATE \_ multiproceso](/windows/desktop/direct3d9/d3dcreate). Esta marca, a la vez que se hace seguro para subprocesos de Direct3D para la representación desde varios subprocesos, toma un enfoque muy conservador, lo que produce una sobrecarga de sincronización alta. Los juegos deben evitar esta marca. En su lugar, diseñe el motor para que toda la comunicación con Direct3D sea de un solo subproceso y cualquier comunicación entre subprocesos se controle directamente. Para obtener más información sobre el diseño de juegos multiproceso, consulte el artículo [codificación de varios núcleos en Xbox 360 y Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores).

## <a name="use-of-rdtsc"></a>Uso de RDTSC

No se recomienda el uso de la instrucción **RDTSC** de x86. **RDTSC** no puede calcular correctamente el tiempo en algunos esquemas de administración de energía que cambian la frecuencia de la CPU de forma dinámica y en muchas CPU de varios núcleos para los que el contador de ciclo no está sincronizado entre núcleos. En su lugar, los juegos deben usar la API de [**QueryPerformanceCounter**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) . Para obtener más información acerca de los problemas de **RDTSC** e implementación de tiempos de alta resolución con **QueryPerformanceCounter**, consulte el artículo sobre el [control de tiempo y los procesadores de varios núcleos](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).

 

 