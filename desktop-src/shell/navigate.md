---
description: Ahora tiene todos los elementos esenciales necesarios para navegar en cualquier parte del espacio de nombres.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navegar por el espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082236"
---
# <a name="navigating-the-namespace"></a><span data-ttu-id="a7547-103">Navegar por el espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a7547-103">Navigating the Namespace</span></span>

<span data-ttu-id="a7547-104">Ahora tiene todos los elementos esenciales necesarios para navegar en cualquier parte del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="a7547-104">You now have all the essential elements needed to navigate anywhere in the namespace.</span></span> <span data-ttu-id="a7547-105">La manera más sencilla de empezar es hacer que la aplicación llame a [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) para recuperar la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del escritorio.</span><span class="sxs-lookup"><span data-stu-id="a7547-105">The simplest way to start is to have your application call [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) to retrieve the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="a7547-106">Después, para navegar hacia abajo por el espacio de nombres, la aplicación puede seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a7547-106">Then, to navigate downward through the namespace, your application can follow these steps:</span></span>

1.  <span data-ttu-id="a7547-107">Enumerar el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a7547-107">Enumerate the folder's contents.</span></span>
2.  <span data-ttu-id="a7547-108">Determine qué objetos son subcarpetas y seleccione uno.</span><span class="sxs-lookup"><span data-stu-id="a7547-108">Determine which objects are subfolders, and select one.</span></span>
3.  <span data-ttu-id="a7547-109">Enlazar a la subcarpeta para recuperar su interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="a7547-109">Bind to the subfolder to retrieve its [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span>

<span data-ttu-id="a7547-110">Repita estos pasos tantas veces como sea necesario para alcanzar el destino.</span><span class="sxs-lookup"><span data-stu-id="a7547-110">Repeat these steps as often as necessary to reach the target.</span></span>

## <a name="a-simple-example-of-namespace-navigation"></a><span data-ttu-id="a7547-111">Un ejemplo sencillo de navegación por espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="a7547-111">A Simple Example of Namespace Navigation</span></span>

<span data-ttu-id="a7547-112">El siguiente fragmento de código de ejemplo es una aplicación de consola simple que muestra una serie de los procedimientos descritos en las secciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="a7547-112">The following piece of sample code is a simple console application that illustrates a number of the procedures discussed in the preceding sections.</span></span> <span data-ttu-id="a7547-113">Se ha omitido la comprobación de errores para mayor claridad.</span><span class="sxs-lookup"><span data-stu-id="a7547-113">Error checking has been omitted for clarity.</span></span> <span data-ttu-id="a7547-114">La aplicación realiza las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7547-114">The application performs the following tasks:</span></span>

1.  <span data-ttu-id="a7547-115">Recupera la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta de archivos de programa ([mediante la interfaz IShellFolder](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a7547-115">Retrieves the Program Files folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface ([Using the IShellFolder Interface](folder-info.md)).</span></span>
2.  <span data-ttu-id="a7547-116">Enumera el contenido de la carpeta ([enumerando el contenido de una carpeta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a7547-116">Enumerates the contents of the folder ([Enumerating the Contents of a Folder](folder-info.md)).</span></span>
3.  <span data-ttu-id="a7547-117">Determina todos los nombres para mostrar e imprime (determina[los nombres para mostrar y otras propiedades](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a7547-117">Determines all the display names and prints them ([Determining Display Names and Other Properties](folder-info.md)).</span></span>
4.  <span data-ttu-id="a7547-118">Busca una subcarpeta ([obteniendo un puntero a la interfaz IShellFolder de una subcarpeta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a7547-118">Looks for a subfolder ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
5.  <span data-ttu-id="a7547-119">Enlaza a la primera subcarpeta que encuentra ([al obtener un puntero a la interfaz IShellFolder de una subcarpeta](folder-info.md)).</span><span class="sxs-lookup"><span data-stu-id="a7547-119">Binds to the first subfolder it finds ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).</span></span>
6.  <span data-ttu-id="a7547-120">Imprime los nombres para mostrar de los objetos en la subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="a7547-120">Prints the display names of the objects in the subfolder.</span></span>


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>

main()
{
    LPITEMIDLIST pidlProgFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfFirstFolder = NULL;
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfProgFiles = NULL;
    LPENUMIDLIST ppenum = NULL;
    ULONG celtFetched;
    HRESULT hr;
    STRRET strDispName;
    TCHAR pszDisplayName[MAX_PATH];
    ULONG uAttr;
   
    CoInitialize( NULL );
    
    hr = SHGetFolderLocation(NULL, CSIDL_PROGRAM_FILES, NULL, 0, &pidlProgFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlProgFiles, NULL, IID_IShellFolder, (LPVOID *) &psfProgFiles);
    psfDeskTop->Release();

    hr = psfProgFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfProgFiles->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
        cout << pszDisplayName << '\n';
        if(!psfFirstFolder)
        {
            uAttr = SFGAO_FOLDER;
            psfProgFiles->GetAttributesOf(1, (LPCITEMIDLIST *) &pidlItems, &uAttr);
            if(uAttr & SFGAO_FOLDER)
            {
                hr = psfProgFiles->BindToObject(pidlItems, NULL, IID_IShellFolder, (LPVOID *) &psfFirstFolder);
            }
        }
        CoTaskMemFree(pidlItems);
    }

    cout << "\n\n";

    ppenum->Release();

    if(psfFirstFolder)
    {
        hr = psfFirstFolder->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

        while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
        {
            psfFirstFolder->GetDisplayNameOf(pidlItems, SHGDN_INFOLDER, &strDispName);
            StrRetToBuf(&strDispName, pidlItems, pszDisplayName, MAX_PATH);
            cout << pszDisplayName << '\n';
            CoTaskMemFree(pidlItems);
        }
    }

    ppenum->Release();
    CoTaskMemFree(pidlProgFiles);
    psfProgFiles->Release();
    psfFirstFolder->Release();

    CoUninitialize();
    return 0;
}
```



 

 
