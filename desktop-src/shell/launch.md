---
description: Una vez que la aplicación ha encontrado un objeto de archivo, el paso siguiente suele actuar sobre él de alguna manera.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908745"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="2dc46-103">Iniciar aplicaciones (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="2dc46-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="2dc46-104">Una vez que la aplicación ha encontrado un objeto de archivo, el paso siguiente suele actuar sobre él de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="2dc46-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="2dc46-105">Por ejemplo, es posible que la aplicación desee iniciar otra aplicación que permita al usuario modificar un archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="2dc46-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="2dc46-106">Si el archivo de interés es un ejecutable, es posible que la aplicación desee simplemente iniciarlo.</span><span class="sxs-lookup"><span data-stu-id="2dc46-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="2dc46-107">En este documento se explica cómo usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para realizar estas tareas.</span><span class="sxs-lookup"><span data-stu-id="2dc46-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="2dc46-108">Usar ShellExecute y ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="2dc46-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="2dc46-109">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="2dc46-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="2dc46-110">Usar ShellExecuteEx para proporcionar servicios de activación desde un sitio</span><span class="sxs-lookup"><span data-stu-id="2dc46-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="2dc46-111">Usar ShellExecute para iniciar el cuadro de diálogo de búsqueda</span><span class="sxs-lookup"><span data-stu-id="2dc46-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="2dc46-112">Un ejemplo sencillo de cómo usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="2dc46-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="2dc46-113">Usar ShellExecute y ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="2dc46-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="2dc46-114">Para usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), la aplicación debe especificar el objeto de archivo o carpeta en el que se actuará y un *verbo* que especifique la operación.</span><span class="sxs-lookup"><span data-stu-id="2dc46-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="2dc46-115">Para **ShellExecute**, asigne estos valores a los parámetros adecuados.</span><span class="sxs-lookup"><span data-stu-id="2dc46-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="2dc46-116">En el caso de **ShellExecuteEx**, rellene los miembros adecuados de una estructura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2dc46-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="2dc46-117">También hay otros miembros o parámetros que se pueden usar para ajustar el comportamiento de las dos funciones.</span><span class="sxs-lookup"><span data-stu-id="2dc46-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="2dc46-118">Los objetos de archivos y carpetas pueden formar parte del sistema de archivos o de los objetos virtuales, y se pueden identificar mediante rutas de acceso o punteros a listas de identificadores de elementos (PIDL).</span><span class="sxs-lookup"><span data-stu-id="2dc46-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="2dc46-119">Verbos de objeto</span><span class="sxs-lookup"><span data-stu-id="2dc46-119">Object Verbs</span></span>

