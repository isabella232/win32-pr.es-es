---
description: Esta sección contiene un ejemplo que muestra cómo una aplicación abre un metarchivo mejorado almacenado en disco y muestra la imagen asociada en el área de cliente.
ms.assetid: e4e5ef5c-d5ea-4931-bbec-1635e8f08c91
title: Abrir un metarchivo mejorado y mostrar su contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb51d9b1d2117f5b47445b3026b9651fa29d656715dc03a1892881b4fd32f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698707"
---
# <a name="opening-an-enhanced-metafile-and-displaying-its-contents"></a>Abrir un metarchivo mejorado y mostrar su contenido

Esta sección contiene un ejemplo que muestra cómo una aplicación abre un metarchivo mejorado almacenado en disco y muestra la imagen asociada en el área de cliente.

En el ejemplo se usa **el cuadro** de diálogo Abrir común para permitir al usuario seleccionar un metarchivo mejorado de una lista de archivos existentes. A continuación, pasa el nombre del archivo seleccionado a la función [**GetEnhMetaFile,**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea) que devuelve un identificador que identifica el archivo. Este identificador se pasa a la [**función PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) para mostrar la imagen.


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



 

 



