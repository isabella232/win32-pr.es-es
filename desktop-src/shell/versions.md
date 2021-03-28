---
description: En esta sección se describe cómo determinar la versión de los archivos dll de Shell en la que se ejecuta la aplicación y cómo dirigirse a la aplicación para una versión específica.
title: 'Versiones de DLL de Shell y Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276736"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Versiones de DLL de Shell y Shlwapi 

En esta sección se describe cómo determinar la versión de los archivos dll de Shell en la que se ejecuta la aplicación y cómo dirigirse a la aplicación para una versión específica.

-   [Números de versión de DLL](#dll-version-numbers)
-   [Uso de DllGetVersion para determinar el número de versión](#using-dllgetversion-to-determine-the-version-number)
    -   [Usar DllGetVersion](#using-dllgetversion)
-   [Versiones del proyecto](#project-versions)

## <a name="dll-version-numbers"></a>Números de versión de DLL

Todos los elementos de programación, excepto algunos de los descritos en la documentación de Shell, se encuentran en dos archivos dll: Shell32.dll y Shlwapi.dll. Debido a las mejoras continuas, las diferentes versiones de estos archivos dll implementan características diferentes. En la documentación de referencia del shell, cada elemento de programación especifica un número de versión de DLL compatible mínimo. Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario. Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes de la DLL.

Antes de Windows XP, las nuevas versiones de Shell32.dll y Shlwapi.dll se proporcionaban a veces con nuevas versiones de Windows Internet Explorer. A partir de Windows XP, esos archivos DLL ya no se proporcionaron como archivos redistribuibles fuera de las nuevas versiones de Windows. En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron a Microsoft Internet Explorer 3,0, Windows 95 y Microsoft Windows NT 4,0.

Shell32.dll versión 4,0 se encuentra en las versiones originales de Windows 95 y Microsoft Windows NT 4,0. El shell no se actualizó con la versión 3,0 de Internet Explorer, por lo que Shell32.dll no tiene la versión 4,70. Shell32.dll versiones 4,71 y 4,72 se enviaron con las correspondientes versiones de Internet Explorer, pero no se instalaron necesariamente (vea la nota 1). En el caso de las versiones posteriores a Microsoft Internet Explorer 4,01 y Windows 98, los números de versión de Shell32.dll y Shlwapi.dll divergen. En general, debe suponer que los archivos dll tienen números de versión diferentes y probar cada uno por separado.

#### <a name="shell32dll"></a>Shell32.dll

| Versión | Plataforma de distribución                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 y Microsoft Windows NT 4,0                                     |
| 4.71    | Microsoft Internet Explorer 4,0. Vea la nota 1.                                |
| 4.72    | Internet Explorer 4,01 y Windows 98. Vea la nota 1.                          |
| 5.0     | Windows 2000 y Windows Millennium Edition (Windows me). Vea la nota 2.       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Versión | Plataforma de distribución                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 y Microsoft Windows NT 4,0                                     |
| 4.71    | Internet Explorer 4,0. Vea la nota 1.                                          |
| 4.72    | Internet Explorer 4,01 y Windows 98. Vea la nota 1.                          |
| 4,7     | Internet Explorer 3. x                                                       |
| 5.0     | Microsoft Internet Explorer 5 y Windows 98 SE. Vea la nota 2.                |
| 5.5     | Microsoft Internet Explorer 5,5 y Windows Millennium Edition (Windows me) |
| 6.0     | Windows XP y Windows Vista                                                |



**Nota 1:** Todos los sistemas con Internet Explorer 4,0 o 4,01 tenían la versión asociada de Shlwapi.dll (4,71 o 4,72, respectivamente). Sin embargo, para sistemas anteriores a Windows 98, se pueden instalar Internet Explorer 4,0 y 4,01 con o sin lo que se conocía como *Shell integrado*. Si Internet Explorer se instaló con el shell integrado, también se instalará la versión asociada de Shell32.dll (4,71 o 4,72). Si Internet Explorer se instaló sin el shell integrado, Shell32.dll permaneció como la versión 4,0. En otras palabras, la presencia de la versión 4,71 o 4,72 de Shlwapi.dll en un sistema no garantiza que Shell32.dll tenga el mismo número de versión. Todos los sistemas de Windows 98 tienen la versión 4,72 de Shell32.dll.

**Nota 2:** La versión 5,0 de Shlwapi.dll se distribuyó con Internet Explorer 5 y se encontró en todos los sistemas en los que se instaló Internet Explorer 5, con la excepción de Windows 2000. La versión 5,0 de Shell32.dll se distribuyó de forma nativa con Windows 2000 y Windows Millennium Edition (Windows me), junto con la versión 5,0 de Shlwapi.dll.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Uso de DllGetVersion para determinar el número de versión

A partir de la versión 4,71, los archivos dll de Shell, entre otros, empezaron a exportar [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Una aplicación puede llamar a esta función para determinar qué versión de DLL está presente en el sistema.

> [!Note]  
> Los archivos dll no exportan necesariamente [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Pruébelo siempre antes de intentar usarlo.

En las versiones de Windows anteriores a Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) devuelve una estructura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) que contiene los números de versión principal y secundaria, el número de compilación y un identificador de plataforma. En el caso de los sistemas Windows 2000 y versiones posteriores, es posible que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Además de la información proporcionada a través de **DLLVERSIONINFO**, **DLLVERSIONINFO2** también proporciona el número de revisión que identifica la Service Pack instalada más reciente, que proporciona una manera más eficaz de comparar los números de versión. Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO** , la estructura posterior es compatible con versiones anteriores.

### <a name="using-dllgetversion"></a>Usar DllGetVersion

La función de ejemplo siguiente `GetVersion` carga un archivo dll especificado e intenta llamar a su función [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) . Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) en un **valor DWORD** que se devuelve a la aplicación que realiza la llamada. Si el archivo DLL no exporta **DllGetVersion**, la función devuelve cero. Con Windows 2000 y sistemas posteriores, puede modificar la función para controlar la posibilidad de que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Si es así, use la información del miembro **ullVersion** de la estructura **DLLVERSIONINFO2** para comparar las versiones, los números de compilación y las versiones de Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion**.

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad. Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


En el ejemplo de código siguiente se muestra cómo puede usar `GetVersion` para comprobar si Shell32.dll es la versión 6,0 o posterior.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Versiones del proyecto

Para asegurarse de que la aplicación es compatible con las distintas versiones de destino de un archivo. dll, las macros de versión están presentes en los archivos de encabezado. Estas macros se utilizan para definir, excluir o volver a definir ciertas definiciones para diferentes versiones de la DLL. Vea [usar los encabezados de Windows](../winprog/using-the-windows-headers.md) para obtener una descripción detallada de estas macros.

Por ejemplo, el nombre de macro **\_ Win32 \_ IE** suele encontrarse en encabezados más antiguos. Usted es responsable de definir la macro como un número hexadecimal. Este número de versión define la versión de destino de la aplicación que está usando el archivo DLL. En la tabla siguiente se muestran los números de versión disponibles y el efecto que cada tiene en la aplicación.


| Versión | Descripción                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | La aplicación es compatible con Shell32.dll versión 4,00 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,00.                                              |
| 0x0300  | La aplicación es compatible con Shell32.dll versión 4,70 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,70.                                              |
| 0x0400  | La aplicación es compatible con Shell32.dll versión 4,71 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,71.                                              |
| 0x0401  | La aplicación es compatible con Shell32.dll versión 4,72 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,72.                                              |
| 0x0500  | La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 5,0 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5,0 de Shell32.dll y Shlwapi.dll. |
| 0x0501  | La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 5,0 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5,0 de Shell32.dll y Shlwapi.dll. |
| 0x0600  | La aplicación es compatible con Shell32.dll y Shlwapi.dll versión 6,0 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 6,0 de Shell32.dll y Shlwapi.dll. |


Si no define la macro de **\_ \_ IE de Win32** en el proyecto, se define automáticamente como 0x0500. Para definir un valor diferente, puede agregar lo siguiente a las directivas de compilador en el archivo make; Sustituya el número de versión deseado por 0x0400.

```
/D _WIN32_IE=0x0400
```

Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado del shell. Sustituya el número de versión deseado por 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
