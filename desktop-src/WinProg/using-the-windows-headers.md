---
title: Uso de los Windows encabezados
description: Use los Windows de encabezado para crear aplicaciones que usen la API Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows API, archivos de encabezado
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 886c5601683cc03fb2486f8be3b69f31c4619b721276babbc2c3e31e28c0a022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643595"
---
# <a name="using-the-windows-headers"></a>Uso de los Windows encabezados

Los archivos de encabezado de Windows API permiten crear aplicaciones de 32 y 64 bits. Incluyen declaraciones para las versiones Unicode y ANSI de la API. Para obtener más información, vea [Unicode en la API Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Usan tipos [de datos](windows-data-types.md) que permiten compilar versiones de 32 y 64 bits de la aplicación desde una sola base de código fuente. Para obtener más información, vea [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Entre las características adicionales [se incluyen anotaciones de encabezado y](header-annotations.md) comprobación de tipos [STRICT.](strict-type-checking.md)

-   [Visual C++ y los archivos Windows encabezado](#visual-c-and-the-windows-header-files)
-   [Macros para declaraciones condicionales](#macros-for-conditional-declarations)
-   [Configuración de WINVER \_ o WIN32 \_ WINNT](#setting-winver-or-_win32_winnt)
-   [Controlar el empaquetado de la estructura](#controlling-structure-packing)
-   [Compilaciones más rápidas con archivos de encabezado más pequeños](#faster-builds-with-smaller-header-files)
-   [Temas relacionados](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ y los archivos Windows encabezado

Microsoft Visual C++ incluye copias de los Windows de encabezado que estaban actuales en el momento en que Visual C++ se publicó. Por lo tanto, si instala archivos de encabezado actualizados desde un SDK, puede acabar con varias versiones de los archivos de encabezado Windows en el equipo. Si no se asegura de que usa la versión más reciente de los archivos de encabezado del SDK, recibirá el siguiente código de error al compilar código que usa características que se introdujeron después de que se publicara Visual C++: error C2065: identificador no declarado.

## <a name="macros-for-conditional-declarations"></a>Macros para declaraciones condicionales

Determinadas funciones que dependen de una versión determinada de Windows se declaran mediante código condicional. Esto le permite usar el compilador para detectar si la aplicación usa funciones que no se admiten en sus versiones de destino de Windows. Para compilar una aplicación que use estas funciones, debe definir las macros adecuadas. De lo contrario, recibirá el mensaje de error C2065.

Los Windows de encabezado usan macros para indicar qué versiones de Windows admiten muchos elementos de programación. Por lo tanto, debe definir estas macros para usar la nueva funcionalidad introducida en cada versión principal del sistema operativo. (Los archivos de encabezado individuales pueden usar macros diferentes; por lo tanto, si se producen problemas de compilación, compruebe el archivo de encabezado que contiene la definición de definiciones condicionales). Para más información, consulte SdkDdkVer.h.

En la tabla siguiente se describen las macros preferidas que se usan en Windows archivos de encabezado. Si define NTDDI \_ VERSION, también debe definir \_ \_ WINNT win32.



| Sistema mínimo requerido                       | Valor de NTDDI \_ VERSION            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "Umbral 2"                 | **NTDDI \_ WIN10 \_ TH2** (0x0A000001)  |
| Windows 10 "Umbral" 1507                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista con Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 con Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 con Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP con Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP con Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP con Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

En las tablas siguientes se describen otras macros que se usan en Windows archivos de encabezado.



| Sistema mínimo requerido                           | Valor mínimo para \_ \_ WINNT y WINVER de WIN32 |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ WIN32 \_ WINNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ WINNT \_ \_ WINBLUE WIN32** (0x0603)        |
| Windows 8                                         | **\_ WIN32 \_ WINNT \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ WIN32 \_ WINNT \_ WIN7** (0x0601)           |
| Windows Server 2008                               | **\_ WIN32 \_ WINNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ WIN32 \_ WINNT \_ VISTA** (0x0600)          |
| Windows Server 2003 con SP1, Windows XP con SP2 | **\_ WIN32 \_ WINNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ WINNT \_ \_ WINXP win32** (0x0501)          |



 



| Versión mínima necesaria          | Valor mínimo de \_ WIN32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11.0            | **\_ WIN32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10.0            | **\_ WIN32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ WIN32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ WIN32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ WIN32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6.0 SP2         | **\_ WIN32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6.0 SP1         | **\_ WIN32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ WIN32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5,5             | **\_ WIN32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5.01            | **\_ WIN32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5.0, 5.0a, 5.0b | **\_ WIN32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Configuración de WINVER \_ o WIN32 \_ WINNT

Puede definir estos símbolos mediante la instrucción define en cada archivo de origen o especificando la opción del compilador \# /D admitida por Visual C++.

Por ejemplo, para establecer WINVER en el archivo de código fuente, use la siguiente instrucción:

`#define WINVER 0x0502`

Para establecer \_ \_ WINNT win32 en el archivo de código fuente, use la siguiente instrucción:

`#define _WIN32_WINNT 0x0502`

Para establecer \_ WINNT win32 mediante la opción del compilador \_ /D, use el siguiente comando:

**cl -c /D \_ WIN32 \_ WINNT=0x0502** _origen_**.cpp**

Para obtener información sobre el uso de la opción del compilador /D, vea [/D (definiciones de preprocesador).](/cpp/build/reference/d-preprocessor-definitions)

Tenga en cuenta que algunas características introducidas en la versión más reciente de Windows se pueden agregar a un Service Pack para una versión anterior de Windows. Por lo tanto, para tener como destino un Service Pack, es posible que deba definir WINNT win32 con el valor de la próxima versión \_ \_ principal del sistema operativo. Por ejemplo, la función [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) se introdujo en Windows Server 2003 y se define condicionalmente si \_ \_ WINNT win32 0x0502 o superior. Esta función también se agregó a Windows XP con SP1. Por lo tanto, si fuera a definir WINNT win32 como 0x0501 para tener como destino Windows XP, se perderían las características definidas en \_ \_ Windows XP con SP1.

## <a name="controlling-structure-packing"></a>Controlar el empaquetado de la estructura

Los proyectos deben compilarse para usar el empaquetado de estructura predeterminado, que actualmente es de 8 bytes porque el tipo entero más grande es de 8 bytes. Esto garantiza que todos los tipos de estructura dentro de los archivos de encabezado se compilan en la aplicación con la misma alineación que Windows API espera. También garantiza que las estructuras con valores de 8 bytes estén correctamente alineadas y no causen errores de alineación en los procesadores que aplican la alineación de datos.

Para obtener más información, vea [/Zp (alineación de miembros de estructura)](/cpp/build/reference/zp-struct-member-alignment) o [empaquetar](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Compilaciones más rápidas con archivos de encabezado más pequeños

Puede reducir el tamaño de los archivos de encabezado Windows excluyendo algunas de las declaraciones de API menos comunes como se muestra a continuación:

-   Defina WIN32 LEAN AND MEAN para excluir API como \_ \_ \_ Cryptography, DDE, RPC, Shell y Windows Sockets.

    `#define WIN32_LEAN_AND_MEAN`

-   Defina uno o varios de los símbolos de *API* NO para excluir la API. Por ejemplo, NOCOMM excluye la API de comunicación serie. Para obtener una lista de los símbolos DE *API* no compatibles, consulte Windows.h.

    `#define NOCOMM`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sitio de descarga del SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 