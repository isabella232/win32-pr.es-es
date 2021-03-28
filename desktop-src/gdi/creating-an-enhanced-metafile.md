---
description: Esta sección contiene un ejemplo en el que se muestra la creación de un metarchivo mejorado que se almacena en un disco con un nombre de archivo especificado por el usuario.
ms.assetid: 084b2737-eb55-4587-b8e8-3eb3fa3688c4
title: Crear un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4877481ed0a68d6379e7eaabb00bbe37cef74c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544539"
---
# <a name="creating-an-enhanced-metafile"></a><span data-ttu-id="38df9-103">Crear un metarchivo mejorado</span><span class="sxs-lookup"><span data-stu-id="38df9-103">Creating an Enhanced Metafile</span></span>

<span data-ttu-id="38df9-104">Esta sección contiene un ejemplo en el que se muestra la creación de un metarchivo mejorado que se almacena en un disco con un nombre de archivo especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="38df9-104">This section contains an example that demonstrates the creation of an enhanced metafile that is stored on a disk, using a file name specified by the user.</span></span>

<span data-ttu-id="38df9-105">En el ejemplo se usa un contexto de dispositivo para la ventana de la aplicación como contexto de dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="38df9-105">The example uses a device context for the application window as the reference device context.</span></span> <span data-ttu-id="38df9-106">(El sistema almacena los datos de resolución de este dispositivo en el encabezado del metarchivo mejorado). La aplicación recupera un identificador que identifica este contexto de dispositivo mediante una llamada a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="38df9-106">(The system stores the resolution data for this device in the enhanced-metafile's header.) The application retrieves a handle identifying this device context by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="38df9-107">En el ejemplo se utilizan las dimensiones del área cliente de la aplicación para definir las dimensiones del marco de imagen.</span><span class="sxs-lookup"><span data-stu-id="38df9-107">The example uses the dimensions of the application's client area to define the dimensions of the picture frame.</span></span> <span data-ttu-id="38df9-108">Con las dimensiones de rectángulo devueltas por la función [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) , la aplicación convierte las unidades de dispositivo en unidades .01-milímetros y pasa los valores convertidos a la función [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="38df9-108">Using the rectangle dimensions returned by the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function, the application converts the device units to .01-millimeter units and passes the converted values to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="38df9-109">En el ejemplo se muestra un cuadro de diálogo **Guardar como** común que permite al usuario especificar el nombre de archivo del nuevo metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="38df9-109">The example displays a **Save As** common dialog box that enables the user to specify the file name of the new enhanced metafile.</span></span> <span data-ttu-id="38df9-110">El sistema anexa la extensión. EMF de tres caracteres a este nombre de archivo y pasa el nombre a la función [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) .</span><span class="sxs-lookup"><span data-stu-id="38df9-110">The system appends the three-character .emf extension to this file name and passes the name to the [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) function.</span></span>

<span data-ttu-id="38df9-111">En el ejemplo también se incrusta una descripción de texto de la imagen en el encabezado Enhanced-Metafile.</span><span class="sxs-lookup"><span data-stu-id="38df9-111">The example also embeds a text description of the picture in the enhanced-metafile header.</span></span> <span data-ttu-id="38df9-112">Esta descripción se especifica como un recurso en la tabla de cadenas del archivo de recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38df9-112">This description is specified as a resource in the string table of the application's resource file.</span></span> <span data-ttu-id="38df9-113">Sin embargo, en una aplicación de trabajo, esta cadena se recuperaría de un control personalizado en un cuadro de diálogo común o de un cuadro de diálogo independiente mostrado únicamente para este propósito.</span><span class="sxs-lookup"><span data-stu-id="38df9-113">However, in a working application, this string would be retrieved from a custom control in a common dialog box or from a separate dialog box displayed solely for this purpose.</span></span>


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



 

 
