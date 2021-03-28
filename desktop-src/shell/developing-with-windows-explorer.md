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
# <a name="developing-with-windows-explorer"></a><span data-ttu-id="7d5d0-103">Desarrollo con el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="7d5d0-103">Developing with Windows Explorer</span></span>

<span data-ttu-id="7d5d0-104">El explorador de Windows es una eficaz aplicación de exploración y administración de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-104">Windows Explorer is a powerful resource-browsing and management application.</span></span> <span data-ttu-id="7d5d0-105">Se puede tener acceso al explorador de Windows como un todo integrado a través de Explorer.exe o la interfaz [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="7d5d0-105">Windows Explorer can be accessed as an integrated whole through Explorer.exe or the [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="7d5d0-106">El explorador de Windows (Explorer.exe) se puede generar como un proceso independiente mediante [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una función similar.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-106">Windows Explorer (Explorer.exe) can be spawned as a separate process using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) or a similar function.</span></span>

> [!Note]  
> <span data-ttu-id="7d5d0-107">Las opciones de línea de comandos para Explorer.exe se documentan en el sitio de soporte técnico de Microsoft Windows en el artículo [Explorador de windows Command-Line opciones](https://support.microsoft.com/kb/152457).</span><span class="sxs-lookup"><span data-stu-id="7d5d0-107">Command-line options for Explorer.exe are documented on the Microsoft Windows Support site in the article [Windows Explorer Command-Line Options](https://support.microsoft.com/kb/152457).</span></span>

 

<span data-ttu-id="7d5d0-108">Las ventanas de explorador abiertas se pueden detectar y programar mediante [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) y se pueden crear nuevas instancias del explorador de Windows mediante [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).</span><span class="sxs-lookup"><span data-stu-id="7d5d0-108">Open explorer windows can be discovered and programmed by using [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID\_ShellWindows), and new instances of Windows Explorer can be created by using [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID\_ShellBrowserWindow).</span></span>

<span data-ttu-id="7d5d0-109">En el ejemplo de código siguiente se muestra cómo se puede usar el modelo de automatización del explorador de Windows para crear y detectar ventanas del explorador que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-109">The following code sample demonstrates how the Windows Explorer automation model can be used to create and discover explorer windows that are running.</span></span>


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



<span data-ttu-id="7d5d0-110">El área cliente del explorador de Windows se puede hospedar mediante la interfaz [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) .</span><span class="sxs-lookup"><span data-stu-id="7d5d0-110">The Windows Explorer client area can be hosted by using the [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) interface.</span></span> <span data-ttu-id="7d5d0-111">El cliente del explorador de Windows y los controles de árbol de espacios de nombres son componentes estándar de Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-111">The Windows Explorer client and the namespace tree controls are standard components of Windows Vista and later.</span></span> <span data-ttu-id="7d5d0-112">Los desarrolladores pueden reutilizar las interfaces como componentes de compilación.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-112">Developers can reuse the interfaces as building components.</span></span> <span data-ttu-id="7d5d0-113">Un uso común de estos controles es crear exploradores personalizados adecuados para el dominio del problema.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-113">One common use of these controls is to create customized explorers appropriate to the problem domain.</span></span>

<span data-ttu-id="7d5d0-114">Los controles del explorador de Windows se clasifican en las siguientes categorías funcionales:</span><span class="sxs-lookup"><span data-stu-id="7d5d0-114">The controls in Windows Explorer are classified into the following functional categories:</span></span>

-   [<span data-ttu-id="7d5d0-115">Controles de navegación</span><span class="sxs-lookup"><span data-stu-id="7d5d0-115">Navigation Controls</span></span>](#navigation-controls)
-   [<span data-ttu-id="7d5d0-116">Controles de comando</span><span class="sxs-lookup"><span data-stu-id="7d5d0-116">Command Controls</span></span>](#command-controls)
-   [<span data-ttu-id="7d5d0-117">Propiedades y controles de vista previa</span><span class="sxs-lookup"><span data-stu-id="7d5d0-117">Property and Preview Controls</span></span>](#property-and-preview-controls)
-   [<span data-ttu-id="7d5d0-118">Filtrar y ver controles</span><span class="sxs-lookup"><span data-stu-id="7d5d0-118">Filtering and View Controls</span></span>](#filtering-and-view-controls)
-   [<span data-ttu-id="7d5d0-119">ListView (control)</span><span class="sxs-lookup"><span data-stu-id="7d5d0-119">Listview Control</span></span>](#listview-control)

## <a name="navigation-controls"></a><span data-ttu-id="7d5d0-120">Controles de navegación</span><span class="sxs-lookup"><span data-stu-id="7d5d0-120">Navigation Controls</span></span>

<span data-ttu-id="7d5d0-121">Los controles de navegación ayudan a los usuarios a determinar el contexto y navegar por el espacio de dominio lógico asociado, denominado pagespace.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-121">Navigation controls assist users in determining context and navigating the associated logical domain space, called the pagespace.</span></span> <span data-ttu-id="7d5d0-122">Por ejemplo, pagespace para el explorador de Windows es el espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-122">For example, the pagespace for Windows Explorer is the Shell namespace.</span></span> <span data-ttu-id="7d5d0-123">Pagespaces se componen de cero o más páginas.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-123">Pagespaces are composed of zero or more pages.</span></span>

<span data-ttu-id="7d5d0-124">En la tabla siguiente se enumeran y describen los controles de navegación disponibles en el explorador de Windows en Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-124">The following table lists and describes the navigation controls available in Windows Explorer in the Windows Vista and later operating systems.</span></span>



| <span data-ttu-id="7d5d0-125">Control de navegación</span><span class="sxs-lookup"><span data-stu-id="7d5d0-125">Navigation control</span></span>               | <span data-ttu-id="7d5d0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d5d0-126">Description</span></span>                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d0-127">Barra de direcciones (control de ruta de navegación)</span><span class="sxs-lookup"><span data-stu-id="7d5d0-127">Address Bar (Breadcrumb control)</span></span> | <span data-ttu-id="7d5d0-128">Muestra la dirección de la página actual en pagespace.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-128">Displays the address of the current page in the pagespace.</span></span> <span data-ttu-id="7d5d0-129">Se puede hacer clic en los botones de navegación para desplazarse a cualquier antecesor en el pagespace.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-129">Breadcrumb buttons can be clicked to navigate to any ancestor in the pagespace.</span></span> <span data-ttu-id="7d5d0-130">Los usuarios también pueden escribir direcciones URL y rutas de acceso para navegar.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-130">Users can also type URLs and paths to navigate.</span></span> |
| <span data-ttu-id="7d5d0-131">Árbol de carpetas</span><span class="sxs-lookup"><span data-stu-id="7d5d0-131">Folder Tree</span></span>                      | <span data-ttu-id="7d5d0-132">Proporciona una nueva versión de un control de árbol, optimizada para pagespacess grandes.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-132">Provides a new version of a tree control, optimized for large pagespaces.</span></span>                                                                                                                  |
| <span data-ttu-id="7d5d0-133">Viajes</span><span class="sxs-lookup"><span data-stu-id="7d5d0-133">Travel</span></span>                           | <span data-ttu-id="7d5d0-134">Habilita la navegación relativa a través de botones de estilo Web como **atrás** y **adelante**.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-134">Enables relative navigation through web-style buttons such as **Back** and **Forward**.</span></span>                                                                                                    |
| <span data-ttu-id="7d5d0-135">Title</span><span class="sxs-lookup"><span data-stu-id="7d5d0-135">Title</span></span>                            | <span data-ttu-id="7d5d0-136">Muestra el nombre y el contexto del explorador actual.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-136">Displays the current explorer name and context.</span></span>                                                                                                                                            |
| <span data-ttu-id="7d5d0-137">Pagespace</span><span class="sxs-lookup"><span data-stu-id="7d5d0-137">Pagespace</span></span>                        | <span data-ttu-id="7d5d0-138">Muestra la rama actual de pagespace.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-138">Displays the current branch of the pagespace.</span></span> <span data-ttu-id="7d5d0-139">Las páginas se pueden ordenar por criterios diferentes.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-139">Pages can be ordered by different criteria.</span></span> <span data-ttu-id="7d5d0-140">Los usuarios pueden hacer clic en una página para ir a ella.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-140">Users can click a page to navigate to it.</span></span>                                                        |



 

## <a name="command-controls"></a><span data-ttu-id="7d5d0-141">Controles de comando</span><span class="sxs-lookup"><span data-stu-id="7d5d0-141">Command Controls</span></span>

<span data-ttu-id="7d5d0-142">Los controles de comandos anuncian las características y la funcionalidad del explorador de Windows a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-142">Command controls advertise the features and functionality of the Windows Explorer to users.</span></span> <span data-ttu-id="7d5d0-143">Estos controles realizan acciones generales o acciones específicas de un elemento o elementos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-143">These controls perform either general actions or actions specific to one selected item or items.</span></span>



| <span data-ttu-id="7d5d0-144">Control de comandos</span><span class="sxs-lookup"><span data-stu-id="7d5d0-144">Command control</span></span> | <span data-ttu-id="7d5d0-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d5d0-145">Description</span></span>                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d0-146">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="7d5d0-146">Toolbar</span></span>         | <span data-ttu-id="7d5d0-147">Muestra botones para los comandos de uso frecuente (una nueva versión de una barra de herramientas de comandos).</span><span class="sxs-lookup"><span data-stu-id="7d5d0-147">Displays buttons for commonly used commands (a new version of a command toolbar).</span></span> <span data-ttu-id="7d5d0-148">Entre las opciones de personalización se incluyen botones desplegables, botones de expansión, texto descriptivo opcional y un área de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-148">Customization options include drop-down buttons, split buttons, optional descriptive text, and an overflow area.</span></span> |
| <span data-ttu-id="7d5d0-149">Imagen prominente</span><span class="sxs-lookup"><span data-stu-id="7d5d0-149">Hero</span></span>            | <span data-ttu-id="7d5d0-150">Aparece como un único control personalizado y opcional en el centro de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-150">Appears as a single, optional, custom control in the center of the toolbar.</span></span> <span data-ttu-id="7d5d0-151">Representa el comando principal del contexto actual.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-151">It represents the primary command for the current context.</span></span>                                                             |
| <span data-ttu-id="7d5d0-152">Barra de menús</span><span class="sxs-lookup"><span data-stu-id="7d5d0-152">Menu Bar</span></span>        | <span data-ttu-id="7d5d0-153">Presenta comandos a través de menús.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-153">Presents commands through menus.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="7d5d0-154">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="7d5d0-154">Context Menu</span></span>    | <span data-ttu-id="7d5d0-155">Muestra un subconjunto de comandos disponibles contextualmente relevante que se muestran como resultado de hacer clic con el botón secundario en un elemento.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-155">Lists a contextually relevant subset of available commands that are displayed as a result of right-clicking an item.</span></span>                                                                               |



 

## <a name="property-and-preview-controls"></a><span data-ttu-id="7d5d0-156">Propiedades y controles de vista previa</span><span class="sxs-lookup"><span data-stu-id="7d5d0-156">Property and Preview Controls</span></span>

<span data-ttu-id="7d5d0-157">Los controles de propiedades y de vista previa se utilizan para obtener una vista previa de los elementos, así como para ver y editar las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-157">Property and preview controls are used to preview items, and to view and edit item properties.</span></span>



| <span data-ttu-id="7d5d0-158">Control</span><span class="sxs-lookup"><span data-stu-id="7d5d0-158">Control</span></span>    | <span data-ttu-id="7d5d0-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d5d0-159">Description</span></span>                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d0-160">Vista previa</span><span class="sxs-lookup"><span data-stu-id="7d5d0-160">Preview</span></span>    | <span data-ttu-id="7d5d0-161">Muestra una vista previa del elemento seleccionado, como una miniatura o un icono dinámico.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-161">Displays a preview of the selected item, such as a thumbnail or a Live Icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="7d5d0-162">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d5d0-162">Properties</span></span> | <span data-ttu-id="7d5d0-163">Muestra las propiedades del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-163">Displays properties of the selected item.</span></span> <span data-ttu-id="7d5d0-164">En el caso de las selecciones múltiples, se muestra un resumen de las propiedades del grupo de elementos seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-164">For multiple selections, it displays a summary of properties for the selected group of items.</span></span> <span data-ttu-id="7d5d0-165">En el caso de una selección nula, muestra un resumen de las propiedades de la página actual (contenido del control ListView).</span><span class="sxs-lookup"><span data-stu-id="7d5d0-165">For a null selection, it displays a summary of properties for the current page (contents of the listview).</span></span> |



 

## <a name="filtering-and-view-controls"></a><span data-ttu-id="7d5d0-166">Filtrar y ver controles</span><span class="sxs-lookup"><span data-stu-id="7d5d0-166">Filtering and View Controls</span></span>

<span data-ttu-id="7d5d0-167">Los controles de filtro y vista se usan para manipular el conjunto de elementos de ListView y para cambiar la presentación de los elementos en el control ListView.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-167">Filtering and view controls are used to manipulate the set of items in the listview and to change the presentation of items in the listview.</span></span>



| <span data-ttu-id="7d5d0-168">Control</span><span class="sxs-lookup"><span data-stu-id="7d5d0-168">Control</span></span>   | <span data-ttu-id="7d5d0-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d5d0-169">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d0-170">Filter</span><span class="sxs-lookup"><span data-stu-id="7d5d0-170">Filter</span></span>    | <span data-ttu-id="7d5d0-171">Filtra u organiza los elementos de un control ListView basándose en las propiedades enumeradas como columnas.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-171">Filters or arranges items in a listview based on properties listed as columns.</span></span> <span data-ttu-id="7d5d0-172">Al hacer clic en una columna, se ordena por esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-172">Clicking on a column sorts by that property.</span></span> |
| <span data-ttu-id="7d5d0-173">Wordwheel</span><span class="sxs-lookup"><span data-stu-id="7d5d0-173">Wordwheel</span></span> | <span data-ttu-id="7d5d0-174">Filtra de forma dinámica e incremental los elementos mostrados en un control ListView en función de una cadena de texto de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-174">Dynamically and incrementally filters the displayed items in a listview based on an input text string.</span></span>                      |
| <span data-ttu-id="7d5d0-175">Ver</span><span class="sxs-lookup"><span data-stu-id="7d5d0-175">View</span></span>      | <span data-ttu-id="7d5d0-176">Permite al usuario cambiar el modo de vista de un control ListView.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-176">Enables the user to change the view mode of a listview control.</span></span> <span data-ttu-id="7d5d0-177">Se puede usar un control deslizante para determinar el tamaño de los iconos.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-177">A slider can be used to determine icon size.</span></span>                |



 

## <a name="listview-control"></a><span data-ttu-id="7d5d0-178">ListView (control)</span><span class="sxs-lookup"><span data-stu-id="7d5d0-178">Listview Control</span></span>

<span data-ttu-id="7d5d0-179">El control ListView se usa para ver un conjunto de elementos en uno de los cuatro modos de vista: detalles, mosaicos, iconos o panorama.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-179">The listview control is used to view a set of items in one of four view modes: details, tiles, icons, or panorama.</span></span> <span data-ttu-id="7d5d0-180">El control ListView también permite al usuario seleccionar y activar uno o más elementos.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-180">The listview control also enables the user to select and activate one or more items.</span></span>

> [!Caution]  
> <span data-ttu-id="7d5d0-181">Aunque algunos de estos controles tienen nombres y/o funcionalidad similar a los controles estándar de Windows Presentation Foundation (WPF) que se encuentran en el espacio de nombres System. Windows. Controls, son clases distintas.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-181">Although some of these controls have names and/or functionality that is similar to standard Windows Presentation Foundation (WPF) controls found in the System.Windows.Controls namespace, they are distinct classes.</span></span>

 

<span data-ttu-id="7d5d0-182">Estos controles independientes funcionan en gran medida a través de eventos generados por la interacción del usuario o por los propios controles.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-182">These separate controls work together largely through events generated either by user interaction or by the controls themselves.</span></span> <span data-ttu-id="7d5d0-183">En la tabla siguiente se muestran las tres categorías de eventos principales.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-183">The following table shows the three primary event categories.</span></span>



| <span data-ttu-id="7d5d0-184">Categoría de eventos</span><span class="sxs-lookup"><span data-stu-id="7d5d0-184">Event category</span></span> | <span data-ttu-id="7d5d0-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d5d0-185">Example</span></span>                                                       |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="7d5d0-186">Navegación</span><span class="sxs-lookup"><span data-stu-id="7d5d0-186">Navigation</span></span>     | <span data-ttu-id="7d5d0-187">Pasar de una página a otra.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-187">Going from one page to another.</span></span>                               |
| <span data-ttu-id="7d5d0-188">Selección</span><span class="sxs-lookup"><span data-stu-id="7d5d0-188">Selection</span></span>      | <span data-ttu-id="7d5d0-189">Cambiar la selección actual en el control ListView.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-189">Changing the current selection in the listview.</span></span>               |
| <span data-ttu-id="7d5d0-190">Ver cambio</span><span class="sxs-lookup"><span data-stu-id="7d5d0-190">View Change</span></span>    | <span data-ttu-id="7d5d0-191">Cambiar el orden de presentación o el modo de vista en el control ListView.</span><span class="sxs-lookup"><span data-stu-id="7d5d0-191">Changing the presentation order or view mode in the listview.</span></span> |



 

 

 
