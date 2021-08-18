---
title: Windows Guía de Advanced Rasterization Platform (WARP)
description: En este artículo se Windows Advanced Rasterization Platform (WARP) y los siguientes aspectos de WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab76fd68985069e6114cd7bbb0901eeba5d911eba574332b1dd2008f0375a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745995"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Windows Guía de Advanced Rasterization Platform (WARP)

En este artículo se Windows Advanced Rasterization Platform (WARP) y los siguientes aspectos de WARP.

-   [¿Qué es WARP?](#what-is-warp)
-   [Ventajas de WARP](#warp-benefits)
    -   [Eliminación de la necesidad de rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
    -   [Habilitación del rendimiento máximo desde hardware gráfico](#enabling-maximum-performance-from-graphics-hardware)
    -   [Habilitar la representación cuando el hardware de Direct3D no está disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Aprovechamiento de los recursos existentes para la representación de software](#leveraging-existing-resources-for-software-rendering)
    -   [Habilitar escenarios que no requieren hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Finalización de la plataforma de gráficos de DirectX](#completing-the-directx-graphics-platform)
-   [Funcionalidades y requisitos de WARP](#warp-capabilities-and-requirements)
-   [Uso de WARP](#how-to-use-warp)
-   [Tipos de aplicación recomendados para WARP](#recommended-application-types-for-warp)
    -   [Juegos informales](#casual-games)
    -   [Aplicaciones que no son de juegos existentes](#existing-non-gaming-applications)
    -   [Juegos de representación avanzada](#advanced-rendering-games)
    -   [Otras aplicaciones](#other-applications)
-   [Arquitectura y rendimiento de WARP](#warp-architecture-and-performance)
-   [Conformidad con WARP](#warp-conformance)

## <a name="what-is-warp"></a>¿Qué es WARP?

WARP es un rasterizador de software totalmente compatible y de alta velocidad. Es un componente de la tecnología de gráficos DirectX introducida por el entorno de ejecución de Direct3D 11. El entorno de ejecución de Direct3D 11 se instala en Windows 7, Windows Server 2008 R2 y Windows Vista con la actualización \[ KB971644. \] Windows 8, Windows 10, Windows Server 2012 & anteriores y Windows RT incluyen el entorno de ejecución de Direct3D 11.1, que tiene una versión actualizada de WARP. Windows 10 Fall Creators Update (1709) incluye una versión de WARP que admite los entornos de ejecución de Direct3D 11 y Direct3D 12.

## <a name="warp-benefits"></a>Ventajas de WARP

WARP proporciona las siguientes ventajas:

-   [Eliminación de la necesidad de rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
-   [Habilitación del rendimiento máximo desde hardware gráfico](#enabling-maximum-performance-from-graphics-hardware)
-   [Habilitar la representación cuando el hardware de Direct3D no está disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Aprovechamiento de los recursos existentes para la representación de software](#leveraging-existing-resources-for-software-rendering)
-   [Habilitar escenarios que no requieren hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Finalización de la plataforma de gráficos de DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Eliminación de la necesidad de rasterizadores de software personalizados

WARP simplifica el desarrollo al eliminar la necesidad de crear un rasterizador de software personalizado y ajustar la aplicación para él en lugar de ajustar la aplicación para hardware. Al proporcionar un rasterizador de software de uso general único, ya no es necesario escribir algoritmos de representación de imágenes de varias maneras para ejecutarse en hardware o software con diferentes características y funcionalidades. Todavía puede implementar algoritmos de varias maneras para lograr un mejor rendimiento o escalado. sin embargo, no es necesario cambiar la API o la arquitectura de representación que se usa para implementar esos algoritmos. En su lugar, puede centrarse en crear una excelente aplicación direct3D 10 o posterior que tendrá el mismo aspecto y tendrá un buen rendimiento en hardware o en software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Habilitación del rendimiento máximo desde hardware gráfico

Cuando una aplicación se ajuste para que se ejecute de forma eficaz en el hardware, también se ejecutará de forma eficaz en WARP. Lo contrario también es cierto; cualquier aplicación que se ajuste para ejecutarse correctamente en WARP tendrá un buen rendimiento en el hardware. Es posible que las aplicaciones que usan Direct3D 10 y versiones posteriores no escalen de forma eficaz en hardware diferente. WARP tiene perfiles de rendimiento similares al hardware, por lo que el ajuste de una aplicación para lotes grandes, la minimización de los cambios de estado y la eliminación de puntos o bloqueos de sincronización beneficiarán tanto al hardware como a WARP.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Habilitar la representación cuando el hardware de Direct3D no está disponible

WARP permite una representación rápida en una variedad de situaciones en las que las implementaciones de hardware no son deseadas o no están disponibles, entre las que se incluyen:

-   Cuando el usuario no tiene hardware compatible con Direct3D
-   Cuando una aplicación se ejecuta como un servicio o en un entorno de servidor
-   Cuando una aplicación desea reservar los recursos de hardware de Direct3D para otros usos
-   Cuando no se instala una tarjeta de vídeo
-   Cuando un controlador de vídeo no está disponible o no funciona correctamente
-   Cuando una tarjeta de vídeo no tiene memoria, se desahora o se tardarían demasiados recursos del sistema en inicializarse

### <a name="leveraging-existing-resources-for-software-rendering"></a>Aprovechamiento de los recursos existentes para la representación de software

Hay una gran comunidad, muchos libros, sitios web, SDK, ejemplos, documentos técnicos, listas de distribución de correo y otros recursos que pueden ayudarle a aprovechar las ventajas de la representación de imágenes basadas en sombreador de Direct3D 10 y versiones posteriores. Con WARP como reserva de software, puede usar los conocimientos existentes sobre el hardware para mejorar el rendimiento de la aplicación cuando se ejecuta con hardware o software. Además, muchas herramientas excelentes de los proveedores de tarjetas gráficas y del SDK de DirectX pueden ayudarle a diseñar, compilar, desarrollar, depurar y analizar problemas de rendimiento de las aplicaciones gráficas. Estas herramientas y conocimientos ahora pueden beneficiar el desarrollo de aplicaciones que se dirige tanto al hardware como al software cuando se usa WARP.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Habilitar escenarios que no requieren hardware gráfico

Varios algoritmos y aplicaciones (algoritmos de procesamiento de imágenes, impresión, comunicación remota, equipos virtuales y otros emuladores, representación de fuentes de alta calidad, gráficos, entre otros) se han optimizado normalmente para la CPU porque no dependen del hardware. Con WARP, puede usar una arquitectura única que ejecute estos algoritmos y aplicaciones y que se pueda ejecutar completamente en software. sin embargo, si la aceleración de hardware está disponible, puede aprovecharla.

### <a name="completing-the-directx-graphics-platform"></a>Finalización de la plataforma de gráficos de DirectX

WARP permite acceder a todas las características gráficas de Direct3D 10 y versiones posteriores, incluso en equipos sin hardware gráfico de Direct3D 10 y versiones posteriores. Direct3D 10 quita los bits de funcionalidad (límites); Es decir, ya no es necesario comprobar si las funcionalidades de gráficos están disponibles en el hardware gráfico porque Direct3D 10 y versiones posteriores garantizan esta disponibilidad. Ahora puede usar todas las características de una amplia gama de tarjetas de vídeo sabiendo que su aplicación se comportará y tendrá el mismo aspecto en todas partes. Puede escalar el rendimiento de estas aplicaciones simplemente deshabilitando características de gráficos costosas en tarjetas de vídeo de gama baja o representando en destinos más pequeños.

## <a name="warp-capabilities-and-requirements"></a>Funcionalidades y requisitos de WARP

WARP es totalmente compatible con todas las características de Direct3D 10 y 10.1. Por ejemplo, WARP admite las siguientes características más importantes:

-   Todos los requisitos de precisión de la especificación 10 y 10.1 de Direct3D
-   Direct3D 11 cuando se usa con los niveles de características 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 0 y \_ \_ 10 1 (para [**\_ \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)obtener más información sobre los niveles de características, vea NIVEL DE CARACTERÍSTICAS D3D)
-   Todos los formatos de textura opcionales, como destinos de representación multimuestreo y muestreo de superficies flotantes
-   Suavizado de contorno, representación de alta calidad hasta 8 veces el suavizado de contorno multimuestreo (MSAA)
-   Filtrado anisotropo
-   Aplicaciones de 32 y 64 bits y aplicaciones de 32 bits que tienen en cuenta direcciones grandes

Al instalar la actualización de plataforma para [Windows 7](https://support.microsoft.com/kb/2670838) en Windows 7 SP1 o Windows Server 2008 R2 SP1, ese sistema operativo incluye el entorno de ejecución de Direct3D 11.1 y una versión de WARP que admite Direct3D 11.x cuando se usa con los niveles de características [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, \_ 10 1 y 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & anteriores y Windows RT incluyen el entorno de ejecución de Direct3D 11.1 y una nueva versión de WARP. Esta versión admite Direct3D 11.x cuando se usa con los niveles de características [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 y 11 \_ 1.

Windows 10 Fall Creators Update (1709) incluye una nueva versión de WARP que admite los niveles de características 12 0 y 12 1 de [Direct3D](../direct3d12/direct3d-12-graphics.md) \_ \_ 12. 

Los requisitos mínimos de equipo para WARP son los mismos que para Windows Vista, específicamente:

-   CPU mínima de 800 MHz
-   No se requiere MMX, SSE o SSE2
-   512 MB como mínimo de RAM

## <a name="how-to-use-warp"></a>Uso de WARP

Los componentes de Direct3D 10, 10.1, 11 y 12 pueden usar un tipo de controlador adicional que puede especificar al crear el dispositivo (por ejemplo, al llamar a la función [**D3D11CreateDevice).**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) Este tipo de controlador es [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) o [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Cuando se especifica este tipo de controlador, el tiempo de ejecución crea un dispositivo WARP y no inicializa un dispositivo de hardware.

Dado que WARP usa la misma interfaz de software para Direct3D que el rasterizador de referencia, cualquier aplicación de Direct3D que pueda admitir la ejecución con el rasterizador de referencia se puede probar mediante WARP. Para usar WARP, cambie el D3d10warp.dll a D3d10ref.dll y colómelo en la misma carpeta que el ejemplo o la aplicación. A continuación, cuando cambie a ref, verá la representación de WARP.

Si cambia el nombre de WARP a D3d10ref.dll y lo coloca en C: Archivos de programa \\ (x86) \\ Microsoft DirectX SDK (junio de 2010) Ejemplos de \\ \\ C++ \\ Direct3D \\ Bin \\ x86, puede ejecutar todos los ejemplos de DirectX en WARP, ya sea haciendo clic en el botón "Alternar referencia" del ejemplo o ejecutando el ejemplo con /ref especificado en la línea de comandos.

## <a name="recommended-application-types-for-warp"></a>Tipos de aplicación recomendados para WARP

Todas las aplicaciones que pueden usar Direct3D pueden usar WARP. Esto incluye los siguientes tipos de aplicaciones:

-   [Juegos informales](#casual-games)
-   [Aplicaciones que no son de juegos existentes](#existing-non-gaming-applications)
-   [Juegos de representación avanzada](#advanced-rendering-games)
-   [Otras aplicaciones](#other-applications)

### <a name="casual-games"></a>Juegos informales

Los juegos suelen tener requisitos de representación sencillos. Sin embargo, también requieren el uso de efectos visuales impresionantes que podrían necesitar aceleración de hardware. La mayoría de los títulos de juegos más vendidos para Windows son simulaciones o juegos ocasionales, ninguno de los cuales requiere gráficos de alto rendimiento. Sin embargo, ambos estilos de juegos se benefician en gran medida de los gráficos modernos basados en sombreador y de la capacidad de escalar en hardware.

### <a name="existing-non-gaming-applications"></a>Aplicaciones que no son de juegos existentes

Una gran cantidad de aplicaciones gráficas requieren un número mínimo de rutas de acceso de código en su capa de representación. WARP permite que estas aplicaciones implementen una ruta de acceso de código direct3D única que pueda tener como destino un gran número de configuraciones de equipo.

### <a name="advanced-rendering-games"></a>Juegos de representación avanzada

Es posible que los desarrolladores de juegos quieran aislar los errores de representación específicos de la tarjeta gráfica o del controlador. Por lo tanto, todos los juegos, incluso los juegos extremadamente exigentes gráficamente, pueden beneficiarse de poder representar su contenido mediante WARP. Puede usar WARP para validar si los artefactos visuales que encuentre están representando errores o problemas con el hardware o los controladores.

### <a name="other-applications"></a>Otras aplicaciones

Las aplicaciones de destino para WARP también incluyen aquellas que podrían no usar actualmente Direct3D 10 o Direct3D 10.1. Estas aplicaciones de destino incluyen aplicaciones que siempre deben funcionar en todos los equipos, aplicaciones de procesamiento de imágenes que no escriben versiones de CPU y GPU de algoritmos de procesamiento de imágenes, algoritmos de procesamiento de imágenes donde la velocidad o el uso de la GPU no son críticos, como la impresión, y emuladores y entornos virtuales que muestran gráficos 3D avanzados.

## <a name="warp-architecture-and-performance"></a>Arquitectura y rendimiento de WARP

WARP se basa en el código base del rasterizador de referencia. Por lo tanto, WARP usa la misma interfaz de software para Direct3D 10 y versiones posteriores y DXGI. WARP se incluye en Windows 7 en el D3d10warp.dll, ubicado en Windows de sistemas. Hay dos versiones de WARP instaladas en máquinas de 64 bits, una versión x86 y x64. La versión x64 podría ejecutarse más rápido en determinadas circunstancias porque el generador de código contenido en WARP puede aprovechar los registros adicionales que están disponibles cuando los usuarios ejecutan aplicaciones de 64 bits.

WARP contiene los dos compiladores de alta velocidad en tiempo real siguientes:

-   Compilador de lenguaje intermedio de alto nivel que convierte el código de bytes HLSL y el estado de representación actual en una secuencia optimizada de comandos vectoriales para las fases del sombreador de geometría (GS), el sombreador de vértices (VS) y el sombreador de píxeles (PS) de la canalización.
-   Generador de código Just-In-Time de alto rendimiento que puede tomar estos comandos y generar código de ensamblado SSE2, SSE4.1, x86, x64, arm y arm64 optimizado.

WARP usa el grupo de subprocesos y la administración de tareas complejas y el seguimiento de dependencias que se introdujo en Windows Vista para permitir que todas las partes de la canalización de representación se distribuyen de forma eficaz entre los núcleos de CPU disponibles.

WARP usa la representación diferida. Es decir, WARP puede representar por lotes comandos para que la rasterización se produzca solo cuando haya suficientes datos disponibles para usar todos los recursos de CPU de forma eficaz. El trabajo en el subproceso de aplicación principal se minimiza para permitir que la aplicación envíe comandos lo antes posible. Si una aplicación también tiene varios subprocesos y usa el grupo de subprocesos, el trabajo se distribuirá uniformemente entre WARP y la aplicación.

El generador de código WARP se ha optimizado para hacer el mejor uso de la arquitectura de CPU moderna. WARP se ejecuta en todos los equipos que pueden ejecutar Windows Vista y sistemas operativos posteriores, incluso si el equipo no es compatible con SSE. Sin embargo, WARP se ha optimizado para equipos que admiten SSE2. También contiene optimizaciones para arquitecturas específicas de procesadores AMD e Intel, así como compatibilidad con las extensiones SSE 4.1.

WARP no requiere hardware gráfico para ejecutarse. Se puede ejecutar incluso en situaciones en las que el hardware no está disponible o no se puede inicializar.

Es probable que las aplicaciones y ejemplos diseñados y creados para ejecutarse en el hardware de Direct3D 10 y versiones posteriores sin ningún conocimiento de WARP se ejecuten bien mediante WARP. Sin embargo, se recomienda reducir la configuración de calidad y la resolución tanto como sea posible para lograr velocidades de fotogramas utilizables. Puede usar WARP para desarrollar y optimizar aplicaciones que se ejecutan bien en hardware y software.

Dado que WARP usa varios núcleos de CPU, funciona mejor en cpu modernas de cuatro núcleos. WARP también se ejecuta mucho más rápido en equipos con extensiones SSE4.1 instaladas. Microsoft realizó pruebas y ajustes de rendimiento significativos en equipos con ocho o más núcleos y SSE4.1, ya que estos equipos de gama alta serán más comunes durante la vigencia de Windows 7 y sistemas operativos posteriores.

Cuando WARP se ejecuta en la CPU, se limita en comparación con una tarjeta gráfica de varias maneras. La velocidad del bus del lado frontal de una CPU suele estar alrededor o por debajo de 10 GB/s. Por el contrario, una tarjeta gráfica a menudo tiene memoria dedicada que usa entre 20 y 100 GB/s o más de ancho de banda de gráficos. El hardware gráfico también tiene unidades de función fija que pueden realizar tareas complejas y costosas, como el filtrado de texturas, la descompresión de formato o las conversiones, de forma asincrónica con poca sobrecarga o costo de energía. Realizar estas operaciones en una CPU típica es costoso en términos de consumo de energía y ciclos de rendimiento.

Los números de rendimiento típicos de una máquina Intel Penryn basada en cuatro núcleos de 3,0 GHz muestran que WARP puede en algunos casos superar a las GPU de gráficos integradas de bajo nivel Direct3D 10 y posteriores en una serie de pruebas comparativas. El hardware gráfico discreto de gama baja suele ser de 4 a 5 veces más rápido que WARP al ejecutar estas pruebas comparativas. Estas GPU discretas o integradas de bajo nivel tienen un uso mínimo de los recursos de CPU. Las tarjetas gráficas de gama media o alta son significativamente más rápidas que WARP para muchas aplicaciones, especialmente cuando una aplicación puede aprovechar el paralelismo y el ancho de banda de memoria que proporcionan estas tarjetas gráficas.

WARP no es un sustituto del hardware gráfico, especialmente porque el rendimiento razonable de direct3D 10 de bajo nivel y hardware discreto posterior ahora es económico. El objetivo de WARP es permitir que las aplicaciones tengan como destino el hardware de nivel 10 de Direct3D sin tener rutas de acceso de código significativamente diferentes ni requisitos de prueba, tanto si se ejecutan en hardware como en software.

En las dos tablas siguientes se muestran datos de ejemplo de WARP con varias CPU y tarjetas gráficas.

En la primera tabla se muestran los datos de ejemplo de WARP con Direct3D 10 Warpsis ejecutándose a 800 x 600 con toda la configuración de calidad en sus niveles más bajos:

| CPU                         | Time   | Ave FPS | FPS mínimo | Marco mínimo | Fps máximo | Marco máximo |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core @ 3.0GHz     | 271.57 | 7.36    | 3,46    | 1966      | 15.01   | 995       |
| Penryn 4 Core @ 3.0GHz      | 351.35 | 5.69    | 2.49    | 1967      | 10.95   | 980       |
| Penryn 2 Core @ 3.0GHz      | 573.98 | 3.48    | 1.35    | 1964      | 6.61    | 988       |
| Core 2 Duo a 2,6 GHz         | 707.19 | 2,83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo a 2,4 GHz         | 763.25 | 2.62    | 0,76    | 1964      | 4.70    | 984       |
| Core 2 Duo a 2,1 GHz         | 908.87 | 2,20    | 0.64    | 1965      | 3,72    | 986       |
| Xeon 8 Core @ 2,0 GHz        | 424.04 | 4.72    | 1,84    | 1967      | 9.56    | 988       |
| AMD FX74 de 4 núcleos a 3,0 GHz    | 583.12 | 3.43    | 1,41    | 1967      | 5.78    | 986       |
| Om 9550 4 núcleos a 2,2 GHz | 664.69 | 3,01    | 0.53    | 1959      | 5.46    | 987       |

En la segunda tabla se muestran datos de ejemplo que ejecutan la misma prueba en una variedad de tarjetas gráficas:

| Tarjeta gráfica         | Time   | Ave FPS | FPS mínimo | Marco mínimo | Fps máximo | Marco máximo |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23.58  | 84.80   | 60.78   | 1957      | 130.83  | 1022      |
| NVIDIA 8500 GT        | 47.63  | 41.99   | 25.67   | 1986      | 72.57   | 991       |
| NVIDIA Quadro 290     | 67.16  | 29.78   | 18.19   | 1969      | 49.87   | 1017      |
| NVIDIA 8400 GS        | 59.01  | 33.89   | 21,22   | 1962      | 51.82   | 1021      |
| ATI 3400              | 53.79  | 37.18   | 22,97   | 618       | 59.77   | 1021      |
| ATI 3200              | 67.19  | 29.77   | 18.91   | 1963      | 45.74   | 980       |
| ATI 2400 PRO          | 67.04  | 29.83   | 17.97   | 606       | 45.91   | 987       |
| Intel DX10 integrado | 386.94 | 5.17    | 1.74    | 1974      | 16.22   | 995       |

## <a name="warp-conformance"></a>Conformidad con WARP

WARP pasa todas las pruebas Windows de conformidad de Hardware Quality Labs (WHQL) estándar para validar dispositivos de hardware Direct3D.

WARP se ha probado con un conjunto de aplicaciones y pruebas comparativas de Direct3D 10 y Direct3D 10.1, y con ejemplos de SDK de DirectX, NVIDIA y AMD.

WARP usó la herramienta de depuración y análisis [DE ANDV](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) Windows en sus pruebas; Microsoft tiene una gran biblioteca de capturas de fotograma único de aplicaciones que se usan para comparar entre hardware y WARP. La mayoría de las imágenes parecen casi idénticas entre hardware y WARP; donde a veces se producen pequeñas diferencias, se encuentran dentro de las tolerancias definidas por la especificación de Direct3D 10.