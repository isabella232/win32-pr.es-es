---
title: Principales problemas de Windows títulos
description: En este artículo se resaltan muchos de los problemas comunes que hemos visto en los juegos de PC de generación actual.
ms.assetid: 89b83473-1aa9-9a2d-8778-15cfb91cdea4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89be8ad7a68c247d589f304ea77fa9b3e63e105739264e39f71794c705b66cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396510"
---
# <a name="top-issues-for-windows-titles"></a>Principales problemas de Windows títulos

El grupo microsoft Windows relaciones de desarrollador de tecnologías de gráficos y juegos realiza un análisis del rendimiento de muchos Windows juegos cada año. Durante estas sesiones, se obtiene experiencia práctica para vincularnos a los comentarios y las consultas del desarrollador que recibimos a diario. En ocasiones, ayudaremos a realizar un seguimiento de un bloqueo incoocuado u otro problema en un título, lo que nos proporciona más información sobre los problemas que encuentran los desarrolladores.

En este artículo se resaltan muchos de los problemas comunes que hemos visto en los juegos de PC de generación actual.

-   [Rendimiento limitado de CPU](#cpu-limited-performance)
-   [Administración deficiente de lotes](#poor-batch-management)
-   [Copia excesiva de memoria](#excessive-memory-copying)
-   [Uso excesivo del envío de dibujo dinámico](#excessive-use-of-dynamic-draw-submission)
-   [Sobrecarga alta en el procesamiento de archivos](#high-overhead-in-file-processing)
-   [Instalación lenta y frustrante](#slow-and-frustrating-installation)
-   [Falta de consideración de la memoria física](#lack-of-consideration-of-physical-memory)
-   [Dependencia excesiva de la conversión Real-Time frecuencia de muestreo de audio](#over-reliance-on-real-time-audio-sample-rate-conversion)
-   [Fragmentación de memoria virtual](#fragmention-of-virtual-memory)
-   [Manipulación de la palabra Floating-Point control](#manipulation-of-the-floating-point-control-word)
-   [Instalación opcional del entorno de ejecución de DirectX](#optional-installation-of-the-directx-runtime)
-   [Uso excesivo de la sincronización de subprocesos](#excessive-use-of-thread-synchronization)
-   [Uso de RDTSC](#use-of-rdtsc)

## <a name="cpu-limited-performance"></a>CPU-Limited rendimiento

La gran mayoría de los juegos están limitados por el rendimiento de la CPU en sistemas con unidades de procesamiento gráfico (GPU) de alto rendimiento. Esto se debe a veces a un uso deficiente del procesamiento por lotes para envíos de draw, pero lo más habitual es que esto se deba a que otros sistemas de juegos consumen una gran parte de los ciclos de CPU disponibles. En los pocos casos en los que hemos visto la GPU como la limitación, la causa es una tasa de relleno muy alta o una demanda de sombreador de píxeles, en la configuración de alta resolución o un bajo rendimiento del sombreador de vértices mediante una tarjeta de vídeo.

Dado que la mayoría de los títulos están limitados por CPU, las mayores ganancias de rendimiento proceden de la optimización de sistemas de juegos con un uso intensivo de CPU. Normalmente, los sistemas de inteligencia artificial o física y la lógica de detección de colisiones asociada son los consumidores principales de los ciclos de CPU en aplicaciones de Microsoft Direct3D que se comportan bien. Cualquier trabajo para mejorar estos sistemas puede mejorar el rendimiento general del juego.

## <a name="poor-batch-management"></a>Administración deficiente de lotes

Lograr un buen paralelismo con la GPU requiere que los lotes de dibujo contengan suficiente geometría (y que los sombreadores tengan la complejidad adecuada) para mantener la tarjeta de vídeo ocupada, sin usar tantos lotes que el búfer de comandos esté desbordado. En el hardware de generación actual, se recomiendan aproximadamente 300 envíos de draw-batch por fotograma (menos en CPU de menor rendimiento) para evitar que el procesamiento del controlador del búfer de comandos se convierta en un cuello de botella de rendimiento. Algunas otras llamadas de estado de API y combinaciones de controladores pueden dar lugar a costosos procesamientos de CPU (compilación de controladores de sombreadores, por ejemplo), por lo que se recomienda encarecidamente el análisis de rendimiento rutinario.

## <a name="excessive-memory-copying"></a>Copia excesiva de memoria

Durante el desarrollo de la mayoría de los títulos de pc, los desarrolladores usan estructuras de datos y cadenas prácticas para la administración de contenido. El trabajo de CPU necesario para la comparación de cadenas, la copia y otras manipulaciones a menudo tiene una sobrecarga medible, especialmente cuando se tienen en cuenta los aciertos de rendimiento asociados con la caché y el subsistema de memoria. Se deben realizar planes al desarrollar estos sistemas para quitar o minimizar la dependencia del procesamiento de cadenas una vez que el producto entra en las fases de prueba y versión principales.

## <a name="excessive-use-of-dynamic-draw-submission"></a>Uso excesivo del envío de dibujo dinámico

El hardware de vídeo moderno funciona bien cuando se trabaja con datos estáticos. Los adaptadores de gama alta suelen tener una cantidad muy grande de memoria de vídeo, pero los datos dinámicos no pueden utilizar esta memoria de forma eficaz.

Aunque se pueden implementar patrones de uso razonablemente eficientes de búferes de vértices dinámicos o búferes de índice para contenido dinámico, muchos títulos sobreutilizarán esta expresión para lo que de otro modo es contenido estático. A menudo vemos esto con árboles de partición de espacio binario (BSP) y sistemas basados en el portal que almacenan geometría en una estructura de datos que no se asigna al hardware y se debe procesar en búferes para cada fotograma. La colocación de tanto contenido en recursos estáticos como sea posible puede reducir en gran medida la sobrecarga de ancho de banda que conlleva transferir datos a la tarjeta de vídeo, hacer un mejor uso de VRAM de la placa y reducir la sobrecarga de cpu y caché implicada en el procesamiento de este contenido.

## <a name="high-overhead-in-file-processing"></a>Sobrecarga alta en el procesamiento de archivos

Los juegos de PC han obtenido una reputación de largos tiempos de carga, especialmente en comparación con los títulos de consola con requisitos estrictos de tiempo de carga. Nuestro análisis de la forma en que muchos títulos hacen uso del subsistema de archivos revela algunos problemas comunes.

La sobrecarga de abrir un archivo suele ser mucho mayor de lo que esperan los desarrolladores. Con los escáneres de virus a petición en uso generalizado y la funcionalidad adicional de NTFS, la apertura de un archivo es una operación bastante costosa. Abrir muchos archivos a la vez o abrir y cerrar repetidamente el mismo archivo es, por tanto, un método deficiente para tratar con la administración de archivos. Algunos juegos han intentado mitigar este costo de rendimiento mediante la prueba de la existencia de un archivo antes de abrirlo. La realidad es que la prueba de la existencia de un archivo en NTFS requiere abrir el archivo, por lo que la prueba antes de abrir da como resultado pagar el costo dos veces.

Los juegos que permiten modificaciones de complementos, o modificaciones, o que todavía incluyen scaffolding de desarrollo para comprobar si hay archivos de datos de invalidación, pueden tener retrasos significativos en la carga del juego debido a la comprobación de estos archivos, incluso cuando esos archivos no están presentes. Se recomienda que los juegos solo comprueben estos archivos cuando se ejecuten con un modificador de línea de comandos especial u otro indicador de modo, para que solo los usuarios que usan esta funcionalidad paguen realmente el costo de rendimiento de estas comprobaciones (a menudo extensas).

Se puede obtener un rendimiento adicional del sistema de archivos de la siguiente manera:

-   Uso adecuado de las sugerencias del sistema de archivos FILE \_ FLAG RANDOM ACCESS y FILE FLAG SEQUENTIAL \_ \_ \_ \_ \_ SCAN
-   Cambiar el tamaño de los búferes para evitar una gran cantidad de llamadas a las API de lectura y escritura del sistema operativo
-   Acceso a archivos de forma asincrónica
-   Carga de subprocesos en segundo plano

También se recomienda encarecidamente convertir datos sin conexión (en tiempo de compilación o instalación) en lugar de confiar en la conversión cuando se ejecuta el juego por primera vez, ya que hacerlo impone un impuesto de rendimiento significativo para todos los usuarios.

## <a name="slow-and-frustrating-installation"></a>Instalación lenta y frustrante

Otro problema común que hemos visto es que se requieren tiempos de instalación muy largos para muchos juegos de PC modernos. Los instaladores solicitan al usuario muchas veces, a veces simplemente para que le diga al usuario, por ejemplo, "No necesita DirectX instalado". Por lo general, estos instaladores ofensivos  requieren  que el usuario seleccione Siguiente o Aceptar muchas veces antes de que comience realmente la instalación del juego. Una vez que comienza, hemos visto que algunos títulos llevan una hora o más antes de que el usuario tenga la oportunidad de jugar el juego. Creemos que la primera hora de experiencia de juego no debe ser la instalación.

Se recomiendan varios enfoques para trabajar con la instalación. En primer lugar, mantenga los mensajes sencillos y al mínimo. En segundo lugar, diseñe los datos del juego de forma que algunos o todos los archivos de datos se puedan usar directamente desde el disco de distribución siempre que sea posible: las unidades de DVD modernas tienen un ancho de banda muy alto. En tercer lugar, considere la posibilidad de implementar la instalación a petición en los títulos para reducir o eliminar el proceso de instalación y permitir que los usuarios entren en el juego lo antes posible. (Para obtener más información sobre la instalación a petición, vea [Instalación a petición de juegos).](/windows/desktop/DxTechArts/install-on-demand-for-games)

Para obtener más recomendaciones sobre la instalación de juegos, [consulte Simplificación de la instalación de juegos.](/windows/desktop/DxTechArts/simplifying-game-installation)

## <a name="lack-of-consideration-of-physical-memory"></a>Falta de consideración de la memoria física

Debido a la gran variabilidad del hardware de pc en el mercado, los títulos suelen usar pruebas de configuración ad hoc para seleccionar la configuración predeterminada para el nivel de detalle gráfico. Algunos de los títulos que hemos visto son el uso del tamaño de memoria de vídeo en estas pruebas, pero no se puede correlacionar con el tamaño de la memoria física. Para controlar situaciones de dispositivo perdido, la mayor parte de la memoria de vídeo (tanto la VRAM local en la tarjeta como la apertura de memoria AGP no local) debe estar copiada por memoria física, ya sea mediante el uso de recursos administrados o estructuras de datos personalizadas. Algunas tarjetas de vídeo de gama alta tienen tamaños de VRAM que tienen el tamaño de memorias de CPU de gama baja. En situaciones en las que el sistema tiene memoria física limitada en comparación con la tarjeta de vídeo, la mayor parte de esa VRAM no se puede usar de forma eficaz y se deben configurar valores de detalle más bajos.

## <a name="over-reliance-on-real-time-audio-sample-rate-conversion"></a>Over-Reliance en la Real-Time frecuencia de muestreo de audio

Otra fuente común de grabación del ciclo de CPU que hemos visto se produce cuando se requiere que el sistema de audio convierta la velocidad de reproducción durante la combinación en el búfer de hardware. Con Windows Driver Model (WDM), el formato de búfer de hardware no está bajo control directo de la aplicación, porque es un recurso de nivel de kernel; en su lugar, el formato se selecciona en función del formato de mayor calidad de todos los orígenes y las funcionalidades del hardware. De forma predeterminada, Windows XP usa una conversión de frecuencia de muestreo de alta calidad para este proceso y, si la mayoría de las muestras de audio requieren una conversión de velocidad, se consumirá una parte significativa de los ciclos de CPU.

Se recomienda crear todos los búferes de Direct Sound con la misma frecuencia de muestreo. Si usa las funciones **waveOut** de Microsoft Win32, también debe usar una frecuencia de muestreo coherente con ellas. Con los controladores WDM, el kernel mezclará todos los búferes y, si usa una mayor frecuencia de muestreo en algunos de ellos, las tasas de muestreo de todo el resto se convertirán para que coincidan. Tenga en cuenta que esto implica usar la misma velocidad de reproducción para todas las muestras de audio, incluidos los búferes de descompresión de audio de streaming. Establecer la tasa de búfer principal no tiene ningún efecto a menos que tenga como destino Windows 98 o Windows Edition Edition.

> [!Note]  
> En Windows Vista y versiones posteriores del sistema operativo, Direct Sound y **waveOut** usan [Windows Audio Session API (WASAPI)](/windows/desktop/CoreAudio/wasapi) para todas las salidas de audio.

 

## <a name="fragmention-of-virtual-memory"></a>Fragmentación de memoria virtual

Hemos visto una serie de problemas recientes relacionados con el límite de 32 bits en el espacio de memoria del proceso. Aunque 2 GB de espacio de direcciones virtuales para los procesos en modo de usuario han sido más que adecuados históricamente, el mayor uso de archivos asignados a memoria de gran tamaño, asignadores de memoria personalizados y el aumento del tamaño de VRAM (que se debe asignar al espacio de proceso) ha empezado a provocar situaciones en las que se están fallando las asignaciones de espacio de memoria virtual. Algunos archivos DLL que no son de Microsoft usan ubicaciones de inicio fijo en medio del espacio de direcciones virtuales, lo que provoca una fragmentación que da lugar a asignaciones con errores.

Estos problemas suelen aparecer cuando el juego usa un esquema de asignación de memoria personalizado que intenta asignar un gran fragmento continuo de espacio de memoria virtual. Nuestra recomendación es escribir asignadores para que soliciten partes más razonables del espacio de direcciones virtuales según sea necesario. Por ejemplo, solicitar 64 o 256 MB a la vez, pero no 1 GB. Sin embargo, se debe tener cuidado para no provocar más fragmentación. La llegada de hardware y sistemas operativos de 64 bits ayudará en gran medida a estos problemas en el futuro, pero se debe tener cuidado con los sistemas de 32 bits de generación actual.

## <a name="manipulation-of-the-floating-point-control-word"></a>Manipulación de la palabra Floating-Point control

Como ayuda para la depuración, algunos desarrolladores han habilitado excepciones en la unidad de punto flotante (FPU) mediante manipulaciones de la palabra de control de punto flotante. Esto es muy problemático y probablemente hará que el proceso se bloquea. Al igual que la convención de llamada requiere que se conserve el registro ebx, la mayoría del sistema asume que la FPU está en un estado predeterminado, dará resultados razonables y no generará excepciones. Los controladores y otros componentes del sistema a menudo calcularán los resultados en función de la suposición de que los valores de error estándar aparecerán en los registros en busca de condiciones incorrectas, pero si se habilitan las excepciones, estas no se podrán tratar y provocarán bloqueos.

Direct3D establecerá la unidad de punto flotante en precisión sencilla, redondeada a la más cercana como parte de la inicialización del subproceso que realiza la llamada, a menos que se utilice la marca PRESERVE de D3DCREATE FPU, en cuyo caso, la palabra de control de punto flotante no \_ \_ se toca. Puesto que la palabra de control es una configuración por subproceso, asegurarse de que todos los subprocesos de la aplicación están establecidos en modo de precisión sencilla puede optimizar el rendimiento. Recuerde que llamar a [**\_ control87**](https://msdn.microsoft.com/library/e9b52ceh(v=VS.71).aspx) no es válido para la codificación nativa x64, que usa SSE exclusivamente en su lugar, y es muy costoso en la arquitectura basada en PowerPC de la CPU Xbox 360.

> [!Note]  
> Si modifica la palabra de control, use [**\_ \_ controlesfps**](https://msdn.microsoft.com/library/c9676k6h(v=VS.80).aspx) y tenga en cuenta que para las plataformas x64 no puede cambiar la precisión de punto flotante a través de la palabra de control.

 

En las bibliotecas en las que es necesario tener reglas de redondeo diferentes u otro comportamiento, como trabajar con sombreadores de vértices de software o compilación, guardamos y restauramos la palabra de control. Si un juego necesita usar el redondeo no estándar o las excepciones de FPU, debe guardar y restaurar la palabra de control de punto flotante, y debe asegurarse de que no llama a ningún código externo que no se haya demostrado que esté seguro de estos problemas, incluidas las API del sistema.

## <a name="optional-installation-of-the-directx-runtime"></a>Instalación opcional del entorno de ejecución de DirectX

Varios juegos preguntan al usuario si desea instalar DirectX. Esto puede causar problemas si el usuario asume que el sistema tiene instalada la versión más reciente de DirectX redistribuible y omite la instalación y, posteriormente, la instalación continúa correctamente. Si el juego requiere una versión específica de D3DX u otra funcionalidad actualizada que no se instaló, el juego no funcionará y el usuario se frustrará mucho.

Se recomienda encarecidamente que el instalador del juego instale silenciosamente directX redistribuible en el que se comcreó el juego. El proceso de instalación de DirectX está diseñado para que compruebe si es necesario actualizar algo y devuelve rápidamente si no lo hace. Por lo tanto, no es necesario preguntar al usuario sobre la instalación de DirectX.

Para realizar una instalación silenciosa de DirectX, ejecute este comando desde el paquete de instalación: **dxsetup.exe /silent**

Además, el tamaño real de la carpeta redistribuible se puede configurar para incluir solo los archivos de archivo (.cab) que realmente son necesarios para las plataformas de destino y el uso del juego.

> [!Note]  
> Antes de usar **dxsetup,** lea [No es tan directo.](https://walbourn.github.io/)

 

## <a name="excessive-use-of-thread-synchronization"></a>Uso excesivo de la sincronización de subprocesos

Al generar perfiles de juegos, las zonas activas principales suelen estar relacionadas con la entrada y la salida de secciones críticas. Con la persistencia de las CPU de varios núcleos, el uso de multithreading en juegos ha aumentado drásticamente y muchas implementaciones dependen de un uso elevado de la sincronización de subprocesos. El tiempo de CPU para tomar una sección crítica incluso sin ninguna contención es bastante significativo y todas las demás formas de sincronización de subprocesos son incluso más costosas. Por lo tanto, se debe tener cuidado para minimizar el uso de estos primitivos.

Una fuente común de sincronización excesiva en juegos es el uso de [D3DCREATE \_ MULTITHREADED.](/windows/desktop/direct3d9/d3dcreate) Esta marca, al tiempo que hace que Direct3D sea seguro para subprocesos para la representación desde varios subprocesos, adopta un enfoque muy conservador, lo que genera una sobrecarga de sincronización alta. Los juegos deben evitar esta marca. En su lugar, diseñe el motor para que toda la comunicación con Direct3D sea de un único subproceso y cualquier comunicación entre subprocesos se controle directamente. Para obtener más información sobre el diseño de juegos multiproceso, vea el artículo Codificación para varios [núcleos](/windows/desktop/DxTechArts/coding-for-multiple-cores)en Xbox 360 y Microsoft Windows .

## <a name="use-of-rdtsc"></a>Uso de RDTSC

No se recomienda el uso de **la instrucción x86 RDTSC.** **RDTSC** no puede calcular correctamente el tiempo en algunos esquemas de administración de energía que cambian dinámicamente la frecuencia de CPU y en muchas CPU de varios núcleos para las que el contador de ciclo no está sincronizado entre núcleos. En su lugar, Los juegos deben usar la API [**QueryPerformanceCounter.**](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter) Para obtener más información sobre los problemas con **RDTSC** e implementar el control de tiempo de alta resolución con **QueryPerformanceCounter**, vea el artículo Game Timing and Multicore Processors (Control de tiempo de juego y procesadores [de varios núcleos).](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)

 

 