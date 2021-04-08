---
description: Las funciones auxiliares de la API de la versión se usan para determinar la versión del sistema operativo que se está ejecutando actualmente. Para obtener más información, vea obtener la versión del sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versión de sistema operativo
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "104078551"
---
# <a name="operating-system-version"></a>Versión de sistema operativo

Las [funciones auxiliares](version-helper-apis.md) de la API de la versión se usan para determinar la versión del sistema operativo que se está ejecutando actualmente. Para obtener más información, vea [obtener la versión del sistema](getting-the-system-version.md).

En la tabla siguiente se resumen los números de versión más recientes del sistema operativo.

| Sistema operativo | Número de versión |
|------------------|----------------|
| Windows 10       | 10,0\*         |
| Windows Server 2019 | 10,0\*      |
| Windows Server 2016 | 10,0\*      |
| Windows 8.1      | 6,3\*          |
| Windows Server 2012 R2 | 6,3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Windows XP 64-bit Edition | 5.2   |
| Windows XP | 5,1                  |
| Windows 2000     | 5.0            |

**\*** Para las aplicaciones que se han manifestado para Windows 8.1 o Windows 10. Las aplicaciones no manifestadas para Windows 8.1 o Windows 10 devolverán el valor de la versión del sistema operativo Windows 8 (6,2). Para manifestar las aplicaciones para Windows 8.1 o Windows 10, consulte establecer como [destino la aplicación para Windows](targeting-your-application-at-windows-8-1.md).<br/>

La identificación del sistema operativo actual no suele ser la mejor manera de determinar si una determinada característica del sistema operativo está presente. Esto se debe a que es posible que el sistema operativo tenga nuevas características agregadas en un archivo DLL redistribuible. En lugar de usar las [funciones auxiliares](version-helper-apis.md) de la API de la versión para determinar la plataforma del sistema operativo o el número de versión, Compruebe la presencia de la propia característica.

Para determinar la mejor manera de probar una característica, consulte la documentación de la característica de interés. En la lista siguiente se describen algunas técnicas comunes para la detección de características:

- Puede comprobar la presencia de las funciones asociadas a una característica. Para comprobar la presencia de una función en un archivo DLL del sistema, llame a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar el archivo dll. A continuación, llame a la función [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para determinar si la función de interés está presente en el archivo dll. Use el puntero devuelto por **GetProcAddress** para llamar a la función. Tenga en cuenta que, aunque la función esté presente, puede ser un código auxiliar que simplemente devuelva un código de error, como la llamada de ERROR \_ \_ no \_ implementada.
- Puede determinar la presencia de algunas características mediante la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Por ejemplo, puede detectar varios monitores de pantalla mediante una llamada a **GetSystemMetrics**(SM \_ CMONITORS).
- Hay varias versiones de los archivos dll redistribuibles que implementan características de Shell y de control común. Para obtener información sobre cómo determinar qué versiones están presentes en el sistema en el que se ejecuta la aplicación, vea el tema [Shell y versiones de controles comunes](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Si necesita un sistema operativo determinado, asegúrese de usarlo como una versión mínima compatible, en lugar de diseñar la prueba para un sistema operativo. De esta manera, el código de detección seguirá funcionando en versiones futuras de Windows.

Tenga en cuenta que una aplicación de 32 bits puede detectar si se ejecuta bajo WOW64 mediante una llamada a la función [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) . Puede obtener información adicional sobre el procesador llamando a la función [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Para obtener más información, vea información de la [versión de Windows 10](/windows/release-information/) y hoja de datos de [ciclo de vida de Windows](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