<span data-ttu-id="2dc46-120">Los verbos disponibles para un objeto son esencialmente los elementos que se encuentran en el menú contextual de un objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc46-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="2dc46-121">Para averiguar qué verbos están disponibles, busque en el registro en</span><span class="sxs-lookup"><span data-stu-id="2dc46-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="2dc46-122">**HKEY \_ Clases \_** \\ **CLSID** raíz \\ *{Object \_ CLSID}* \\ **Shell** \\ *Verb*</span><span class="sxs-lookup"><span data-stu-id="2dc46-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="2dc46-123">donde el *objeto \_ CLSID* es el identificador de clase (CLSID) del objeto y *Verb* es el nombre del verbo disponible.</span><span class="sxs-lookup"><span data-stu-id="2dc46-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="2dc46-124">La  \\ subclave del **comando** Verb contiene los datos que indican lo que ocurre cuando se invoca ese verbo.</span><span class="sxs-lookup"><span data-stu-id="2dc46-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="2dc46-125">Para averiguar qué verbos están disponibles para los [objetos de Shell predefinidos](handlers.md), busque en el registro en</span><span class="sxs-lookup"><span data-stu-id="2dc46-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="2dc46-126">**HKEY \_ \_** \\ *\_ Nombre de objeto* raíz de clases \\  \\ *verbo* de Shell</span><span class="sxs-lookup"><span data-stu-id="2dc46-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="2dc46-127">donde *Object \_ Name* es el nombre del objeto de Shell predefinido.</span><span class="sxs-lookup"><span data-stu-id="2dc46-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="2dc46-128">Una vez más , la \\ subclave del **comando** Verb contiene los datos que indican lo que ocurre cuando se invoca ese verbo.</span><span class="sxs-lookup"><span data-stu-id="2dc46-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="2dc46-129">Los verbos disponibles comúnmente incluyen:</span><span class="sxs-lookup"><span data-stu-id="2dc46-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="2dc46-130">Verbo</span><span class="sxs-lookup"><span data-stu-id="2dc46-130">Verb</span></span>       | <span data-ttu-id="2dc46-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dc46-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc46-132">edición</span><span class="sxs-lookup"><span data-stu-id="2dc46-132">edit</span></span>       | <span data-ttu-id="2dc46-133">Inicia un editor y abre el documento para su edición.</span><span class="sxs-lookup"><span data-stu-id="2dc46-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="2dc46-134">find</span><span class="sxs-lookup"><span data-stu-id="2dc46-134">find</span></span>       | <span data-ttu-id="2dc46-135">Inicia una búsqueda a partir del directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="2dc46-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="2dc46-136">abrir</span><span class="sxs-lookup"><span data-stu-id="2dc46-136">open</span></span>       | <span data-ttu-id="2dc46-137">Inicia una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2dc46-137">Launches an application.</span></span> <span data-ttu-id="2dc46-138">Si este archivo no es un archivo ejecutable, se inicia su aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="2dc46-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="2dc46-139">imprimir</span><span class="sxs-lookup"><span data-stu-id="2dc46-139">print</span></span>      | <span data-ttu-id="2dc46-140">Imprime el archivo de documento.</span><span class="sxs-lookup"><span data-stu-id="2dc46-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="2dc46-141">properties</span><span class="sxs-lookup"><span data-stu-id="2dc46-141">properties</span></span> | <span data-ttu-id="2dc46-142">Muestra las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="2dc46-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="2dc46-143">runas</span><span class="sxs-lookup"><span data-stu-id="2dc46-143">runas</span></span>      | <span data-ttu-id="2dc46-144">Inicia una aplicación como administrador.</span><span class="sxs-lookup"><span data-stu-id="2dc46-144">Launches an application as Administrator.</span></span> <span data-ttu-id="2dc46-145">Control de cuentas de usuario (UAC) solicitará al usuario su consentimiento para</span><span class="sxs-lookup"><span data-stu-id="2dc46-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="2dc46-146">Ejecute la aplicación con privilegios elevados o escriba las credenciales de una cuenta de administrador usada para ejecutar el</span><span class="sxs-lookup"><span data-stu-id="2dc46-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="2dc46-147">aplicación Aha!.</span><span class="sxs-lookup"><span data-stu-id="2dc46-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="2dc46-148">Cada verbo corresponde al comando que se utilizaría para iniciar la aplicación desde una ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="2dc46-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="2dc46-149">El verbo **Open** es un buen ejemplo, ya que normalmente se admite.</span><span class="sxs-lookup"><span data-stu-id="2dc46-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="2dc46-150">En el caso de los archivos. exe, **abra** simplemente inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2dc46-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="2dc46-151">Sin embargo, se suele usar para iniciar una aplicación que funciona en un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="2dc46-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="2dc46-152">Por ejemplo, Microsoft WordPad puede abrir los archivos. txt.</span><span class="sxs-lookup"><span data-stu-id="2dc46-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="2dc46-153">El verbo **Open** de un archivo. txt se correspondería a algo como el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="2dc46-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="2dc46-154">Al usar [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para abrir un archivo. txt, Wordpad.exe se inicia con el archivo especificado como su argumento.</span><span class="sxs-lookup"><span data-stu-id="2dc46-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="2dc46-155">Algunos comandos pueden tener argumentos adicionales, como marcas, que se pueden agregar según sea necesario para iniciar la aplicación correctamente.</span><span class="sxs-lookup"><span data-stu-id="2dc46-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="2dc46-156">Para obtener más información sobre los menús contextuales y los verbos, vea [extender los menús contextuales](context.md).</span><span class="sxs-lookup"><span data-stu-id="2dc46-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="2dc46-157">En general, intentar determinar la lista de verbos disponibles para un archivo determinado es algo complicado.</span><span class="sxs-lookup"><span data-stu-id="2dc46-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="2dc46-158">En muchos casos, puede simplemente establecer el parámetro *lpVerb* en **null**, que invoca el comando predeterminado para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc46-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="2dc46-159">Este procedimiento suele ser equivalente a establecer *lpVerb* en "Open", pero algunos tipos de archivo pueden tener un comando predeterminado diferente.</span><span class="sxs-lookup"><span data-stu-id="2dc46-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="2dc46-160">Para obtener más información, consulte extensión de los [menús contextuales](context.md) y la documentación de referencia de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="2dc46-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="2dc46-161">Usar ShellExecuteEx para proporcionar servicios de activación desde un sitio</span><span class="sxs-lookup"><span data-stu-id="2dc46-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="2dc46-162">Los servicios de una cadena de sitios pueden controlar muchos comportamientos de activación de elementos.</span><span class="sxs-lookup"><span data-stu-id="2dc46-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="2dc46-163">A partir de Windows 8, puede proporcionar un puntero a la cadena de sitios a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para habilitar estos comportamientos.</span><span class="sxs-lookup"><span data-stu-id="2dc46-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="2dc46-164">Para proporcionar el sitio a **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="2dc46-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="2dc46-165">Especifique la marca de \_ máscara See \_ \_ HINST \_ is \_ site Flag en el miembro **fMask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="2dc46-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="2dc46-166">Proporcione [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el miembro **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="2dc46-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="2dc46-167">Usar ShellExecute para iniciar el cuadro de diálogo de búsqueda</span><span class="sxs-lookup"><span data-stu-id="2dc46-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="2dc46-168">Cuando un usuario hace clic con el botón secundario en un icono de carpeta en el explorador de Windows, uno de los elementos de menú es "Buscar".</span><span class="sxs-lookup"><span data-stu-id="2dc46-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="2dc46-169">Si seleccionan ese elemento, el shell inicia su utilidad de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2dc46-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="2dc46-170">Esta utilidad muestra un cuadro de diálogo que se puede usar para buscar en archivos una cadena de texto especificada.</span><span class="sxs-lookup"><span data-stu-id="2dc46-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="2dc46-171">Una aplicación puede iniciar mediante programación la utilidad de búsqueda para un directorio llamando a [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "Find" como parámetro *lpVerb* y la ruta de acceso del directorio como el parámetro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="2dc46-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="2dc46-172">Por ejemplo, la siguiente línea de código inicia la utilidad de búsqueda para el directorio c: mis \\ programas.</span><span class="sxs-lookup"><span data-stu-id="2dc46-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="2dc46-173">Un ejemplo sencillo de cómo usar ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="2dc46-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="2dc46-174">La siguiente aplicación de consola de ejemplo muestra el uso de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="2dc46-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="2dc46-175">La mayoría del código de comprobación de errores se ha omitido para mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="2dc46-175">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="2dc46-176">En primer lugar, la aplicación recupera el PIDL del directorio de Windows y enumera su contenido hasta que encuentra el primer archivo. bmp.</span><span class="sxs-lookup"><span data-stu-id="2dc46-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="2dc46-177">A diferencia del ejemplo anterior, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) se usa para recuperar el nombre de análisis del archivo en lugar de su nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="2dc46-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="2dc46-178">Dado que se trata de una carpeta del sistema de archivos, el nombre de análisis es una ruta de acceso completa, que es lo que se necesita para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="2dc46-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="2dc46-179">Una vez que se encuentra el primer archivo. bmp, los valores adecuados se asignan a los miembros de una estructura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2dc46-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="2dc46-180">El miembro **lpFile** se establece en el nombre de análisis del archivo y el miembro **lpVerb** en **null** para comenzar la operación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2dc46-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="2dc46-181">En este caso, la operación predeterminada es "Open".</span><span class="sxs-lookup"><span data-stu-id="2dc46-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="2dc46-182">A continuación, la estructura se pasa a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), que inicia el controlador predeterminado para los archivos de mapa de bits, normalmente MSPaint.exe, para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="2dc46-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="2dc46-183">Una vez que la función devuelve, se liberan los PIDL y se libera la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="2dc46-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
