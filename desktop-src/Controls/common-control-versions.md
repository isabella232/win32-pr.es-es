---
title: Versiones de control comunes
description: En este tema se enumeran las versiones disponibles de la biblioteca de control común (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo dirigir la aplicación para una versión específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f1a70be183ff0bd3b1f88af548605fece254cfb172f27b247a12a7557c11a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921135"
---
# <a name="common-control-versions"></a>Versiones de control comunes

En este tema se enumeran las versiones disponibles de la biblioteca de control común (ComCtl32.dll), se describe cómo identificar la versión que usa la aplicación y se explica cómo dirigir la aplicación para una versión específica.

En este tema se incluyen las siguientes secciones.

-   [Números comunes de versiones de DLL de control](#common-control-dll-versions-numbers)
-   [Tamaños de estructura para diferentes versiones de control comunes](#structure-sizes-for-different-common-control-versions)
-   [Usar DllGetVersion para determinar el número de versión](#using-dllgetversion-to-determine-the-version-number)
-   [Project Versiones](#project-versions)
-   [Temas relacionados](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Números comunes de versiones de DLL de control

La compatibilidad con los controles comunes se proporciona ComCtl32.dll, que incluyen todas las versiones de 32 y 64 bits Windows. Cada versión sucesiva del archivo DLL admite las características y la API de versiones anteriores y agrega nuevas características.

Dado que varias versiones de ComCtl32.dll se distribuyeron con Internet Explorer, la versión activa a veces es diferente de la versión que se distribuyó con el sistema operativo. Por lo tanto, la aplicación debe determinar directamente qué versión de ComCtl32.dll está presente.

En la documentación de referencia de controles comunes, muchos elementos de programación especifican un número mínimo de versión de DLL compatible. Este número de versión indica que el elemento de programación se implementa en esa versión y versiones posteriores del archivo DLL, a menos que se especifique lo contrario. Si no se especifica ningún número de versión, el elemento de programación se implementa en todas las versiones existentes del archivo DLL.

En la tabla siguiente se describen las distintas versiones de DLL y cómo se distribuyeron en sistemas operativos compatibles.



ComCtl32.dll

Versión

Plataforma de distribución

5.81

Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5 y Microsoft Internet Explorer 6

5.82

Windows Server 2003, Windows Vista, Windows Server 2008 y Windows 7

6,0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 y Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Tamaños de estructura para diferentes versiones de control comunes

Las mejoras continuas en los controles comunes han dado lugar a la necesidad de ampliar muchas de las estructuras. Por esta razón, el tamaño de las estructuras ha cambiado entre diferentes versiones de Commctrl.h. Dado que la mayoría de las estructuras de control comunes toman un tamaño de estructura como uno de los parámetros, se puede producir un error en un mensaje o una función si no se reconoce el tamaño. Para solucionar este problema, se han definido constantes de tamaño de estructura para ayudar a dirigirse a diferentes versiones de ComCtl32.dll. En la lista siguiente se definen las constantes de tamaño de estructura.



|    Constante de tamaño de estructura                           |     Definición                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| TAMAÑO DE HDITEM \_ V1 \_              | Tamaño de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) en la versión 4.0.                           |
| TAMAÑO DE IMAGELISTDRAWPARAMS \_ V3 \_ | Tamaño de la estructura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) en la versión 5.9. |
| LVCOLUMN \_ V1 \_ SIZE            | Tamaño de la [**estructura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) en la versión 4.0.                       |
| LVGROUP \_ V5 \_ SIZE             | Tamaño de la [**estructura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) en la versión 6.0.                         |
| LVHITTESTINFO \_ V1 \_ SIZE       | Tamaño de la [**estructura LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) en la versión 4.0.             |
| LVITEM \_ V1 \_ SIZE              | Tamaño de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 4.0.                           |
| LVITEM \_ V5 \_ SIZE              | Tamaño de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) en la versión 6.0.                           |
| LVTILEINFO \_ V5 \_ SIZE          | Tamaño de la [**estructura LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) en la versión 6.0.                   |
| TAMAÑO DE MCHITTESTINFO \_ V1 \_       | Tamaño de la [**estructura MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) en la versión 4.0.             |
| TAMAÑO NMLVCUSTOMDRAW \_ V3 \_      | Tamaño de la estructura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) en la versión 4.7.           |
| TAMAÑO NMTTDISPINFO \_ V1 \_        | Tamaño de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en la versión 4.0.               |
| TAMAÑO NMTVCUSTOMDRAW \_ V3 \_      | Tamaño de la [**estructura NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) en la versión 4.7.           |
| TAMAÑO PROPSHEETHEADER \_ V1 \_     | Tamaño de la estructura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) en la versión 4.0.         |
| TAMAÑO DE PROPSHEETPAGE \_ V1 \_       | Tamaño de la estructura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) en la versión 4.0.             |
| TAMAÑO DE REBARBANDINFO \_ V3 \_       | Tamaño de la [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 4.7.             |
| TAMAÑO DE REBARBANDINFO \_ V6 \_       | Tamaño de la [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) en la versión 6.0.             |
| TTTOOLINFO \_ V1 \_ SIZE          | Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4.0.                       |
| TTTOOLINFO \_ V2 \_ SIZE          | Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 4.7.                       |
| TTTOOLINFO \_ V3 \_ SIZE          | Tamaño de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) en la versión 6.0.                       |
| TVINSERTSTRUCT \_ V1 \_ SIZE      | Tamaño de la [**estructura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) en la versión 4.0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Usar DllGetVersion para determinar el número de versión

