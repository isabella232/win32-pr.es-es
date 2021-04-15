---
title: Versiones de controles comunes
description: En este tema se enumeran las versiones disponibles de la biblioteca de controles comunes (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo establecer como destino la aplicación para una versión específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488591"
---
# <a name="common-control-versions"></a>Versiones de controles comunes

En este tema se enumeran las versiones disponibles de la biblioteca de controles comunes (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo establecer como destino la aplicación para una versión específica.

En este tema se incluyen las siguientes secciones.

-   [Números de versión de DLL de control común](#common-control-dll-versions-numbers)
-   [Tamaños de estructura para diferentes versiones de control comunes](#structure-sizes-for-different-common-control-versions)
-   [Uso de DllGetVersion para determinar el número de versión](#using-dllgetversion-to-determine-the-version-number)
-   [Versiones del proyecto](#project-versions)
-   [Temas relacionados](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Números de versión de DLL de control común

ComCtl32.dll proporciona compatibilidad con los controles comunes, que incluyen todas las versiones de 32 y 64 bits de Windows. Cada versión sucesiva del archivo DLL es compatible con las características y API de las versiones anteriores y agrega nuevas características.

Dado que varias versiones de ComCtl32.dll se distribuyeron con Internet Explorer, la versión que está activa a veces es diferente de la versión que se distribuyó con el sistema operativo. Por lo tanto, la aplicación debe determinar directamente qué versión de ComCtl32.dll está presente.

En la documentación de referencia de controles comunes, muchos elementos de programación especifican un número de versión de DLL compatible mínima. Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario. Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes de la DLL.

En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron en los sistemas operativos compatibles.



ComCtl32.dll

Versión

Plataforma de distribución

5,81

Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 y Microsoft Internet Explorer 6

5,82

Windows Server 2003, Windows Vista, Windows Server 2008 y Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 y Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Tamaños de estructura para diferentes versiones de control comunes

Las mejoras continuas en los controles comunes han dado lugar a la necesidad de extender muchas de las estructuras. Por esta razón, el tamaño de las estructuras ha cambiado entre las distintas versiones de commctrl. h. Dado que la mayoría de las estructuras de control comunes toman un tamaño de estructura como uno de los parámetros, se puede producir un error en un mensaje o una función si no se reconoce el tamaño. Para solucionar este comportamiento, las constantes de tamaño de la estructura se han definido como ayuda para tener como destino una versión diferente de ComCtl32.dll. En la lista siguiente se definen las constantes de tamaño de la estructura.



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| Tamaño de HDITEM \_ v1 \_              | Tamaño de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) en la versión 4,0.                           |
| Tamaño de IMAGELISTDRAWPARAMS \_ V3 \_ | Tamaño de la estructura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) en la versión 5,9. |
| Tamaño de LVCOLUMN \_ v1 \_            | Tamaño de la estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) en la versión 4,0.                       |
| Tamaño de LVGROUP \_ V5 \_             | Tamaño de la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) en la versión 6,0.                         |
| Tamaño de LVHITTESTINFO \_ v1 \_       | Tamaño de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) en la versión 4,0.             |
| Tamaño de LVITEM \_ v1 \_              | Tamaño de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 4,0.                           |
| Tamaño de LVITEM \_ V5 \_              | Tamaño de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 6,0.                           |
| Tamaño de LVTILEINFO \_ V5 \_          | Tamaño de la estructura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) en la versión 6,0.                   |
| Tamaño de MCHITTESTINFO \_ v1 \_       | Tamaño de la estructura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) en la versión 4,0.             |
| Tamaño de NMLVCUSTOMDRAW \_ V3 \_      | Tamaño de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) en la versión 4,7.           |
| Tamaño de NMTTDISPINFO \_ v1 \_        | Tamaño de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en la versión 4,0.               |
| Tamaño de NMTVCUSTOMDRAW \_ V3 \_      | Tamaño de la estructura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) en la versión 4,7.           |
| Tamaño de PROPSHEETHEADER \_ v1 \_     | Tamaño de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) en la versión 4,0.         |
| Tamaño de PROPSHEETPAGE \_ v1 \_       | Tamaño de la estructura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) en la versión 4,0.             |
| Tamaño de REBARBANDINFO \_ V3 \_       | Tamaño de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 4,7.             |
| Tamaño de REBARBANDINFO \_ V6 \_       | Tamaño de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 6,0.             |
| Tamaño de TTTOOLINFO \_ v1 \_          | Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4,0.                       |
| Tamaño de TTTOOLINFO \_ V2 \_          | Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4,7.                       |
| Tamaño de TTTOOLINFO \_ V3 \_          | Tamaño de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 6,0.                       |
| Tamaño de TVINSERTSTRUCT \_ v1 \_      | Tamaño de la estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) en la versión 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Uso de DllGetVersion para determinar el número de versión

