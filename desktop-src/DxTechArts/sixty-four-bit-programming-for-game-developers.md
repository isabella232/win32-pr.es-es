---
title: programación de 64 bits para desarrolladores de juegos
description: En este artículo se abordan los problemas de compatibilidad y traslado, y ayuda a los desarrolladores a facilitar su transición a las plataformas de 64 bits.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e57ea1b3cc3272ca40465df31a04244d99e68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078073"
---
# <a name="64-bit-programming-for-game-developers"></a>programación de 64 bits para desarrolladores de juegos

Los fabricantes de procesadores están enviando exclusivamente procesadores de 64 bits en sus equipos de escritorio, e incluso los chipsets de la mayoría de los equipos portátiles admiten la tecnología x64. Es importante que los desarrolladores de juegos aprovechen las mejoras que ofrecen los procesadores de 64 bits con sus aplicaciones nuevas y para asegurarse de que sus aplicaciones anteriores se ejecutan correctamente en los nuevos procesadores y en las ediciones de 64 bits de Windows Vista y Windows 7. En este artículo se abordan los problemas de compatibilidad y traslado, y ayuda a los desarrolladores a facilitar su transición a las plataformas de 64 bits.

Microsoft tiene actualmente los siguientes sistemas operativos de 64 bits:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (disponible para OEM y para desarrolladores a través de MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 solo está disponible como edición de 64 bits.

 

-   [Diferencias en la memoria direccionable](#differences-in-addressable-memory)
-   [Especificar el reconocimiento de direcciones grandes al compilar](#specifying-large-address-aware-when-building)
-   [Compatibilidad de aplicaciones de 32 bits en plataformas de 64 bits](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Posibles errores de compatibilidad](#potential-compatibility-pitfalls)
-   [Migración de aplicaciones a plataformas de 64 bits](#porting-applications-to-64-bit-platforms)
-   [Generación de perfiles y optimización de aplicaciones trasladadas](#profiling-and-optimization-of-ported-applications)
-   [Código administrado en un sistema operativo de 64 bits](#managed-code-on-a-64-bit-operating-system)
-   [Implicaciones de rendimiento de la ejecución de un sistema operativo de 64 bits](#performance-implications-of-running-a-64-bit-operating-system)
-   [Resumen](#summary)

## <a name="differences-in-addressable-memory"></a>Diferencias en la memoria direccionable

Lo primero que la mayoría de los desarrolladores tiene en cuenta es que los procesadores de 64 bits proporcionan un gran avance en la cantidad de memoria física y virtual que se puede solucionar.

-   las aplicaciones de 32 bits en plataformas de 32 bits pueden ocupar hasta 2 GB.
-   las aplicaciones de 32 bits compiladas con la marca del enlazador/LARGEADDRESSAWARE: YES en Windows XP o Windows Server 2003 de 32 bits con la opción de arranque/3GB especial pueden tener una dirección de hasta 3 GB. Esto restringe el kernel a solo 1 GB, lo que puede provocar errores en algunos controladores o servicios.
-   las aplicaciones de 32 bits compiladas con la marca del enlazador/LARGEADDRESSAWARE: YES en las ediciones de 32 bits de Windows Vista, Windows Server 2008 y Windows 7 pueden direccionar la memoria hasta el número especificado por el elemento IncreaseUserVa de datos de la configuración de arranque (BCD). IncreaseUserVa puede tener un valor comprendido entre 2048, el valor predeterminado, 3072 (que coincide con la cantidad de memoria configurada por la opción de arranque/3GB en Windows XP). El resto de 4 GB se asigna al kernel y puede dar lugar a errores en las configuraciones de controlador y servicio.

    Para obtener más información sobre BCD, consulte [datos de la configuración de arranque (BCD)](https://msdn.microsoft.com/library/aa362692.aspx) en MSDN.

-   las aplicaciones de 32 bits en plataformas de 64 bits pueden direccionar hasta 2 GB o hasta 4 GB con la marca del enlazador/LARGEADDRESSAWARE: YES.
-   las aplicaciones de 64 bits usan 43 bits para el direccionamiento, que proporciona 8 TB de direcciones virtuales para las aplicaciones y 8 TB reservados para el kernel.

Además de la memoria, las aplicaciones de 64 bits que usan la e/s de archivos asignada a la memoria se benefician mucho del mayor espacio de direcciones virtuales. La arquitectura de 64 bits también tiene un rendimiento de punto flotante mejorado y un paso más rápido de los parámetros. Los procesadores de 64 bits tienen el doble del número de registros, tanto de los tipos de uso general como de las extensiones SIMD de streaming (SSE), así como la compatibilidad con conjuntos de instrucciones SSE y SSE2. muchos procesadores de 64 bits incluso admiten conjuntos de instrucciones SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Especificar el reconocimiento de direcciones grandes al compilar

Es recomendable especificar una dirección de gran tamaño al compilar aplicaciones de 32 bits mediante el uso de la marca del enlazador/LARGEADDRESSAWARE, incluso si la aplicación no está pensada para una plataforma de 64 bits, debido a las ventajas que se obtienen sin costo alguno. Como se explicó anteriormente, la habilitación de esta marca para una compilación permite a un programa de 32 bits tener acceso a más memoria con opciones de arranque especiales en un sistema operativo de 32 bits o en un sistema operativo de 64 bits. Sin embargo, los desarrolladores deben tener cuidado de no realizar suposiciones de puntero, como suponiendo que el valor de High-bit nunca se establece en un puntero de 32 bits. En general, la habilitación de la marca/LARGEADDRESSAWARE es una buena práctica.

Las aplicaciones de 32 bits que reconocen gran cantidad de direcciones pueden determinar en tiempo de ejecución cuánto espacio de direcciones virtuales está disponible para ellos con la configuración del sistema operativo actual llamando a [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex). El resultado de ullTotalVirtual va de 2147352576 bytes (2 GB) a 4294836224 bytes (4 GB). Los valores mayores que 3221094400 (3 GB) solo se pueden obtener en las ediciones de 64 bits de Windows. Por ejemplo, si IncreaseUserVa tiene un valor de 2560, el resultado es ullTotalVirtual con un valor de 2684223488 bytes.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilidad de aplicaciones de 32 bits en plataformas de 64 bits

Los sistemas operativos Windows de 64 bits son compatibles con la arquitectura de IA32 y la mayoría de las API que usan las aplicaciones de 32 bits están disponibles a través del emulador de Windows 32 bits en Windows 64-bit, WOW64. WOW64 ayuda a garantizar que estas API funcionen según lo previsto.

WOW64 tiene una capa de ejecución que controla la serialización de datos de 32 bits. WOW64 redirige las solicitudes de archivos DLL, redirige algunas ramas del registro para las aplicaciones de 32 bits y refleja algunas ramas del registro para las aplicaciones de 32 y 64 bits.

Puede encontrar más información sobre WOW64 en detalles de la [implementación de WOW64](/windows/desktop/WinProg64/wow64-implementation-details) en MSDN. Para ver los procedimientos recomendados para compilar aplicaciones que se ejecutan en WOW64, consulte [procedimientos recomendados para WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) en el centro de desarrollo de hardware de Windows.

### <a name="potential-compatibility-pitfalls"></a>Posibles errores de compatibilidad

La mayoría de las aplicaciones desarrolladas para una plataforma de 32 bits se ejecutarán sin problemas en una plataforma de 64 bits. Algunas aplicaciones pueden tener problemas, entre los que se incluyen los siguientes:

-   Todos los controladores para las ediciones de 64 bits de los sistemas operativos Windows deben ser versiones de 64 bits. Requerir nuevos controladores de 64 bits tiene implicaciones en los esquemas de protección de copia que se basan en controladores antiguos. Tenga en cuenta que los controladores en modo kernel deben estar firmados con Authenticode para ser cargados por las ediciones de 64 bits de Windows.
-   los procesos de 64 bits no pueden cargar archivos dll de 32 bits y los procesos de 32 bits no pueden cargar archivos dll de 64 bits. Los desarrolladores deben asegurarse de que las versiones de 64 bits de los archivos dll de terceros estén disponibles antes de continuar con el desarrollo. Si debe usar una DLL de 32 bits en un proceso de 64 bits, se puede usar la comunicación entre procesos de Windows (IPC). Los componentes COM también pueden hacer uso de servidores fuera de proceso y de cálculo de referencias para la comunicación entre límites, pero si lo hace, se puede producir una reducción del rendimiento.
-   Muchos procesadores x64 son también procesadores de varios núcleos y los desarrolladores deben probar cómo esto afecta a sus aplicaciones heredadas. Puede encontrar más información sobre los procesadores de varios núcleos y las implicaciones de las aplicaciones de juegos en [procesadores de control de tiempo y multinúcleo](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).
-   Las aplicaciones también deben llamar a [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para detectar rutas de acceso de archivo, ya que algunos nombres de carpeta han cambiado en ciertos casos. Por ejemplo, \_ los archivos de programa CSIDL \_ devolverían "c: \\ archivos de programa (x86)" para una aplicación de 32 bits que se ejecuta en una plataforma de 64 bits en lugar de "C: \\ archivos de programa". Los desarrolladores deben ser conscientes de cómo funcionan las capacidades de redirección y reflexión del emulador de WOW64.

Además, los desarrolladores deben tener cuidado con los programas de 16 bits que puedan seguir usando. WOW64 no puede controlar las aplicaciones de 16 bits; Esto incluye los instaladores anteriores y todos los programas de MS-DOS.

> [!Note]  
> Los problemas de compatibilidad más comunes son los instaladores que ejecutan código de 16 bits y no tienen controladores de 64 bits para los esquemas de protección de copia.

 

En la siguiente sección se describen los problemas relacionados con el traslado de código a nativo de 64 bits para los desarrolladores que desean asegurarse de que sus programas heredados funcionan en plataformas de 64 bits. También es para los desarrolladores que no están familiarizados con la programación de 64 bits.

## <a name="porting-applications-to-64-bit-platforms"></a>Migración de aplicaciones a plataformas de 64 bits

Tener las herramientas y las bibliotecas adecuadas le ayudará a facilitar la transición del desarrollo de 32 a 64 bits. El SDK de DirectX 9 tiene bibliotecas que admiten proyectos basados en x86 y x64. Microsoft Visual Studio 2005 y Visual Studio 2008 admiten la generación de código para x86 y x64, y incluyen bibliotecas optimizadas para generar código x64. Sin embargo, también será necesario que los desarrolladores distribuyan los tiempos de ejecución de Visual C con sus aplicaciones. Tenga en cuenta que las ediciones Express de Visual Studio 2005 y Visual Studio 2008 no incluyen el compilador x64, pero las ediciones Standard, Professional y Team System.

Los desarrolladores que tienen como destino plataformas de 32 bits pueden prepararse para el desarrollo de 64 bits con el fin de facilitar su transición más adelante. Al compilar proyectos de 32 bits, los desarrolladores deben usar la marca/Wp64, lo que provocará la generación de advertencias sobre los problemas que afectan a la portabilidad. Si cambia a las herramientas y las bibliotecas de 64 bits, es probable que genere muchos errores de compilación nuevos inicialmente; por lo tanto, se recomienda cambiar las bibliotecas y herramientas independientes de bits y corregir cualquier advertencia antes de cambiar a una compilación de 64 bits.

No obstante, el cambio de herramientas, el cambio de bibliotecas y el uso de ciertas marcas de compilador no serán suficientes. Las suposiciones de los estándares de codificación se deben volver a evaluar para asegurarse de que los estándares de codificación actuales no permiten problemas de portabilidad. Los problemas de portabilidad pueden incluir el truncamiento de punteros, el tamaño y la alineación de los tipos de datos, la dependencia de los archivos dll de 32 bits, el uso de las API heredadas, el código de ensamblado y los archivos binarios antiguos.

> [!Note]  
> Visual C++ 2010 incluye los encabezados stdint. h y cstdint C99 que definen los tipos de portabilidad estándar Int32 \_ t, UInt32 \_ t, Int64 \_ t, UInt64 \_ t, IntPtr \_ t y UIntPtr \_ t. El uso de estas junto con los \_ tipos de datos estándar ptrdiff t y size \_ t puede ser preferible a los tipos de portabilty de Windows que se usan a continuación para mejorar la portabilidad del código.

 

Entre los principales problemas de migración se incluyen los siguientes:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Truncamiento de puntero**
</dt> <dd>

Los punteros son de 64 bits en un sistema operativo de 64 bits, por lo que la conversión de punteros a otros tipos de datos puede dar lugar a un truncamiento, y la aritmética de punteros puede producir daños. El uso de la marca/Wp64 normalmente proporcionará una advertencia sobre este tipo de problema, pero el uso de tipos polimórficos (INT \_ ptr, DWORD \_ ptr, size \_ T, uint \_ ptr, etc.) al convertir tipos de puntero es una buena práctica para ayudar a evitar todo este problema. Como los punteros son de 64 bits en plataformas nuevas, los desarrolladores deben comprobar el orden de los punteros y los tipos de datos de las clases y estructuras para reducir o eliminar el relleno.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Tipos de datos y archivos binarios**
</dt> <dd>

Aunque los punteros aumentan de 32 bits a 64 en una plataforma de 64 bits, otros tipos de datos no. Se pueden usar tipos de datos de precisión fija (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) en lugares donde se debe conocer el tamaño del tipo de datos; por ejemplo, en una estructura de archivos binarios. Los cambios en el tamaño de puntero y la alineación de datos requieren un tratamiento especial para garantizar la compatibilidad de 32 bits a 64 bits. Puede encontrar más información en [preparación para Windows de 64 bits: los nuevos tipos de datos](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**Antiguas API de Win32 y alineación de datos**
</dt> <dd>

Algunas API de Win32 han quedado en desuso y se han reemplazado por llamadas API más neutras como SetWindowLongPtr en lugar de SetWindowLong.

La reducción del rendimiento para los accesos no alineados es mayor en la plataforma x64 que en una plataforma x86. La alineación de tipos \_ (t) y las \_ macros de desplazamiento de campo (t, Member) se pueden utilizar para determinar la información de alineación que puede usar directamente el código. El uso correcto de estas macros anteriores debe eliminar posibles penalizaciones de acceso no alineadas.

Puede encontrar más información sobre la macro de alineación de tipos \_ , la macro de desplazamiento de campo \_ y la información general de programación de 64 bits en [programación de Windows de 64 bits: sugerencias de migración: consideraciones adicionales](/windows/desktop/WinProg64/additional-considerations) y preparación [para Windows de 64 bits: reglas para usar punteros](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Código de ensamblado**
</dt> <dd>

El código de ensamblado alineado no se admite en las plataformas de 64 bits y debe reemplazarse. Los cambios en la arquitectura pueden haber cambiado los cuellos de botella de la aplicación y C/C++ o intrínsecos pueden conseguir resultados similares con código que es más fácil de leer. La práctica más recomendable es cambiar todo el código de ensamblado a C o C++. Los intrínsecos se pueden usar en lugar del código de ensamblado, pero solo deben usarse después de haber realizado la generación de perfiles y el análisis completos.

Los de x87, MMX y 3DNow! los conjuntos de instrucciones están en desuso en los modos de 64 bits. Los conjuntos de instrucciones siguen presentes para mantener la compatibilidad con versiones anteriores del modo de 32 bits; sin embargo, para evitar problemas de compatibilidad en el futuro, no se recomienda su uso en proyectos actuales y futuros.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**API en desuso**
</dt> <dd>

Algunas API de DirectX anteriores se han quitado de las aplicaciones nativas de 64 bits: DirectPlay 4 y versiones anteriores, DirectDraw 6 y versiones anteriores, Direct3D 8 y versiones anteriores, y DirectInput 7 y versiones anteriores. Además, la API principal de DirectMusic está disponible para las aplicaciones nativas de 64 bits, pero el productor de DirectMusic y el nivel de rendimiento están desusados.

Visual Studio emite advertencias de desuso y estos cambios no son un problema para los desarrolladores que usan las API más recientes.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Generación de perfiles y optimización de aplicaciones trasladadas

Todos los desarrolladores deben volver a generar perfiles de las aplicaciones que se van a migrar a nuevas arquitecturas. Muchas aplicaciones que se trasladan a plataformas de 64 bits tendrán distintos perfiles de rendimiento de sus versiones de 32 bits. Los desarrolladores deben ejecutar pruebas de rendimiento de 64 bits antes de evaluar lo que se debe optimizar. La buena noticia de esto es que muchas optimizaciones tradicionales funcionan en plataformas de 64 bits. Además, los compiladores de 64 bits también pueden realizar muchas optimizaciones con el uso correcto de las marcas de compilador y las sugerencias de codificación.

Algunas estructuras pueden tener sus tipos de datos internos reordenados para conservar el espacio de memoria y mejorar el almacenamiento en caché. Los índices de matriz se pueden usar en lugar de un puntero completo de 64 bits en algunos casos. La marca/FP: Fast puede mejorar la optimización de punto flotante y la vectorización. \_ \_ El uso de Restrict, declspec (Restrict) y declspec (noalias) puede ayudar al compilador a resolver alias y mejorar el uso del archivo de registro.

Puede encontrar más información sobre/FP: Fast en [/FP (especificar el comportamiento de Floating-Point)](/cpp/build/reference/fp-specify-floating-point-behavior).

Puede encontrar más información sobre \_ \_ Restrict en [Modificadores específicos de Microsoft](/cpp/cpp/microsoft-specific-modifiers).

Puede encontrar más información sobre declspec (Restrict) en [procedimientos recomendados de optimización](/cpp/build/optimization-best-practices).

Puede encontrar más información sobre declspec (noalias) en [ \_ \_ declspec (noalias)](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx).

## <a name="managed-code-on-a-64-bit-operating-system"></a>Código administrado en un sistema operativo de 64 bits

El código administrado lo usan muchos desarrolladores de juegos en su cadena de herramientas, por lo que es útil entender cómo se comporta en un sistema operativo de 64 bits. El código administrado es un conjunto de instrucciones neutro, por lo que cuando se ejecuta una aplicación administrada en un sistema operativo de 64 bits, Common Language Runtime (CLR) puede ejecutarlo como un proceso de 32 bits o de 64 bits. De forma predeterminada, el CLR ejecuta las aplicaciones administradas como 64 bits y deben funcionar correctamente sin problemas. Sin embargo, si la aplicación depende de un archivo DLL nativo de 32 bits, se producirá un error en la aplicación al intentar llamar a este archivo DLL. Un proceso de 64 bits necesita código completamente de 64 bits y no se puede llamar a una DLL de 32 bits desde un proceso de 64 bits. La mejor solución a largo plazo consiste en compilar el código nativo como de 64 bits también, pero una solución perfectamente razonable consiste en marcar simplemente la aplicación administrada como solo para x86 mediante el uso de la marca de compilación/Platform: x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implicaciones de rendimiento de la ejecución de un sistema operativo de 64 bits

Dado que los procesadores con la arquitectura de Intel 64 y AMD64 pueden ejecutar instrucciones de 32 bits de forma nativa, pueden ejecutar aplicaciones de 32 bits a toda velocidad, incluso en un sistema operativo de 64 bits. La conversión de parámetros entre 32 y 64 bits supone un costo modesto al llamar a funciones del sistema operativo, pero este costo suele ser insignificante. Esto significa que no debería ver ninguna ralentización al ejecutar aplicaciones de 32 bits en un sistema operativo de 64 bits.

Al compilar aplicaciones como de 64 bits, los cálculos son más complicados. Un programa de 64 bits usa punteros de 64 bits y sus instrucciones son ligeramente más grandes, por lo que el requisito de memoria se incrementa ligeramente. Esto puede producir una ligera caída del rendimiento. Por otro lado, tener el doble de registros y tener la capacidad de realizar cálculos de enteros de 64 bits en una sola instrucción, a menudo es más que compensar. El resultado neto es que una aplicación de 64 bits puede ejecutarse ligeramente más lenta que la misma aplicación compilada como 32 bits, pero a menudo se ejecutará un poco más rápido.

## <a name="summary"></a>Resumen

Las arquitecturas de 64 bits permiten a los desarrolladores imponer las limitaciones de la apariencia, el sonido y la reproducción de juegos. Sin embargo, la transición de la programación de 32 bits a la programación de 64 bits no es trivial. Al comprender las diferencias entre los dos y el uso de las herramientas más recientes, la transición a las plataformas de 64 bits puede ser más fácil y rápida.

Puede encontrar más información sobre la programación de 64 bits en [Visual C++ centro para desarrolladores: programación de 64 bits](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 