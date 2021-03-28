---
description: El explorador de Windows es una eficaz aplicación de exploración y administración de recursos.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Desarrollo con el explorador de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497044"
---
# <a name="developing-with-windows-explorer"></a>Desarrollo con el explorador de Windows

El explorador de Windows es una eficaz aplicación de exploración y administración de recursos. Se puede tener acceso al explorador de Windows como un todo integrado a través de Explorer.exe o la interfaz [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . El explorador de Windows (Explorer.exe) se puede generar como un proceso independiente mediante [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una función similar.

> [!Note]  
> Las opciones de línea de comandos para Explorer.exe se documentan en el sitio de soporte técnico de Microsoft Windows en el artículo [Explorador de windows Command-Line opciones](https://support.microsoft.com/kb/152457).

 

Las ventanas de explorador abiertas se pueden detectar y programar mediante [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) y se pueden crear nuevas instancias del explorador de Windows mediante [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

En el ejemplo de código siguiente se muestra cómo se puede usar el modelo de automatización del explorador de Windows para crear y detectar ventanas del explorador que se están ejecutando.


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



El área cliente del explorador de Windows se puede hospedar mediante la interfaz [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . El cliente del explorador de Windows y los controles de árbol de espacios de nombres son componentes estándar de Windows Vista y versiones posteriores. Los desarrolladores pueden reutilizar las interfaces como componentes de compilación. Un uso común de estos controles es crear exploradores personalizados adecuados para el dominio del problema.

Los controles del explorador de Windows se clasifican en las siguientes categorías funcionales:

-   [Controles de navegación](#navigation-controls)
-   [Controles de comando](#command-controls)
-   [Propiedades y controles de vista previa](#property-and-preview-controls)
-   [Filtrar y ver controles](#filtering-and-view-controls)
-   [ListView (control)](#listview-control)

## <a name="navigation-controls"></a>Controles de navegación

Los controles de navegación ayudan a los usuarios a determinar el contexto y navegar por el espacio de dominio lógico asociado, denominado pagespace. Por ejemplo, pagespace para el explorador de Windows es el espacio de nombres del shell. Pagespaces se componen de cero o más páginas.

En la tabla siguiente se enumeran y describen los controles de navegación disponibles en el explorador de Windows en Windows Vista y sistemas operativos posteriores.



| Control de navegación               | Descripción                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de direcciones (control de ruta de navegación) | Muestra la dirección de la página actual en pagespace. Se puede hacer clic en los botones de navegación para desplazarse a cualquier antecesor en el pagespace. Los usuarios también pueden escribir direcciones URL y rutas de acceso para navegar. |
| Árbol de carpetas                      | Proporciona una nueva versión de un control de árbol, optimizada para pagespacess grandes.                                                                                                                  |
| Viajes                           | Habilita la navegación relativa a través de botones de estilo Web como **atrás** y **adelante**.                                                                                                    |
| Title                            | Muestra el nombre y el contexto del explorador actual.                                                                                                                                            |
| Pagespace                        | Muestra la rama actual de pagespace. Las páginas se pueden ordenar por criterios diferentes. Los usuarios pueden hacer clic en una página para ir a ella.                                                        |



 

## <a name="command-controls"></a>Controles de comando

Los controles de comandos anuncian las características y la funcionalidad del explorador de Windows a los usuarios. Estos controles realizan acciones generales o acciones específicas de un elemento o elementos seleccionados.



| Control de comandos | Descripción                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de herramientas         | Muestra botones para los comandos de uso frecuente (una nueva versión de una barra de herramientas de comandos). Entre las opciones de personalización se incluyen botones desplegables, botones de expansión, texto descriptivo opcional y un área de desbordamiento. |
| Imagen prominente            | Aparece como un único control personalizado y opcional en el centro de la barra de herramientas. Representa el comando principal del contexto actual.                                                             |
| Barra de menús        | Presenta comandos a través de menús.                                                                                                                                                                   |
| Menú contextual    | Muestra un subconjunto de comandos disponibles contextualmente relevante que se muestran como resultado de hacer clic con el botón secundario en un elemento.                                                                               |



 

## <a name="property-and-preview-controls"></a>Propiedades y controles de vista previa

Los controles de propiedades y de vista previa se utilizan para obtener una vista previa de los elementos, así como para ver y editar las propiedades de los elementos.



| Control    | Descripción                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vista previa    | Muestra una vista previa del elemento seleccionado, como una miniatura o un icono dinámico.                                                                                                                                                                       |
| Propiedades | Muestra las propiedades del elemento seleccionado. En el caso de las selecciones múltiples, se muestra un resumen de las propiedades del grupo de elementos seleccionado. En el caso de una selección nula, muestra un resumen de las propiedades de la página actual (contenido del control ListView). |



 

## <a name="filtering-and-view-controls"></a>Filtrar y ver controles

Los controles de filtro y vista se usan para manipular el conjunto de elementos de ListView y para cambiar la presentación de los elementos en el control ListView.



| Control   | Descripción                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filter    | Filtra u organiza los elementos de un control ListView basándose en las propiedades enumeradas como columnas. Al hacer clic en una columna, se ordena por esa propiedad. |
| Wordwheel | Filtra de forma dinámica e incremental los elementos mostrados en un control ListView en función de una cadena de texto de entrada.                      |
| Ver      | Permite al usuario cambiar el modo de vista de un control ListView. Se puede usar un control deslizante para determinar el tamaño de los iconos.                |



 

## <a name="listview-control"></a>ListView (control)

El control ListView se usa para ver un conjunto de elementos en uno de los cuatro modos de vista: detalles, mosaicos, iconos o panorama. El control ListView también permite al usuario seleccionar y activar uno o más elementos.

> [!Caution]  
> Aunque algunos de estos controles tienen nombres y/o funcionalidad similar a los controles estándar de Windows Presentation Foundation (WPF) que se encuentran en el espacio de nombres System. Windows. Controls, son clases distintas.

 

Estos controles independientes funcionan en gran medida a través de eventos generados por la interacción del usuario o por los propios controles. En la tabla siguiente se muestran las tres categorías de eventos principales.



| Categoría de eventos | Ejemplo                                                       |
|----------------|---------------------------------------------------------------|
| Navegación     | Pasar de una página a otra.                               |
| Selección      | Cambiar la selección actual en el control ListView.               |
| Ver cambio    | Cambiar el orden de presentación o el modo de vista en el control ListView. |



 

 

 
