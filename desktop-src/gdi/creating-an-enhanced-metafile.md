---
description: Esta sección contiene un ejemplo que muestra la creación de un metarchivo mejorado que se almacena en un disco, con un nombre de archivo especificado por el usuario.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Creación de un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e53266ac0677da211308c7028f4d61869fc2890f27c06daeff9cfb6fea87e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849235"
---
# <a name="creating-an-enhanced-metafile"></a>Creación de un metarchivo mejorado

Esta sección contiene un ejemplo que muestra la creación de un metarchivo mejorado que se almacena en un disco, con un nombre de archivo especificado por el usuario.

En el ejemplo se usa un contexto de dispositivo para la ventana de aplicación como contexto de dispositivo de referencia. (El sistema almacena los datos de resolución de este dispositivo en el encabezado del metarchivo mejorado). La aplicación recupera un identificador que identifica este contexto de dispositivo mediante una llamada a la [**función GetDC.**](/windows/desktop/api/Winuser/nf-winuser-getdc)

En el ejemplo se usan las dimensiones del área cliente de la aplicación para definir las dimensiones del marco de imagen. Con las dimensiones de rectángulo devueltas por la función [**GetClientRect,**](/windows/win32/api/winuser/nf-winuser-getclientrect) la aplicación convierte las unidades de dispositivo en unidades de 01 milímetros y pasa los valores convertidos a la función [**CreateEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)

En el ejemplo se muestra **un cuadro** de diálogo Guardar como común que permite al usuario especificar el nombre de archivo del nuevo metarchivo mejorado. El sistema anexa la extensión .emf de tres caracteres a este nombre de archivo y pasa el nombre a la [**función CreateEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)

En el ejemplo también se inserta una descripción de texto de la imagen en el encabezado de metarchivo mejorado. Esta descripción se especifica como un recurso en la tabla de cadenas del archivo de recursos de la aplicación. Sin embargo, en una aplicación en funcionamiento, esta cadena se recuperaría de un control personalizado en un cuadro de diálogo común o de un cuadro de diálogo independiente mostrado únicamente para este propósito.


```C++
// Obtain a handle to a reference device context.  
 
hdcRef = GetDC(hWnd); 
 
// Determine the picture frame dimensions.  
// iWidthMM is the display width in millimeters.  
// iHeightMM is the display height in millimeters.  
// iWidthPels is the display width in pixels.  
// iHeightPels is the display height in pixels  
 
iWidthMM = GetDeviceCaps(hdcRef, HORZSIZE); 
iHeightMM = GetDeviceCaps(hdcRef, VERTSIZE); 
iWidthPels = GetDeviceCaps(hdcRef, HORZRES); 
iHeightPels = GetDeviceCaps(hdcRef, VERTRES); 
 
// Retrieve the coordinates of the client  
// rectangle, in pixels.  
 
GetClientRect(hWnd, &rect); 
 
// Convert client coordinates to .01-mm units.  
// Use iWidthMM, iWidthPels, iHeightMM, and  
// iHeightPels to determine the number of  
// .01-millimeter units per pixel in the x-  
//  and y-directions.  
 
rect.left = (rect.left * iWidthMM * 100)/iWidthPels; 
rect.top = (rect.top * iHeightMM * 100)/iHeightPels; 
rect.right = (rect.right * iWidthMM * 100)/iWidthPels; 
rect.bottom = (rect.bottom * iHeightMM * 100)/iHeightPels; 
 
// Load the filename filter from the string table.  
 
LoadString(hInst, IDS_FILTERSTRING, 
     (LPSTR)szFilter, sizeof(szFilter)); 
 
// Replace the '%' separators that are embedded  
// between the strings in the string-table entry  
// with '\0'.  
 
for (i=0; szFilter[i]!='\0'; i++) 
    if (szFilter[i] == '%') 
            szFilter[i] = '\0'; 
 
// Load the dialog title string from the table.  
 
LoadString(hInst, IDS_TITLESTRING, 
     (LPSTR)szTitle, sizeof(szTitle)); 
 
// Initialize the OPENFILENAME members.  
 
szFile[0] = '\0'; 
 
Ofn.lStructSize = sizeof(OPENFILENAME); 
Ofn.hwndOwner = hWnd; 
Ofn.lpstrFilter = szFilter; 
Ofn.lpstrFile= szFile; 
Ofn.nMaxFile = sizeof(szFile)/ sizeof(*szFile); 
Ofn.lpstrFileTitle = szFileTitle; 
Ofn.nMaxFileTitle = sizeof(szFileTitle); 
Ofn.lpstrInitialDir = (LPSTR)NULL; 
Ofn.Flags = OFN_SHOWHELP | OFN_OVERWRITEPROMPT; 
Ofn.lpstrTitle = szTitle; 
 
// Display the Filename common dialog box. The  
// filename specified by the user is passed  
// to the CreateEnhMetaFile function and used to  
// store the metafile on disk.  
 
GetSaveFileName(&Ofn); 
 
// Load the description from the string table.  
 
LoadString(hInst, IDS_DESCRIPTIONSTRING, 
     (LPSTR)szDescription, sizeof(szDescription)); 
 
// Replace the '%' string separators that are  
// embedded between strings in the string-table  
// entry with '\0'.  
 
for (i=0; szDescription[i]!='\0'; i++) 
{
    if (szDescription[i] == '%') 
            szDescription[i] = '\0'; 
}
 
// Create the metafile device context.  
 
hdcMeta = CreateEnhMetaFile(hdcRef, 
          (LPTSTR) Ofn.lpstrFile, 
          &rect, (LPSTR)szDescription); 
 
if (!hdcMeta) 
    errhandler("CreateEnhMetaFile", hWnd); 
 
// Release the reference device context.  
 
ReleaseDC(hWnd, hdcRef); 
```



 

 
