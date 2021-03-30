---
description: Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtener el identificador de una carpeta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997733"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="189d8-103">Obtener el identificador de una carpeta</span><span class="sxs-lookup"><span data-stu-id="189d8-103">Getting a Folder's ID</span></span>

<span data-ttu-id="189d8-104">Para poder usar un objeto de espacio de nombres, necesita una manera de identificarlo.</span><span class="sxs-lookup"><span data-stu-id="189d8-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="189d8-105">Esto significa obtener su puntero a una lista de identificadores de elemento (PIDL) o, en el caso de objetos del sistema de archivos, su ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="189d8-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="189d8-106">En esta sección se describen dos de las formas más sencillas de obtener los identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="189d8-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="189d8-107">Para un enfoque más eficaz que funcione con cualquier carpeta, use la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="189d8-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="189d8-108">Vea obtener [información sobre el contenido de una carpeta](folder-info.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="189d8-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="189d8-109">Cuadro de diálogo OpenFiles</span><span class="sxs-lookup"><span data-stu-id="189d8-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="189d8-110">Cuadro de diálogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="189d8-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="189d8-111">Carpetas especiales y CSIDLs</span><span class="sxs-lookup"><span data-stu-id="189d8-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="189d8-112">Un ejemplo sencillo de cómo usar CSIDLs y SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="189d8-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="189d8-113">Cuadro de diálogo OpenFiles</span><span class="sxs-lookup"><span data-stu-id="189d8-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="189d8-114">Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede usar la interfaz [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) .</span><span class="sxs-lookup"><span data-stu-id="189d8-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="189d8-115">Al llamar a esta interfaz con la marca de **FOS \_ PICKFOLDERS** , se inicia el cuadro de diálogo de [abrir archivos](../dlgbox/open-and-save-as-dialog-boxes.md) comunes en el modo "seleccionar carpetas".</span><span class="sxs-lookup"><span data-stu-id="189d8-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="189d8-116">En Windows Vista y versiones posteriores, esta es la manera recomendada para elegir carpetas.</span><span class="sxs-lookup"><span data-stu-id="189d8-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="189d8-117">Cuadro de diálogo SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="189d8-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="189d8-118">Para permitir que el usuario navegue por el espacio de nombres y seleccione una carpeta, la aplicación puede simplemente invocar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="189d8-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="189d8-119">Al llamar a esta función, se inicia un cuadro de diálogo con una interfaz de usuario que funciona como los cuadros de diálogo comunes [abrir o guardar](../dlgbox/open-and-save-as-dialog-boxes.md) .</span><span class="sxs-lookup"><span data-stu-id="189d8-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="189d8-120">Cuando el usuario selecciona una carpeta, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) devuelve el PIDL completo de la carpeta y su nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="189d8-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="189d8-121">Si la carpeta está en el sistema de archivos, la aplicación puede convertir PIDL en una ruta de acceso llamando a [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span><span class="sxs-lookup"><span data-stu-id="189d8-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="189d8-122">La aplicación también puede restringir el intervalo de carpetas del que el usuario puede seleccionar especificando una carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="189d8-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="189d8-123">Solo se mostrarán las carpetas que están por debajo de esa raíz en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="189d8-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="189d8-124">En la ilustración siguiente se muestra el cuadro de diálogo **SHBrowseForFolder** , con la carpeta raíz establecida en archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="189d8-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![captura de pantalla del cuadro de diálogo Buscar carpeta](images/shell1.png)

