---
title: Usar los encabezados de Windows
description: Use los archivos de encabezado de Windows para crear aplicaciones que usen la API de Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- API de Windows, archivos de encabezado
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 4d27b14a6e545db9a9a38c205012b149942adf7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421215"
---
# <a name="using-the-windows-headers"></a>Usar los encabezados de Windows

Los archivos de encabezado de la API de Windows permiten crear aplicaciones de 32 y 64 bits. Incluyen declaraciones para las versiones Unicode y ANSI de la API. Para obtener más información, consulte [Unicode en la API de Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Usan [tipos de datos](windows-data-types.md) que le permiten compilar versiones de 32 y 64 bits de la aplicación a partir de una base de código fuente única. Para obtener más información, consulte [preparación para Windows de 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Entre las características adicionales se incluyen [anotaciones de encabezado](header-annotations.md) y [comprobación estricta de tipos](strict-type-checking.md).

-   [Visual C++ y los archivos de encabezado de Windows](#visual-c-and-the-windows-header-files)
-   [Macros para declaraciones condicionales](#macros-for-conditional-declarations)
-   [Configuración de WINVER o \_ Win32 \_ Winnt](#setting-winver-or-_win32_winnt)
-   [Controlar el empaquetado de estructuras](#controlling-structure-packing)
-   [Compilaciones más rápidas con archivos de encabezado más pequeños](#faster-builds-with-smaller-header-files)
-   [Temas relacionados](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ y los archivos de encabezado de Windows

Microsoft Visual C++ incluye copias de los archivos de encabezado de Windows que estaban actualizados en el momento en que se liberó Visual C++. Por lo tanto, si instala los archivos de encabezado actualizados desde un SDK, es posible que acabe con varias versiones de los archivos de encabezado de Windows del equipo. Si no está seguro de que está utilizando la versión más reciente de los archivos de encabezado del SDK, recibirá el siguiente código de error al compilar el código que usa las características que se introdujeron después de que se liberara Visual C++: error C2065: identificador no declarado.

## <a name="macros-for-conditional-declarations"></a>Macros para declaraciones condicionales

Ciertas funciones que dependen de una versión determinada de Windows se declaran mediante código condicional. Esto le permite usar el compilador para detectar si la aplicación usa funciones que no se admiten en sus versiones de destino de Windows. Para compilar una aplicación que usa estas funciones, debe definir las macros adecuadas. De lo contrario, recibirá el mensaje de error C2065.

Los archivos de encabezado de Windows usan macros para indicar qué versiones de Windows admiten muchos elementos de programación. Por lo tanto, debe definir estas macros para que usen la nueva funcionalidad introducida en cada versión principal del sistema operativo. (Los archivos de encabezado individuales pueden usar macros diferentes; por lo tanto, si se producen problemas de compilación, compruebe el archivo de encabezado que contiene la definición de las definiciones condicionales). Para obtener más información, vea SdkDdkVer. h.

En la tabla siguiente se describen las macros preferidas que se usan en los archivos de encabezado de Windows. Si define la \_ versión de NTDDI, también debe definir \_ Win32 \_ Winnt.



| Mínimo de sistema requerido                       | Valor de la \_ versión de NTDDI            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "umbral 2"                 | **NTDDI \_ WIN10 \_ Th2** (0x0A000001)  |
| Windows 10 1507 "umbral"                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista con Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 con Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 con Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP con Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP con Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP con Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

En las tablas siguientes se describen otras macros que se usan en los archivos de encabezado de Windows.



| Mínimo de sistema requerido                           | Valor mínimo para \_ Win32 \_ WinNT y winver |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ Win32 \_ WinNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ Win32 \_ WinNT \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ Win32 \_ WinNT \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ Win32 \_ WinNT \_ win7** (0x0601)           |
| Windows Server 2008                               | **\_ Win32 \_ WinNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ Win32 \_ WinNT \_ vista** (0x0600)          |
| Windows Server 2003 con SP1, Windows XP con SP2 | **\_ Win32 \_ WinNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ Win32 \_ WinNT \_ WinXP** (0x0501)          |



 



| Versión mínima necesaria          | Valor mínimo de \_ Win32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11,0            | **\_ Win32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10,0            | **\_ Win32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ Win32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ Win32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ Win32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6,0 SP2         | **\_ Win32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6,0 SP1         | **\_ Win32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ Win32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5,5             | **\_ Win32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5,01            | **\_ Win32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5,0, 5.0 a, 5.0 b | **\_ Win32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Configuración de WINVER o \_ Win32 \_ Winnt

Puede definir estos símbolos mediante la \# instrucción define en cada archivo de código fuente o especificando la opción de compilador/d compatible con Visual C++.

Por ejemplo, para establecer WINVER en el archivo de código fuente, use la siguiente instrucción:

`#define WINVER 0x0502`

Para establecer \_ Win32 \_ WinNT en el archivo de código fuente, utilice la siguiente instrucción:

`#define _WIN32_WINNT 0x0502`

Para establecer \_ Win32 \_ WinNT mediante la opción del compilador/d, use el siguiente comando:

**cl-c/d \_ WIN32 \_ WinNT = 0x0502** _source_**. cpp**

Para obtener información sobre el uso de la opción de compilador/D, vea [/d (definiciones de preprocesador)](/cpp/build/reference/d-preprocessor-definitions).

Tenga en cuenta que algunas características introducidas en la versión más reciente de Windows se pueden agregar a un Service Pack de una versión anterior de Windows. Por lo tanto, para tener como destino un Service Pack, puede que tenga que definir \_ Win32 \_ WinNT con el valor de la siguiente versión principal del sistema operativo. Por ejemplo, la función [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) se presentó en Windows Server 2003 y se define condicionalmente si \_ Win32 \_ WinNT es 0x0502 o superior. Esta función también se ha agregado a Windows XP con SP1. Por lo tanto, si fuera a definir \_ Win32 \_ WinNT como 0x0501 para tener como destino Windows XP, omitiría las características definidas en Windows XP con SP1.

## <a name="controlling-structure-packing"></a>Controlar el empaquetado de estructuras

Los proyectos se deben compilar para utilizar la estructura predeterminada Packing, que es actualmente de 8 bytes porque el tipo entero más grande es de 8 bytes. Esto garantiza que todos los tipos de estructura de los archivos de encabezado se compilan en la aplicación con la misma alineación que espera la API de Windows. También garantiza que las estructuras con valores de 8 bytes se alineen correctamente y no producirán errores de alineación en los procesadores que imponen la alineación de los datos.

Para obtener más información, consulte [/ZP (alineación de miembros de estructura)](/cpp/build/reference/zp-struct-member-alignment) o [Pack](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Compilaciones más rápidas con archivos de encabezado más pequeños

Puede reducir el tamaño de los archivos de encabezado de Windows excluyendo algunas de las declaraciones de API menos comunes de la siguiente manera:

-   Defina WIN32 \_ lean \_ y \_ medias para excluir API como Cryptography, DDE, RPC, Shell y Windows Sockets.

    `#define WIN32_LEAN_AND_MEAN`

-   Defina uno o varios de los símbolos de *API* no para excluir la API. Por ejemplo, nocomm excluye la API de comunicación en serie. Para obtener una lista de NO admitir símbolos de *API* , consulte Windows. h.

    `#define NOCOMM`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows SDK sitio de descarga](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 