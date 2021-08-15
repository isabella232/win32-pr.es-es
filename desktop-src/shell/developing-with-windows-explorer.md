---
description: Windows Explorer es una aplicación eficaz de exploración y administración de recursos.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Desarrollo con Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d00b513b3ee73c30b100cb4236d2c9fb327e1f9557d12ba86738ee9e910ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460193"
---
# <a name="developing-with-windows-explorer"></a>Desarrollo con Windows Explorer

Windows Explorer es una aplicación eficaz de exploración y administración de recursos. Windows Se puede acceder al Explorador como un conjunto integrado a través Explorer.exe o la [**interfaz IExplorerBrowser.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) Windows El Explorador (Explorer.exe) se puede generar como un proceso independiente mediante [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una función similar.

> [!Note]  
> Las opciones de línea de comandos Explorer.exe se documentan en el sitio de soporte técnico de Microsoft Windows en el artículo Windows [Explorer Command-Line Opciones de .](https://support.microsoft.com/kb/152457)

 

Las ventanas abiertas del explorador se pueden detectar y programar mediante [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID ShellWindows) y se pueden crear nuevas instancias de Windows Explorer mediante \_ [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

En el ejemplo de código siguiente se muestra cómo se puede usar el modelo de automatización Windows Explorer para crear y detectar ventanas del explorador que se están ejecutando.


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



El Windows cliente del Explorador de aplicaciones se puede hospedar mediante la [interfaz IExplorerBrowser.](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) El cliente Windows Explorer y los controles de árbol de espacio de nombres son componentes estándar de Windows Vista y versiones posteriores. Los desarrolladores pueden reutilizar las interfaces como componentes de creación. Un uso común de estos controles es crear exploradores personalizados adecuados para el dominio del problema.

Los controles de Windows Explorer se clasifican en las siguientes categorías funcionales:

-   [Controles de navegación](#navigation-controls)
-   [Controles de comando](#command-controls)
-   [Controles de propiedad y vista previa](#property-and-preview-controls)
-   [Filtrado y controles de vista](#filtering-and-view-controls)
-   [Listview Control](#listview-control)

## <a name="navigation-controls"></a>Controles de navegación

Los controles de navegación ayudan a los usuarios a determinar el contexto y navegar por el espacio de dominio lógico asociado, denominado espacio de páginas. Por ejemplo, el espacio de páginas de Windows Explorer es el espacio de nombres shell. Los espacios de página se componen de cero o más páginas.

En la tabla siguiente se enumeran y describen los controles de navegación disponibles en Windows Explorer en Windows Vista y sistemas operativos posteriores.



| Control de navegación               | Descripción                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de direcciones (control ruta de navegación) | Muestra la dirección de la página actual en el espacio de páginas. Se puede hacer clic en los botones de ruta de navegación para navegar a cualquier antecesor en el espacio de páginas. Los usuarios también pueden escribir direcciones URL y rutas de acceso para navegar. |
| Árbol de carpetas                      | Proporciona una nueva versión de un control de árbol, optimizada para espacios de página grandes.                                                                                                                  |
| Viajes                           | Habilita la navegación relativa a través de botones de estilo web como **Atrás** y **Adelante.**                                                                                                    |
| Título                            | Muestra el nombre y el contexto actuales del explorador.                                                                                                                                            |
| Espacio de páginas                        | Muestra la rama actual del espacio de páginas. Las páginas se pueden ordenar por criterios diferentes. Los usuarios pueden hacer clic en una página para ir a ella.                                                        |



 

## <a name="command-controls"></a>Controles de comando

Los controles de comandos anuncian a los usuarios las características y funcionalidades Windows Explorer. Estos controles realizan acciones generales o acciones específicas de un elemento o elementos seleccionados.



| Control de comandos | Descripción                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra de herramientas         | Muestra los botones de los comandos usados habitualmente (una nueva versión de una barra de herramientas de comandos). Las opciones de personalización incluyen botones desplegables, botones de división, texto descriptivo opcional y un área de desbordamiento. |
| Imagen prominente            | Aparece como un control único, opcional y personalizado en el centro de la barra de herramientas. Representa el comando principal para el contexto actual.                                                             |
| Barra de menús        | Presenta comandos a través de menús.                                                                                                                                                                   |
| Menú contextual    | Enumera un subconjunto pertinente contextualmente de los comandos disponibles que se muestran como resultado de hacer clic con el botón derecho en un elemento.                                                                               |



 

## <a name="property-and-preview-controls"></a>Controles de propiedad y vista previa

Los controles de propiedad y vista previa se usan para obtener una vista previa de los elementos y para ver y editar las propiedades de los elementos.



| Control    | Descripción                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vista previa    | Muestra una vista previa del elemento seleccionado, como una miniatura o un icono en directo.                                                                                                                                                                       |
| Propiedades | Muestra las propiedades del elemento seleccionado. Para varias selecciones, muestra un resumen de las propiedades del grupo de elementos seleccionado. Para una selección nula, muestra un resumen de las propiedades de la página actual (contenido de la vista de lista). |



 

## <a name="filtering-and-view-controls"></a>Filtrado y visualización de controles

Los controles de filtrado y vista se usan para manipular el conjunto de elementos de la vista de lista y para cambiar la presentación de los elementos en la vista de lista.



| Control   | Descripción                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filter    | Filtra u organiza elementos en una vista de lista en función de las propiedades enumeradas como columnas. Al hacer clic en una columna, se ordena por esa propiedad. |
| Rueda de palabras | Filtra dinámica e incrementalmente los elementos mostrados en una vista de lista en función de una cadena de texto de entrada.                      |
| Ver      | Permite al usuario cambiar el modo de vista de un control listview. Se puede usar un control deslizante para determinar el tamaño del icono.                |



 

## <a name="listview-control"></a>Listview Control

El control listview se usa para ver un conjunto de elementos en uno de los cuatro modos de vista: detalles, iconos, iconos o panorama. El control listview también permite al usuario seleccionar y activar uno o varios elementos.

> [!Caution]  
> Aunque algunos de estos controles tienen nombres o funcionalidades similares a los controles Windows Presentation Foundation estándar (WPF) que se encuentran en el sistema. Windows. Controla el espacio de nombres, son clases distintas.

 

Estos controles independientes funcionan conjuntamente en gran medida a través de eventos generados por la interacción del usuario o por los propios controles. En la tabla siguiente se muestran las tres categorías de eventos principales.



| Categoría de eventos | Ejemplo                                                       |
|----------------|---------------------------------------------------------------|
| Navegación     | Pasar de una página a otra.                               |
| Número de selección      | Cambiar la selección actual en la vista de lista.               |
| Ver cambio    | Cambiar el orden de presentación o el modo de vista en la vista de lista. |



 

 

 