Una aplicación puede llamar a la función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para determinar qué versión de dll está presente en el sistema.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) devuelve una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Además de la información proporcionada a través de [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** también proporciona el número de revisión que identifica la Service Pack instalada más reciente, que proporciona una manera más eficaz de comparar los números de versión. Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO** , la estructura posterior es compatible con versiones anteriores.


La función de ejemplo siguiente `GetVersion` carga un archivo dll especificado e intenta llamar a su función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) . Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) en un **valor DWORD** que se devuelve a la aplicación que realiza la llamada. Si el archivo DLL no exporta **DllGetVersion**, la función devuelve cero. Puede modificar la función para controlar la posibilidad de que **DllGetVersion** devuelva una estructura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Si es así, use la información del miembro **ullVersion** de la estructura **DLLVERSIONINFO2** para comparar las versiones, los números de compilación y las versiones de Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion**.

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos para la seguridad. Consulte la documentación de **LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



En el ejemplo de código siguiente se muestra cómo puede usar `GetVersion` para comprobar si ComCtl32.dll es la versión 6,0 o posterior.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Versiones del proyecto

Para asegurarse de que la aplicación es compatible con las distintas versiones de destino de un archivo. dll, las macros de versión están presentes en los archivos de encabezado. Estas macros se utilizan para definir, excluir o volver a definir ciertas definiciones para diferentes versiones de la DLL. Vea [usar los encabezados de Windows](/windows/desktop/WinProg/using-the-windows-headers) para obtener una descripción detallada de estas macros.

Por ejemplo, el nombre de macro **\_ Win32 \_ IE** suele encontrarse en encabezados más antiguos. Usted es responsable de definir la macro como un número hexadecimal. Este número de versión define la versión de destino de la aplicación que está usando el archivo DLL. En la tabla siguiente se muestran los números de versión disponibles y el efecto que cada tiene en la aplicación.



| Versión | Descripción                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | La aplicación es compatible con ComCtl32.dll versión 4,70 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,70. |
| 0x0400  | La aplicación es compatible con ComCtl32.dll versión 4,71 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,71. |
| 0x0401  | La aplicación es compatible con ComCtl32.dll versión 4,72 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4,72. |
| 0x0500  | La aplicación es compatible con ComCtl32.dll versión 5,80 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5,80. |
| 0x0501  | La aplicación es compatible con ComCtl32.dll versión 5,81 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5,81. |
| 0x0600  | La aplicación es compatible con ComCtl32.dll versión 6,0 y versiones posteriores. La aplicación no puede implementar características que se agregaron después de la versión 6,0.   |



 

Si no define la macro de **\_ \_ IE de Win32** en el proyecto, se define automáticamente como 0x0500. Para definir un valor diferente, puede agregar lo siguiente a las directivas de compilador en el archivo make; Sustituya el número de versión deseado por 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado del shell. Sustituya el número de versión deseado por 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 