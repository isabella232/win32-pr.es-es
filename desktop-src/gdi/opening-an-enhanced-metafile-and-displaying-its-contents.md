---
description: Esta sección contiene un ejemplo que muestra cómo una aplicación abre un metarchivo mejorado almacenado en disco y muestra la imagen asociada en el área cliente.
ms.assetid: e4e5ef5c-d5ea-4931-bbec-1635e8f08c91
title: Abrir un metarchivo mejorado y mostrar su contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f27ce191d66345e5b46ef355757a9c077cf2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984907"
---
# <a name="opening-an-enhanced-metafile-and-displaying-its-contents"></a><span data-ttu-id="9580e-103">Abrir un metarchivo mejorado y mostrar su contenido</span><span class="sxs-lookup"><span data-stu-id="9580e-103">Opening an Enhanced Metafile and Displaying Its Contents</span></span>

<span data-ttu-id="9580e-104">Esta sección contiene un ejemplo que muestra cómo una aplicación abre un metarchivo mejorado almacenado en disco y muestra la imagen asociada en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="9580e-104">This section contains an example demonstrating how an application opens an enhanced metafile stored on disk and displays the associated picture in the client area.</span></span>

<span data-ttu-id="9580e-105">En el ejemplo se usa el cuadro de diálogo **abrir** común para permitir al usuario seleccionar un metarchivo mejorado en una lista de archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="9580e-105">The example uses the **Open** common dialog box to enable the user to select an enhanced metafile from a list of existing files.</span></span> <span data-ttu-id="9580e-106">A continuación, pasa el nombre del archivo seleccionado a la función [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea) , que devuelve un identificador que identifica el archivo.</span><span class="sxs-lookup"><span data-stu-id="9580e-106">It then passes the name of the selected file to the [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea) function, which returns a handle identifying the file.</span></span> <span data-ttu-id="9580e-107">Este identificador se pasa a la función [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) para mostrar la imagen.</span><span class="sxs-lookup"><span data-stu-id="9580e-107">This handle is passed to the [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) function in order to display the picture.</span></span>


```C++
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace occurrences of '%' string separator  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
{
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
}
 
LoadString(hInst, IDS_DEFEXTSTRING, 
     (LPSTR)szDefExt, sizeof(szFilter)); 
 
 
// Use the OpenFilename common dialog box  
// to obtain the desired filename.  

szFile[0] = '\0'; 
OPENFILENAME Ofn; 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrCustomFilter = (LPSTR)NULL; 
Ofn.nMaxCustFilter = 0L; 
Ofn.nFilterIndex = 1L; 
Ofn.lpstrFile = szFile; 
Ofn.nMaxFile = sizeof(szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR) NULL; 
Ofn.lpstrTitle = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST; 
Ofn.nFileOffset = 0; 
Ofn.nFileExtension = 0; 
Ofn.lpstrDefExt = szDefExt; 
 
GetOpenFileName(&Ofn); 
 
// Open the metafile.  
 
HENHMETAFILE hemf = GetEnhMetaFile(Ofn.lpstrFile); 
 
// Retrieve a handle to a window device context.  
 
HDC hDC = GetDC(hWnd); 
 
// Retrieve the client rectangle dimensions.  
 
GetClientRect(hWnd, &rct); 
 
// Draw the picture.  
 
PlayEnhMetaFile(hDC, hemf, &rct); 
 
// Release the metafile handle.  
 
DeleteEnhMetaFile(hemf); 
 
// Release the window DC.  
 
ReleaseDC(hWnd, hDC); 
```



 

 