Una aplicación puede llamar a la función [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) para determinar qué versión de DLL está presente en el sistema.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) devuelve una [**estructura DLLVERSIONINFO2.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) Además de la información proporcionada a través de [**DLLVERSIONINFO,**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) **DLLVERSIONINFO2** también proporciona el número de revisión que identifica el Service Pack instalado más reciente, que proporciona una manera más sólida de comparar los números de versión. Dado que el primer miembro de **DLLVERSIONINFO2** es una estructura **DLLVERSIONINFO,** la estructura posterior es compatible con versiones anteriores.


La siguiente función de `GetVersion` ejemplo carga un archivo DLL especificado e intenta llamar a su función [**DllGetVersion.**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) Si se realiza correctamente, usa una macro para empaquetar los números de versión principal y secundaria de la estructura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) en un **DWORD** que se devuelve a la aplicación que realiza la llamada. Si el archivo DLL no exporta **DllGetVersion**, la función devuelve cero. Puede modificar la función para controlar la posibilidad de que **DllGetVersion** devuelva una [**estructura DLLVERSIONINFO2.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) Si es así, use la información del miembro **ullVersion** de esa estructura **DLLVERSIONINFO2** para comparar versiones, números de compilación y versiones de Service Pack. La [**macro MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica la tarea de comparar estos valores con los de **ullVersion.**

> [!Note]  
> El [**uso incorrecto de LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede suponer riesgos de seguridad. Consulte la documentación **de LoadLibrary** para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Windows.

 


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



En el ejemplo de código siguiente se muestra cómo puede usar para probar si `GetVersion` ComCtl32.dll versión 6.0 o posterior.


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



## <a name="project-versions"></a>Project Versiones

Para asegurarse de que la aplicación es compatible con diferentes versiones de destino de un archivo .dll, las macros de versión están presentes en los archivos de encabezado. Estas macros se usan para definir, excluir o volver a definir determinadas definiciones para distintas versiones del archivo DLL. Consulte [Uso de los Windows encabezados para](/windows/desktop/WinProg/using-the-windows-headers) obtener una descripción detallada de estas macros.

Por ejemplo, el nombre de macro **\_ WIN32 \_ IE** se encuentra normalmente en encabezados anteriores. Usted es responsable de definir la macro como un número hexadecimal. Este número de versión define la versión de destino de la aplicación que usa el archivo DLL. En la tabla siguiente se muestran los números de versión disponibles y el efecto que cada uno tiene en la aplicación.



| Versión | Descripción                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | La aplicación es compatible con ComCtl32.dll versión 4.70 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4.70. |
| 0x0400  | La aplicación es compatible con ComCtl32.dll versión 4.71 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4.71. |
| 0x0401  | La aplicación es compatible con ComCtl32.dll versión 4.72 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 4.72. |
| 0x0500  | La aplicación es compatible con ComCtl32.dll versión 5.80 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5.80. |
| 0x0501  | La aplicación es compatible con ComCtl32.dll versión 5.81 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 5.81. |
| 0x0600  | La aplicación es compatible con ComCtl32.dll versión 6.0 y posteriores. La aplicación no puede implementar características que se agregaron después de la versión 6.0.   |



 

Si no define la macro **\_ WIN32 \_ IE** en el proyecto, se define automáticamente como 0x0500. Para definir un valor diferente, puede agregar lo siguiente a las directivas del compilador en el archivo make. sustituya el número de versión deseado para 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Otro método consiste en agregar una línea similar a la siguiente en el código fuente antes de incluir los archivos de encabezado de Shell. Sustituya el número de versión deseado por 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 