---
description: Ahora tiene todos los elementos esenciales necesarios para navegar por cualquier lugar del espacio de nombres.
ms.assetid: bd9f903d-bea6-494f-af81-d90457dc2647
title: Navegar por el espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24993369222fb32f9de6c79a0c998b1d7be9f2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572492"
---
# <a name="navigating-the-namespace"></a>Navegar por el espacio de nombres

Ahora tiene todos los elementos esenciales necesarios para navegar por cualquier lugar del espacio de nombres. La manera más sencilla de empezar es hacer que la aplicación llame a [**SHGetDesktopFolder para**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder) recuperar la interfaz [**IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) escritorio. A continuación, para navegar hacia abajo por el espacio de nombres, la aplicación puede seguir estos pasos:

1.  Enumerar el contenido de la carpeta.
2.  Determine qué objetos son subcarpetas y seleccione uno.
3.  Enlace a la subcarpeta para recuperar su [**interfaz IShellFolder.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)

Repita estos pasos con la frecuencia necesaria para llegar al destino.

## <a name="a-simple-example-of-namespace-navigation"></a>Un ejemplo sencillo de navegación de espacio de nombres

El siguiente fragmento de código de ejemplo es una aplicación de consola sencilla que ilustra una serie de procedimientos descritos en las secciones anteriores. Se ha omitido la comprobación de errores para mayor claridad. La aplicación realiza las tareas siguientes:

1.  Recupera la interfaz [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de la carpeta Archivos de programa ([mediante la interfaz IShellFolder](folder-info.md)).
2.  Enumera el contenido de la carpeta ([enumerando el contenido de una carpeta](folder-info.md)).
3.  Determina todos los nombres para mostrar y los imprime (Determinar nombres[para mostrar y otras propiedades).](folder-info.md)
4.  Busca una subcarpeta ( Obtener un puntero a la interfaz[IShellFolder](folder-info.md)de una subcarpeta ).
5.  Enlaza a la primera subcarpeta que encuentra ([Getting a Pointer to a Subfolder's IShellFolder Interface](folder-info.md)).
6.  Imprime los nombres para mostrar de los objetos de la subcarpeta .


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



 

 
