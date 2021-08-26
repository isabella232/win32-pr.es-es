---
title: Programación de 64 bits para desarrolladores de juegos
description: En este artículo se abordan problemas de compatibilidad y porte, y ayuda a los desarrolladores a facilitar su transición a plataformas de 64 bits.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439db3173e18206cb04875ab9c4422dbcedc7230508c8e98cf09b7fe27bfb9f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042435"
---
# <a name="64-bit-programming-for-game-developers"></a>Programación de 64 bits para desarrolladores de juegos

Los fabricantes de procesadores están enviando exclusivamente procesadores de 64 bits en sus equipos de escritorio e incluso los chips de la mayoría de los equipos portátiles admiten tecnología x64. Es importante que los desarrolladores de juegos aprovechen las mejoras que ofrecen los procesadores de 64 bits con sus nuevas aplicaciones y que las aplicaciones anteriores se ejecuten correctamente en los nuevos procesadores y las ediciones de 64 bits de Windows Vista y Windows 7. En este artículo se abordan problemas de compatibilidad y porte, y ayuda a los desarrolladores a facilitar su transición a plataformas de 64 bits.

Microsoft tiene actualmente los siguientes sistemas operativos de 64 bits:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (disponible para oem y desarrolladores a través de MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 solo está disponible como una edición de 64 bits.

 

-   [Diferencias en la memoria direccionable](#differences-in-addressable-memory)
-   [Especificación de direcciones grandes al compilar](#specifying-large-address-aware-when-building)
-   [Compatibilidad de aplicaciones de 32 bits en plataformas de 64 bits](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Posibles problemas de compatibilidad](#potential-compatibility-pitfalls)
-   [Porte de aplicaciones a plataformas de 64 bits](#porting-applications-to-64-bit-platforms)
-   [Generación de perfiles y optimización de aplicaciones porteadas](#profiling-and-optimization-of-ported-applications)
-   [Código administrado en un sistema operativo de 64 bits](#managed-code-on-a-64-bit-operating-system)
-   [Implicaciones de rendimiento de ejecutar un sistema operativo de 64 bits](#performance-implications-of-running-a-64-bit-operating-system)
-   [Resumen](#summary)

## <a name="differences-in-addressable-memory"></a>Diferencias en la memoria direccionable

Lo primero que observan la mayoría de los desarrolladores es que los procesadores de 64 bits proporcionan un gran salto en la cantidad de memoria física y virtual que se puede abordar.

-   Las aplicaciones de 32 bits en plataformas de 32 bits pueden abordar hasta 2 GB.
-   Las aplicaciones de 32 bits creadas con la marca de vinculador /LARGEADDRESSAWARE:YES en Windows XP de 32 bits o Windows Server 2003 con la opción de arranque especial /3gb pueden abordar hasta 3 GB. Esto restringe el kernel a solo 1 GB, lo que puede provocar errores en algunos controladores o servicios.
-   Las aplicaciones de 32 bits creadas con la marca de vinculador /LARGEADDRESSAWARE:YES en las ediciones de 32 bits de Windows Vista, Windows Server 2008 y Windows 7 pueden dirigir la memoria hasta el número especificado por el elemento IncreaseUserVa de los datos de configuración de arranque (BCD). IncreaseUserVa puede tener un valor que va desde 2048, el valor predeterminado, hasta 3072 (que coincide con la cantidad de memoria configurada por la opción de arranque /3gb en Windows XP). El resto de 4 GB se asigna al kernel y puede dar lugar a errores en las configuraciones del controlador y del servicio.

    Para obtener más información sobre BCD, vea [datos de la configuración de arranque (BCD)](https://msdn.microsoft.com/library/aa362692.aspx) en MSDN.

-   Las aplicaciones de 32 bits en plataformas de 64 bits pueden abordar hasta 2 GB o hasta 4 GB con la marca del vinculador /LARGEADDRESSAWARE:YES.
-   Las aplicaciones de 64 bits usan 43 bits para el direccionamiento, lo que proporciona 8 TB de dirección virtual para las aplicaciones y 8 TB reservados para el kernel.

Además de la memoria, las aplicaciones de 64 bits que usan E/S de archivos asignados a memoria se benefician en gran parte del aumento del espacio de direcciones virtuales. La arquitectura de 64 bits también ha mejorado el rendimiento de punto flotante y un paso más rápido de los parámetros. Los procesadores de cuatro bits tienen el doble de registros, tanto de uso general como de extensiones SIMD de streaming (SSE), así como compatibilidad con conjuntos de instrucciones SSE y SSE2. muchos procesadores de 64 bits incluso admiten conjuntos de instrucciones SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Especificación de direcciones grandes al compilar

Es una buena práctica especificar una dirección grande al compilar aplicaciones de 32 bits, mediante el uso de la marca del vinculador /LARGEADDRESSAWARE, incluso si la aplicación no está pensada para una plataforma de 64 bits, debido a las ventajas que se ganan sin costo alguno. Como se explicó anteriormente, habilitar esta marca para una compilación permite que un programa de 32 bits acceda a más memoria con opciones de arranque especiales en un sistema operativo de 32 bits o en un sistema operativo de 64 bits. Sin embargo, los desarrolladores deben tener cuidado de que no se realizan suposiciones de puntero, como suponer que el bit alto nunca se establece en un puntero de 32 bits. En general, habilitar la marca /LARGEADDRESSAWARE es un procedimiento recomendado.

Las aplicaciones de treinta y dos bits que tienen en cuenta direcciones grandes pueden determinar en tiempo de ejecución cuánto espacio total de direcciones virtuales está disponible para ellas con la configuración actual del sistema operativo mediante una llamada a [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex). El resultado de ullTotalVirtual oscilará entre 2147352576 bytes (2 GB) y 4294836224 bytes (4 GB). Los valores mayores que 3221094400 (3 GB) solo se pueden obtener en ediciones de 64 bits de Windows. Por ejemplo, si IncreaseUserVa tiene un valor de 2560, el resultado es ullTotalVirtual con un valor de 2684223488 bytes.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilidad de aplicaciones de 32 bits en plataformas de 64 bits

Los sistemas operativos Windows de cuatro bits son binarios compatibles con la arquitectura IA32 y la mayoría de las API que usan las aplicaciones de 32 bits están disponibles a través de Windows de 32 bits en Windows de 64 bits Emulator, WOW64. WOW64 ayuda a garantizar que estas API funcionarán según lo previsto.

WOW64 tiene una capa de ejecución que controla la marshalling de datos de 32 bits. WOW64 redirige las solicitudes de archivo DLL, redirige algunas ramas del Registro para aplicaciones de 32 bits y refleja algunas ramas del Registro para aplicaciones de 32 y 64 bits.

Puede encontrar más información sobre WOW64 en Detalles de implementación de [WOW64](/windows/desktop/WinProg64/wow64-implementation-details) en MSDN. Para obtener procedimientos recomendados para compilar aplicaciones que se ejecutan en WOW64, consulte Procedimientos recomendados para [WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) en Windows Hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Posibles problemas de compatibilidad

La mayoría de las aplicaciones desarrolladas para una plataforma de 32 bits se ejecutarán sin problemas en una plataforma de 64 bits. Algunas aplicaciones podrían tener problemas, entre los que se incluyen los siguientes:

-   Todos los controladores de las ediciones de 64 bits Windows sistemas operativos deben ser versiones de 64 bits. Requerir nuevos controladores de 64 bits tiene implicaciones para los esquemas de protección de copia que se basan en controladores antiguos. Tenga en cuenta que los controladores en modo kernel deben estar firmados por Authenticode para que los carguen las ediciones de 64 bits de Windows.
-   Los procesos de 64 bits no pueden cargar archivos DLL de 32 bits y los procesos de 32 bits no pueden cargar archivos DLL de 64 bits. Los desarrolladores deben asegurarse de que las versiones de 64 bits de archivos DLL de terceros estén disponibles antes de continuar con el desarrollo. Si debe usar un archivo DLL de 32 bits en un proceso de 64 bits, Windows se puede usar la comunicación entre procesos (IPC). Los componentes COM también pueden usar servidores fuera de proceso y la programación para comunicarse entre límites, pero esto puede producir una penalización en el rendimiento.
-   Muchos procesadores x64 también son procesadores de varios núcleos y los desarrolladores deben probar cómo afecta esto a sus aplicaciones heredadas. Puede encontrar más información sobre los procesadores de varios núcleos y las implicaciones para las aplicaciones de juegos en [Game Timing y Procesadores multinúcleo.](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)
-   Las aplicaciones también deben llamar a [**SHGetFolderPath para detectar**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) rutas de acceso de archivo, ya que algunos nombres de carpeta han cambiado en algunos casos. Por ejemplo, CSIDL PROGRAM FILES devolvería \_ \_ "C: Archivos de \\ programa(x86)" para una aplicación de 32 bits que se ejecuta en una plataforma de 64 bits en lugar de "C: Archivos de \\ programa". Los desarrolladores deben tener en cuenta cómo funcionan las funcionalidades de redireccionamiento y reflexión del emulador WOW64.

Además, los desarrolladores deben tener cuidado con los programas de 16 bits que podrían seguir usando. WOW64 no puede controlar aplicaciones de 16 bits; esto incluye los instaladores antiguos y todos los programas MS-DOS.

> [!Note]  
> Los problemas de compatibilidad más comunes son los instaladores que ejecutan código de 16 bits y no tienen controladores de 64 bits para los esquemas de protección de copia.

 

En la sección siguiente se de abordan problemas relacionados con la porción de código a código nativo de 64 bits para desarrolladores que desean asegurarse de que sus programas heredados funcionan en plataformas de 64 bits. También es para desarrolladores que no están familiarizados con la programación de 64 bits.

## <a name="porting-applications-to-64-bit-platforms"></a>Porte de aplicaciones a plataformas de 64 bits

Tener las herramientas y bibliotecas adecuadas le ayudará a facilitar la transición del desarrollo de 32 bits a 64 bits. El SDK de DirectX 9 tiene bibliotecas para admitir proyectos basados en x86 y x64. Microsoft Visual Studio 2005 y Visual Studio 2008 admiten la generación de código para x86 y x64, y incluyen bibliotecas optimizadas para generar código x64. Sin embargo, también será necesario que los desarrolladores distribuyan los entornos de ejecución de Visual C con sus aplicaciones. Tenga en cuenta que las ediciones Express de Visual Studio 2005 y Visual Studio 2008 no incluyen el compilador x64, pero sí las ediciones Standard, Professional y Team System.

Los desarrolladores que tienen como destino plataformas de 32 bits pueden prepararse para el desarrollo de 64 bits para facilitar su transición más adelante. Al compilar proyectos de 32 bits, los desarrolladores deben usar la marca /Wp64, lo que provocará la generación de advertencias sobre problemas que afectan a la portabilidad. Cambiar a bibliotecas y herramientas de 64 bits probablemente generará muchos errores de compilación nuevos inicialmente. por lo tanto, es aconsejable cambiar las herramientas y bibliotecas neutrales de bits y corregir las advertencias antes de cambiar a una compilación de 64 bits.

Sin embargo, cambiar las herramientas, cambiar las bibliotecas y usar determinadas marcas del compilador no será suficiente. Las suposiciones en los estándares de codificación deben volver a evaluarse para asegurarse de que los estándares de codificación actuales no permiten problemas de portabilidad. Los problemas de portabilidad pueden incluir truncamiento de punteros, tamaño y alineación de tipos de datos, dependencia de archivos DLL de 32 bits, uso de API heredadas, código de ensamblado y archivos binarios antiguos.

> [!Note]  
> Visual C++ 2010 incluye los encabezados stdint.h y cstdint C99 que definen los tipos de portabilidad estándar int32 \_ t, uint32 \_ t, int64 \_ t, uint64 \_ t, intptr \_ t y uintptr \_ t. El uso de estos junto con los tipos de datos t de ptrdiff estándar y size t puede ser preferible a los tipos de portabilidad de Windows que se usan a continuación para mejorar la portabilidad \_ \_ del código.

 

Entre los principales problemas de porte se incluyen los siguientes:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Truncamiento de puntero**
</dt> <dd>

Los punteros son de 64 bits en un sistema operativo de 64 bits, por lo que la conversión de punteros a otros tipos de datos puede dar lugar a truncamiento y la aritmética de punteros puede dar lugar a daños. El uso de la marca /Wp64 normalmente proporcionará una advertencia sobre este tipo de problema, pero el uso de tipos polimórficos (INT \_ PTR, DWORD \_ PTR, SIZE \_ T, UINT PTR, entre otros) cuando la conversión de tipos de puntero es una buena práctica para evitar este problema por \_ completo. Dado que los punteros son de 64 bits en nuevas plataformas, los desarrolladores deben comprobar el orden de los punteros y los tipos de datos de las clases y estructuras para reducir o eliminar el relleno.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Tipos de datos y archivos binarios**
</dt> <dd>

Aunque los punteros aumentan de 32 bits a 64 en una plataforma de 64 bits, otros tipos de datos no. Los tipos de datos de precisión fija (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) se pueden usar en lugares donde se debe conocer el tamaño del tipo de datos; por ejemplo, en una estructura de archivos binarios. Los cambios en el tamaño del puntero y la alineación de datos requieren un control especial para garantizar la compatibilidad de 32 bits a 64 bits. Puede encontrar más información en [Getting Ready for 64-bit Windows: The New Data Types](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**API anteriores de Win32 y alineación de datos**
</dt> <dd>

Algunas API de Win32 han quedado en desuso y se han reemplazado por llamadas API más neutras, como SetWindowLongPtr en lugar de SetWindowLong.

La penalización del rendimiento de los accesos no alineados es mayor en la plataforma x64 que en una plataforma x86. Las macros TYPE \_ ALIGNMENT(t) y FIELD OFFSET(t, member) se pueden usar para determinar la información de alineación que el \_ código puede usar directamente. El uso correcto de estas macros mencionadas anteriormente debe eliminar posibles penalizaciones de acceso no alineadas.

Puede encontrar más información sobre la macro TYPE ALIGNMENT, la macro FIELD OFFSET y la información general de programación de 64 bits en \_ \_ 64 bits Windows [Programming: Migration Sugerencias: Additional Considerations](/windows/desktop/WinProg64/additional-considerations) and [Getting Ready for 64-bit Windows: Rules for Using Pointers](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Código de ensamblado**
</dt> <dd>

El código de ensamblado en línea no se admite en plataformas de 64 bits y debe reemplazarse. Los cambios en la arquitectura pueden haber cambiado los cuellos de botella de la aplicación y C/C++ u intrínsecos pueden lograr resultados similares con código que es más fácil de leer. La práctica más aconsejable es cambiar todo el código de ensamblado a C o C++. Los intrínsecos se pueden usar en lugar del código de ensamblado, pero solo se deben usar una vez realizada la generación de perfiles y el análisis completos.

El x87, MMX y 3DNow! Los conjuntos de instrucciones están en desuso en modos de 64 bits. Los conjuntos de instrucciones siguen estando presentes por compatibilidad con versiones anteriores para el modo de 32 bits. sin embargo, para evitar problemas de compatibilidad en el futuro, no se recomienda su uso en proyectos actuales y futuros.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**API en desuso**
</dt> <dd>

Se han eliminado algunas API anteriores de DirectX para aplicaciones nativas de 64 bits: DirectPlay 4 y versiones anteriores, DirectDraw 6 y versiones anteriores, Direct3D 8 y versiones anteriores, y DirectInput 7 y versiones anteriores. Además, la API principal de DirectMusic está disponible para las aplicaciones nativas de 64 bits, pero la capa de rendimiento y el productor de DirectProducto están en desuso.

Visual Studio advertencias de desuso y estos cambios no son un problema para los desarrolladores que usan las API más recientes.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Generación de perfiles y optimización de aplicaciones porteadas

Todos los desarrolladores deben volver a perfiles de las aplicaciones que se van a porte a nuevas arquitecturas. Muchas aplicaciones que se van a porte a plataformas de 64 bits tendrán perfiles de rendimiento diferentes de sus versiones de 32 bits. Los desarrolladores deben ejecutar pruebas de rendimiento de 64 bits antes de evaluar lo que se debe optimizar. La buena noticia es que muchas optimizaciones tradicionales funcionan en plataformas de 64 bits. Además, los compiladores de 64 bits también pueden realizar muchas optimizaciones con el uso correcto de marcas del compilador y sugerencias de codificación.

Algunas estructuras pueden tener sus tipos de datos internos reordenados para conservar el espacio de memoria y mejorar el almacenamiento en caché. Los índices de matriz se pueden usar en lugar de un puntero completo de 64 bits en algunos casos. La marca /fp:fast puede mejorar la optimización y vectorización de punto flotante. El \_ \_ uso de restrict, declspec(restrict) y declspec(noalias) puede ayudar al compilador a resolver el alias y mejorar el uso del archivo de registro.

Puede encontrar más información sobre /fp:fast en [/fp (Especificar Floating-Point comportamiento).](/cpp/build/reference/fp-specify-floating-point-behavior)

Puede encontrar más información \_ \_ sobre la restricción en [Modificadores específicos de Microsoft](/cpp/cpp/microsoft-specific-modifiers).

Puede encontrar más información sobre declspec(restrict) en [Procedimientos recomendados de optimización.](/cpp/build/optimization-best-practices)

Puede encontrar más información sobre declspec(noalias) en [ \_ \_ declspec(noalias).](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx)

## <a name="managed-code-on-a-64-bit-operating-system"></a>Código administrado en un sistema operativo de 64 bits

Muchos desarrolladores de juegos usan código administrado en su cadena de herramientas, por lo que puede resultar útil comprender cómo se comporta en un sistema operativo de 64 bits. El código administrado es neutro en el conjunto de instrucciones, por lo que cuando se ejecuta una aplicación administrada en un sistema operativo de 64 bits, Common Language Runtime (CLR) puede ejecutarlo como un proceso de 32 o 64 bits. De forma predeterminada, CLR ejecuta aplicaciones administradas como de 64 bits y deben funcionar bien sin problemas. Sin embargo, si la aplicación depende de un archivo DLL nativo de 32 bits, se producirá un error en la aplicación cuando intente llamar a este archivo DLL. Un proceso de 64 bits necesita código de 64 bits y no se puede llamar a un archivo DLL de 32 bits desde un proceso de 64 bits. La mejor solución a largo plazo es compilar también el código nativo como de 64 bits, pero una solución a corto plazo perfectamente razonable es simplemente marcar la aplicación administrada como para x86 solo mediante la marca de compilación /platform:x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implicaciones de rendimiento de ejecutar un sistema operativo de 64 bits

Dado que los procesadores con arquitectura AMD64 e Intel 64 pueden ejecutar instrucciones de 32 bits de forma nativa, pueden ejecutar aplicaciones de 32 bits a velocidad completa, incluso en un sistema operativo de 64 bits. Hay un costo moderado por convertir parámetros entre 32 y 64 bits al llamar a funciones del sistema operativo, pero este costo suele ser insignificante. Esto significa que no debería ver ninguna ralentización al ejecutar aplicaciones de 32 bits en un sistema operativo de 64 bits.

Al compilar aplicaciones como de 64 bits, los cálculos son más complicados. Un programa de 64 bits usa punteros de 64 bits y sus instrucciones son ligeramente mayores, por lo que el requisito de memoria aumenta ligeramente. Esto puede provocar una ligera disminución del rendimiento. Por otro lado, tener el doble de registros y tener la capacidad de realizar cálculos enteros de 64 bits en una sola instrucción a menudo será mayor que compensar. El resultado neto es que una aplicación de 64 bits podría ejecutarse ligeramente más lenta que la misma aplicación compilada como de 32 bits, pero a menudo se ejecutará ligeramente más rápido.

## <a name="summary"></a>Resumen

Las arquitecturas de cuatro bits permiten a los desarrolladores insertar las limitaciones sobre el aspecto, el sonido y el juego de los juegos. Sin embargo, la transición de la programación de 32 bits a la programación de 64 bits no es trivial. Al comprender las diferencias entre los dos y usar las herramientas más nuevas, la transición a plataformas de 64 bits puede ser más fácil y rápida.

Puede encontrar más información sobre la programación de 64 bits [en Visual C++ Developer Center: Programación de 64 bits.](https://msdn.microsoft.com/vstudio//aa336463.aspx)

 

 