<span data-ttu-id="189d8-126">Más adelante se proporciona un ejemplo sencillo de cómo usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) .</span><span class="sxs-lookup"><span data-stu-id="189d8-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="189d8-127">Carpetas especiales y CSIDLs</span><span class="sxs-lookup"><span data-stu-id="189d8-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="189d8-128">Un número de carpetas usadas habitualmente se designa como *especial* en el sistema.</span><span class="sxs-lookup"><span data-stu-id="189d8-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="189d8-129">Estas carpetas tienen un propósito bien definido y la mayoría están presentes en todos los sistemas.</span><span class="sxs-lookup"><span data-stu-id="189d8-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="189d8-130">Incluso si no están presentes inicialmente, sus nombres y ubicaciones todavía están definidos, por lo que se pueden agregar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="189d8-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="189d8-131">La colección de carpetas especiales incluye todas las carpetas virtuales estándar del sistema, como las impresoras, mis documentos y el entorno de red.</span><span class="sxs-lookup"><span data-stu-id="189d8-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="189d8-132">También incluye una serie de carpetas del sistema de archivos estándar, como archivos de programa y sistema.</span><span class="sxs-lookup"><span data-stu-id="189d8-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="189d8-133">Aunque las carpetas son un componente estándar de todos los sistemas, sus nombres y ubicaciones en el espacio de nombres pueden variar.</span><span class="sxs-lookup"><span data-stu-id="189d8-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="189d8-134">Por ejemplo, el directorio del sistema es C: \\ WinNT \\ system32 en algunos sistemas y C: \\ Windows \\ system32 en otros.</span><span class="sxs-lookup"><span data-stu-id="189d8-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="189d8-135">En el pasado, las variables de entorno proporcionaban una manera de determinar el nombre y la ubicación de una carpeta especial en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="189d8-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="189d8-136">El Shell ofrece ahora una forma más sólida y flexible de identificar carpetas especiales, [**CSIDLs**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="189d8-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="189d8-137">En general, debe utilizarlos en lugar de variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="189d8-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="189d8-138">CSIDLs proporcionan una forma uniforme de identificar y ubicar carpetas especiales, con independencia de su nombre o ubicación en un sistema determinado.</span><span class="sxs-lookup"><span data-stu-id="189d8-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="189d8-139">A diferencia de las variables de entorno, CSIDLs se puede usar con carpetas virtuales, así como con carpetas del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="189d8-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="189d8-140">Cada carpeta especial tiene asignada una CSIDL única.</span><span class="sxs-lookup"><span data-stu-id="189d8-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="189d8-141">Por ejemplo, la carpeta archivos de programa del sistema de archivos tiene **los \_ \_ archivos de programa** CSIDL de CSIDL y la carpeta virtual de entorno de red tiene la **\_ red** CSIDL de CSIDL.</span><span class="sxs-lookup"><span data-stu-id="189d8-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="189d8-142">Se usa CSIDL junto con una de varias funciones de Shell para recuperar el PIDL de una carpeta especial o una ruta de acceso de la carpeta del sistema de archivos especial.</span><span class="sxs-lookup"><span data-stu-id="189d8-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="189d8-143">Si la carpeta no existe en un sistema, la aplicación puede obligar a que se cree mediante la combinación de su CSIDL con la **marca de CSIDL \_ \_ Create**.</span><span class="sxs-lookup"><span data-stu-id="189d8-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="189d8-144">CSIDL se puede pasar a las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="189d8-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="189d8-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), que recupera el PIDL de una carpeta especial.</span><span class="sxs-lookup"><span data-stu-id="189d8-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="189d8-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), que recupera la ruta de acceso de una carpeta especial del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="189d8-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="189d8-147">Tenga en cuenta que estas dos funciones se introdujeron con la versión 5,0 del shell y reemplazan las funciones [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) y [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .</span><span class="sxs-lookup"><span data-stu-id="189d8-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="189d8-148">Un ejemplo sencillo de cómo usar CSIDLs y SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="189d8-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="189d8-149">La siguiente función de ejemplo, PidlBrowse, muestra cómo usar CSIDLs para recuperar PIDL de una carpeta y usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) para que el usuario seleccione una carpeta.</span><span class="sxs-lookup"><span data-stu-id="189d8-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="189d8-150">Devuelve el PIDL y el nombre para mostrar de la carpeta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="189d8-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="189d8-151">La aplicación que realiza la llamada pasa un identificador de ventana, que es necesario para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="189d8-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="189d8-152">El parámetro *nCSIDL* es un CSIDL opcional que se usa para especificar una carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="189d8-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="189d8-153">Solo se mostrarán las carpetas situadas debajo de la carpeta raíz en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="189d8-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="189d8-154">La ilustración mostrada anteriormente se generó mediante una llamada a esta función con *nCSIDL* establecido en **\_ \_ los archivos de programa CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="189d8-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="189d8-155">La aplicación que realiza la llamada también pasa un búfer de cadena, *pszDisplayName*, para contener el nombre para mostrar de la carpeta seleccionada cuando PidlBrowse devuelve.</span><span class="sxs-lookup"><span data-stu-id="189d8-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="189d8-156">Es responsabilidad de la aplicación que realiza la llamada liberar el IDList devuelto por **SHBrowseForFolder** mediante [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="189d8-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
