---
title: Guía de Windows Advanced Rasterization Platform (WARP)
description: En este artículo se describe la plataforma de rasterización avanzada de Windows (WARP) y los siguientes aspectos de WARP.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793083"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Guía de Windows Advanced Rasterization Platform (WARP)

En este artículo se describe la plataforma de rasterización avanzada de Windows (WARP) y los siguientes aspectos de WARP.

-   [¿Qué es WARP?](#what-is-warp)
-   [Ventajas de WARP](#warp-benefits)
    -   [Eliminación de la necesidad de Rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
    -   [Habilitar el máximo rendimiento del hardware de gráficos](#enabling-maximum-performance-from-graphics-hardware)
    -   [Habilitar la representación cuando el hardware de Direct3D no está disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Aprovechar los recursos existentes para la representación de software](#leveraging-existing-resources-for-software-rendering)
    -   [Habilitar escenarios que no requieren hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Completar la plataforma de gráficos de DirectX](#completing-the-directx-graphics-platform)
-   [Funcionalidades y requisitos de WARP](#warp-capabilities-and-requirements)
-   [Cómo usar WARP](#how-to-use-warp)
-   [Tipos de aplicación recomendados para WARP](#recommended-application-types-for-warp)
    -   [Juegos esporádicos](#casual-games)
    -   [Aplicaciones existentes que no son de juegos](#existing-non-gaming-applications)
    -   [Juegos de representación avanzados](#advanced-rendering-games)
    -   [Otras aplicaciones](#other-applications)
-   [Arquitectura y rendimiento de WARP](#warp-architecture-and-performance)
-   [Conformidad con WARP](#warp-conformance)

## <a name="what-is-warp"></a>¿Qué es WARP?

WARP es un rasterizador de software totalmente compatible con alta velocidad. Es un componente de la tecnología de gráficos de DirectX que se incorporó en el tiempo de ejecución de Direct3D 11. El tiempo de ejecución de Direct3D 11 se instala en Windows 7, Windows Server 2008 R2 y Windows Vista con la \[ actualización de KB971644 \] . Windows 8, Windows 10, Windows Server 2012 & anteriores y Windows RT incluyen el tiempo de ejecución de Direct3D 11,1, que tiene una versión actualizada de WARP. Windows 10 Fall Creators Update (1709) incluye una versión de WARP que admite los tiempos de ejecución de Direct3D 11 y Direct3D 12.

## <a name="warp-benefits"></a>Ventajas de WARP

WARP proporciona las siguientes ventajas:

-   [Eliminación de la necesidad de Rasterizadores de software personalizados](#removing-the-need-for-custom-software-rasterizers)
-   [Habilitar el máximo rendimiento del hardware de gráficos](#enabling-maximum-performance-from-graphics-hardware)
-   [Habilitar la representación cuando el hardware de Direct3D no está disponible](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Aprovechar los recursos existentes para la representación de software](#leveraging-existing-resources-for-software-rendering)
-   [Habilitar escenarios que no requieren hardware gráfico](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Completar la plataforma de gráficos de DirectX](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Eliminación de la necesidad de Rasterizadores de software personalizados

WARP simplifica el desarrollo al eliminar la necesidad de crear un rasterizador de software personalizado y optimizar su aplicación en lugar de ajustar la aplicación para el hardware. Al proporcionar un único rasterizador de software de uso general, ya no es necesario escribir algoritmos de representación de imágenes de varias maneras para ejecutarse en hardware o software con diferentes características y capacidades. Todavía puede implementar algoritmos de varias maneras para lograr un mejor rendimiento o escalado. sin embargo, no es necesario cambiar la arquitectura de representación o API que se usa para implementar esos algoritmos. En su lugar, puede centrarse en la creación de una aplicación de Direct3D 10 o una versión posterior que tendrá el mismo aspecto y rendimiento en el hardware o en el software.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Habilitar el máximo rendimiento del hardware de gráficos

Cuando se optimiza una aplicación para que se ejecute de forma eficaz en el hardware, también se ejecutará de forma eficaz en WARP. Lo contrario también es cierto. cualquier aplicación que esté optimizada para ejecutarse correctamente en WARP funcionará bien en el hardware. Es posible que las aplicaciones que usan Direct3D 10 y versiones posteriores de manera ineficaz no escalen de forma eficaz en hardware diferente. WARP tiene perfiles de rendimiento similares a los de hardware, por lo que la optimización de una aplicación para lotes grandes, con lo que se minimizan los cambios de estado y se quitan los puntos de sincronización y los bloqueos beneficiarán tanto el hardware como la

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Habilitar la representación cuando el hardware de Direct3D no está disponible

WARP permite una representación rápida en una gran variedad de situaciones en las que las implementaciones de hardware no son deseables o no están disponibles, entre las que se incluyen:

-   Cuando el usuario no tiene ningún hardware compatible con Direct3D
-   Cuando una aplicación se ejecuta como un servicio o en un entorno de servidor
-   Cuando una aplicación desea reservar los recursos de hardware de Direct3D para otros usos
-   Cuando no se instala una tarjeta de vídeo
-   Cuando un controlador de vídeo no está disponible o no funciona correctamente
-   Cuando una tarjeta de vídeo no tiene memoria suficiente, se bloquea o tarda demasiados recursos del sistema en inicializarse

### <a name="leveraging-existing-resources-for-software-rendering"></a>Aprovechar los recursos existentes para la representación de software

Hay una gran comunidad, muchos libros, sitios web, SDK, ejemplos, notas del producto, listas de distribución de correo y otros recursos que pueden ayudarle a aprovechar las ventajas de Direct3D 10 y versiones posteriores de representación de imágenes basadas en sombreadores. Con WARP como reserva de software, puede usar el conocimiento existente sobre el hardware para mejorar el rendimiento de la aplicación cuando se ejecuta con hardware o software. Además, muchas herramientas excelentes de los proveedores de tarjetas de gráficos y del SDK de DirectX pueden ayudarle a diseñar, compilar, desarrollar, depurar y analizar los problemas de rendimiento de las aplicaciones de gráficos. Estas herramientas y conocimientos pueden ahora beneficiarse del desarrollo de aplicaciones que se dirige al hardware y al software cuando se usa WARP.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Habilitar escenarios que no requieren hardware gráfico

Los distintos algoritmos y aplicaciones (algoritmos de procesamiento de imágenes, impresión, comunicación remota, equipos virtuales y otros emuladores, representación de fuentes de alta calidad, gráficos, gráficos, etc.) se han optimizado para la CPU, ya que no dependen del hardware. Con WARP, puede usar una única arquitectura que ejecute estos algoritmos y aplicaciones y que se pueda ejecutar completamente en el software; sin embargo, si la aceleración de hardware está disponible, puede beneficiarse de ella.

### <a name="completing-the-directx-graphics-platform"></a>Completar la plataforma de gráficos de DirectX

WARP permite tener acceso a todas las características de gráficos de Direct3D 10 y versiones posteriores, incluso en equipos sin el hardware de gráficos de Direct3D 10 y versiones posteriores. Bits de capacidad quitados de Direct3D 10 (Cap); es decir, ya no tiene que comprobar si las capacidades de gráficos están disponibles en el hardware de gráficos porque Direct3D 10 y versiones posteriores garantizan esta disponibilidad. Ahora puede usar todas las características de una amplia gama de tarjetas de vídeo sabiendo que su aplicación se comportará y tendrá el mismo aspecto en todas partes. Puede escalar el rendimiento de estas aplicaciones simplemente deshabilitando características de gráficos muy costosas en tarjetas de vídeo de baja gama o en destinos más pequeños.

## <a name="warp-capabilities-and-requirements"></a>Funcionalidades y requisitos de WARP

WARP es totalmente compatible con todas las características de Direct3D 10 y 10,1. Por ejemplo, WARP admite las siguientes características más importantes:

-   Todos los requisitos de precisión de la especificación Direct3D 10 y 10,1
-   Direct3D 11 cuando se usa con los niveles de características 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 y 10 \_ 1 (para obtener más información sobre los niveles de características, consulte [**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level))
-   Todos los formatos de textura opcionales, como los destinos de representación multiejemplo y el muestreo de superficies flotantes
-   Alisado, representación de alta calidad hasta 8X con suavizado de contorno de muestreo Multimuestra (MSAA)
-   Filtrado anisotrópico
-   aplicaciones de 32 bits y de 64 bits y aplicaciones de 32 bits con reconocimiento de direcciones grandes

Al instalar la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838) en Windows 7 SP1 o windows Server 2008 R2 SP1, ese sistema operativo incluye el tiempo de ejecución de Direct3D 11,1 y una versión de Warp que admite Direct3D 11. x cuando se usa con [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1 y 11 \_ 0.

Windows 8, Windows 10, Windows Server 2012 & anteriores y Windows RT incluyen el tiempo de ejecución de Direct3D 11,1 y una nueva versión de WARP. Esta versión es compatible con Direct3D 11. x cuando se usa con [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 y 11 \_ 1.

Windows 10 Fall Creators Update (1709) incluye una nueva versión de WARP que admite [](../direct3d12/direct3d-12-graphics.md) los niveles de características 12 \_ 0 y 12 1 de Direct3D 12 \_ . 

Los requisitos mínimos de equipo para WARP son los mismos que para Windows Vista, en concreto:

-   CPU mínima de 800 MHz
-   No es necesario MMX, SSE o SSE2
-   Mínimo 512 MB de RAM

## <a name="how-to-use-warp"></a>Cómo usar WARP

Los componentes de Direct3D 10, 10,1, 11 y 12 pueden usar un tipo de controlador adicional que se puede especificar al crear el dispositivo (por ejemplo, al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ). Este tipo de controlador es [**D3D10 tipo \_ \_ \_ Warp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) o tipo de controlador [**D3D \_ \_ \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Cuando se especifica este tipo de controlador, el tiempo de ejecución crea un dispositivo WARP y no inicializa un dispositivo de hardware.

Dado que WARP usa la misma interfaz de software para Direct3D que el rasterizador de referencia, cualquier aplicación de Direct3D que pueda admitir la ejecución con el rasterizador de referencia se puede probar mediante WARP. Para usar WARP, cambie el nombre de D3d10warp.dll a D3d10ref.dll y colóquelo en la misma carpeta que el ejemplo o la aplicación. A continuación, cuando cambie a Ref, verá la representación de WARP.

Si cambia el nombre de WARP a D3d10ref.dll y lo coloca en C: \\ archivos de programa (x86) \\ SDK de Microsoft DirectX (junio 2010) \\ ejemplos de \\ C++ \\ \\ de Direct3D bin \\ x86, puede ejecutar todos los ejemplos de DirectX en Warp, bien haciendo clic en el botón "alternar referencia" en el ejemplo o ejecutando el ejemplo con/Ref especificado en la línea de comandos.

## <a name="recommended-application-types-for-warp"></a>Tipos de aplicación recomendados para WARP

Todas las aplicaciones que pueden usar Direct3D pueden usar WARP. Esto incluye los siguientes tipos de aplicaciones:

-   [Juegos esporádicos](#casual-games)
-   [Aplicaciones existentes que no son de juegos](#existing-non-gaming-applications)
-   [Juegos de representación avanzados](#advanced-rendering-games)
-   [Otras aplicaciones](#other-applications)

### <a name="casual-games"></a>Juegos esporádicos

Los juegos suelen tener requisitos de representación sencillos. Sin embargo, también requieren el uso de efectos visuales impresionantes que podrían necesitar aceleración de hardware. La mayoría de los títulos de juegos más vendidos para Windows son simulaciones o juegos esporádicos, ninguno de los cuales requiere gráficos de alto rendimiento. Sin embargo, ambos estilos de juegos se benefician enormemente de los gráficos modernos basados en sombreador y de la capacidad de escalar en el hardware.

### <a name="existing-non-gaming-applications"></a>Aplicaciones existentes que no son de juegos

Una gran cantidad de aplicaciones gráficas requiere un número mínimo de rutas de acceso de código en su capa de representación. WARP permite que estas aplicaciones implementen una única ruta de acceso de código de Direct3D que puede tener como destino un gran número de configuraciones de equipos.

### <a name="advanced-rendering-games"></a>Juegos de representación avanzados

Es posible que los desarrolladores de juegos quieran aislar los errores de representación específicos del controlador o la tarjeta gráfica. Por lo tanto, todos los juegos, incluso los juegos extremadamente gráficos exigentes, pueden beneficiarse de poder representar su contenido mediante el uso de WARP. Puede usar WARP para validar si los artefactos visuales que encuentre son errores de representación o problemas con el hardware o los controladores.

### <a name="other-applications"></a>Otras aplicaciones

Las aplicaciones de destino para WARP también incluyen aquellas que podrían no usar actualmente Direct3D 10 o Direct3D 10,1. Estas aplicaciones de destino incluyen aplicaciones que siempre deben funcionar en todos los equipos, aplicaciones de procesamiento de imágenes que no escriben versiones de CPU y GPU de algoritmos de procesamiento de imágenes, algoritmos de procesamiento de imágenes en los que la velocidad o el uso de la GPU no es fundamental, como la impresión y los emuladores y los entornos virtuales que muestran gráficos 3D avanzados.

## <a name="warp-architecture-and-performance"></a>Arquitectura y rendimiento de WARP

WARP se basa en el código base del rasterizador de referencia. Por lo tanto, WARP usa la misma interfaz de software para Direct3D 10 y versiones posteriores y DXGI. WARP se incluye en Windows 7 en el D3d10warp.dll, que se encuentra en las carpetas sistemas de Windows. Dos versiones de WARP se instalan en equipos de 64 bits, una versión x86 y x64. La versión x64 puede ejecutarse más rápido en determinadas circunstancias porque el generador de código contenido en WARP puede aprovechar los registros adicionales que están disponibles cuando los usuarios ejecutan aplicaciones de 64 bits.

WARP contiene los dos compiladores en tiempo real de alta velocidad siguientes:

-   Compilador de lenguaje intermedio de alto nivel que convierte el código de bytes HLSL y el estado de representación actual en un flujo optimizado de comandos vectoriales para las fases del sombreador de geometría (GS), del sombreador de vértices (VS) y del sombreador de píxeles (PS) de la canalización.
-   Generador de código Just-in-Time de alto rendimiento que puede tomar estos comandos y generar código de ensamblado SSE2, SSE 4.1, x86, x64, ARM y arm64 optimizado.

WARP usa el grupo de subprocesos y la administración compleja de tareas y el seguimiento de dependencias que se introdujeron en Windows Vista para permitir que todas las partes de la canalización de representación se distribuyan de manera eficaz en los núcleos de CPU disponibles.

WARP utiliza la representación aplazada. Es decir, WARP puede procesar por lotes los comandos para que la rasterización solo se produzca cuando haya suficientes datos disponibles para usar todos los recursos de la CPU de manera eficaz. El trabajo en el subproceso principal de la aplicación está minimizado para permitir que la aplicación envíe comandos lo más rápido posible. Si una aplicación también es multiproceso y usa el grupo de subprocesos, el trabajo se distribuirá uniformemente entre WARP y la aplicación.

El generador de código de ALABEo se ha optimizado para hacer el mejor uso de la arquitectura de CPU moderna. WARP se ejecuta en todos los equipos que pueden ejecutar Windows Vista y sistemas operativos posteriores, incluso si el equipo no es compatible con SSE. Sin embargo, WARP se ha optimizado para equipos que admiten SSE2. También contiene optimizaciones para arquitecturas específicas de procesadores AMD e Intel, así como compatibilidad con las extensiones SSE 4,1.

WARP no requiere la ejecución de hardware de gráficos. Puede ejecutarse incluso en situaciones en las que el hardware no está disponible o no se puede inicializar.

Las aplicaciones y los ejemplos que se diseñaron y crearon para ejecutarse en el hardware de Direct3D 10 y versiones posteriores sin ningún conocimiento de WARP probablemente funcionarán bien mediante WARP. Sin embargo, se recomienda reducir la configuración y la resolución de calidad tanto como sea posible para lograr velocidades de fotogramas que se puedan usar. Puede usar WARP para desarrollar y ajustar las aplicaciones que se ejecutan correctamente en el hardware y el software.

Dado que WARP usa varios núcleos de CPU, funciona mejor en CPU modernas de cuatro núcleos. WARP también se ejecuta significativamente más rápido en equipos con extensiones SSE 4.1 instaladas. Microsoft llevó a cabo un ajuste significativo en el rendimiento y las pruebas en los equipos con ocho o más núcleos y SSE 4.1 porque estos equipos de alta gama serán más comunes durante la vigencia de Windows 7 y los sistemas operativos posteriores.

Cuando se ejecuta WARP en la CPU, se compara con una tarjeta gráfica de varias maneras. La velocidad de bus frontal de una CPU suele ser de alrededor de 10 GB/s. Por el contrario, una tarjeta gráfica suele tener una memoria dedicada que usa de 20 a 100 GB/s o más de ancho de banda de gráficos. El hardware gráfico también tiene unidades de función fija que pueden realizar tareas complejas y costosas, como el filtrado de texturas, la descompresión de formato o las conversiones, de forma asincrónica con poca sobrecarga o costo energético. Realizar estas operaciones en una CPU típica es costoso en lo que respecta al consumo de energía y a los ciclos de rendimiento.

Los números de rendimiento típicos de un equipo con cuatro núcleos basados en Intel Penryn 3.0 GHz muestran que el ALABEo puede, en algunos casos, superar las GPU de gráficos integradas de Direct3D 10 y versiones posteriores integradas en una serie de pruebas comparativas. El hardware de gráficos discretos de low-end suele ser de 4 a 5 veces más rápido que WARP en la ejecución de estas pruebas comparativas. Estas GPU integradas de low-end o discretas tienen un uso mínimo de los recursos de la CPU. Las tarjetas de gráficos de gama media o alta son significativamente más rápidas que las de muchas aplicaciones, especialmente cuando una aplicación puede aprovechar el paralelismo y el ancho de banda de memoria que proporcionan estas tarjetas gráficas.

WARP no es un reemplazo del hardware de gráficos, especialmente en el caso de que el hardware independiente de Direct3D 10 de low-end y posterior sea económico. El objetivo de WARP es permitir que las aplicaciones se dirijan al hardware de nivel de Direct3D 10 sin tener rutas de acceso de código o requisitos de prueba significativamente diferentes, tanto si se ejecutan en hardware como en software.

En las dos tablas siguientes se muestran datos de ejemplo de ALABEo con varias CPU y tarjetas de gráficos.

En la primera tabla se muestran los datos de ejemplo de ALABEo con Direct3D 10 Crysis que se ejecutan en 800x600 con todos los valores de calidad en los niveles más bajos:

| CPU                         | Hora   | Promedio de FPS | FPS mín. | Marco mín. | FPS máx. | Fotograma máximo |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core a 3,0 GHz     | 271,57 | 7.36    | 3,46    | 1966      | 15,01   | 995       |
| Penryn 4 núcleos a 3,0 GHz      | 351,35 | 5,69    | 2.49    | 1967      | 10,95   | 980       |
| Penryn 2 núcleos a 3,0 GHz      | 573,98 | 3.48    | 1,35    | 1964      | 6,61    | 988       |
| Core 2 Duo a 2,6 GHz         | 707,19 | 2,83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo a 2,4 GHz         | 763,25 | 2.62    | 0,76    | 1964      | 4,70    | 984       |
| Core 2 Duo a 2,1 GHz         | 908,87 | 2,20    | 0,64    | 1965      | 3,72    | 986       |
| Xeon 8 núcleos a 2,0 GHz        | 424,04 | 4.72    | 1,84    | 1967      | 9,56    | 988       |
| AMD FX74 4 núcleos a 3,0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 core a 2,2 GHz | 664,69 | 3,01    | 0,53    | 1959      | 5.46    | 987       |

La segunda tabla muestra datos de ejemplo que ejecutan la misma prueba en una variedad de tarjetas gráficas:

| Tarjeta gráfica         | Hora   | Promedio de FPS | FPS mín. | Marco mín. | FPS máx. | Fotograma máximo |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 GT        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59,01  | 33,89   | 21,22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22,97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 PRO          | 67,04  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel contenido DX10 integrado | 386,94 | 5.17    | 1,74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Conformidad con WARP

WARP supera todas las pruebas de conformidad de los laboratorios de calidad de hardware de Windows (WHQL) estándar para validar los dispositivos de hardware de Direct3D.

WARP se ha probado con un conjunto de aplicaciones y pruebas comparativas de Direct3D 10 y Direct3D 10,1 y con ejemplos de SDK de DirectX, NVIDIA y AMD.

WARP utilizó la herramienta de análisis y depuración [PIX](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) para Windows en sus pruebas; Microsoft tiene una gran biblioteca de capturas de una sola trama de aplicaciones que se usan para comparar entre hardware y WARP. La mayoría de las imágenes aparecen casi idénticas entre hardware y WARP; Cuando a veces se producen pequeñas diferencias, se encuentran dentro de las tolerancias definidas por la especificación de Direct3D 10.