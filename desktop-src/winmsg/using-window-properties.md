---
description: En esta sección se explica cómo realizar las siguientes tareas asociadas a las propiedades de la ventana.
ms.assetid: cdf196ec-300c-4c7b-8a4f-68088c4a2507
title: Usar las propiedades de la ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 736682eb34191a061aa9753ef9d5e8c7e366fbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716068"
---
# <a name="using-window-properties"></a><span data-ttu-id="447d4-103">Usar las propiedades de la ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-103">Using Window Properties</span></span>

<span data-ttu-id="447d4-104">En esta sección se explica cómo realizar las siguientes tareas asociadas a las propiedades de la ventana.</span><span class="sxs-lookup"><span data-stu-id="447d4-104">This section explains how to perform the following tasks associated with window properties.</span></span>

-   [<span data-ttu-id="447d4-105">Agregar una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-105">Adding a Window Property</span></span>](#adding-a-window-property)
-   [<span data-ttu-id="447d4-106">Recuperación de una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-106">Retrieving a Window Property</span></span>](#retrieving-a-window-property)
-   [<span data-ttu-id="447d4-107">Enumerar las propiedades de la ventana de una ventana determinada</span><span class="sxs-lookup"><span data-stu-id="447d4-107">Listing Window Properties for a Given Window</span></span>](#listing-window-properties-for-a-given-window)
-   [<span data-ttu-id="447d4-108">Eliminar una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-108">Deleting a Window Property</span></span>](#deleting-a-window-property)

## <a name="adding-a-window-property"></a><span data-ttu-id="447d4-109">Agregar una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-109">Adding a Window Property</span></span>

<span data-ttu-id="447d4-110">En el ejemplo siguiente se carga un icono y después un cursor y se asigna memoria para un búfer.</span><span class="sxs-lookup"><span data-stu-id="447d4-110">The following example loads an icon and then a cursor and allocates memory for a buffer.</span></span> <span data-ttu-id="447d4-111">A continuación, en el ejemplo se usa la función [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) para asignar el icono, el cursor y los identificadores de memoria resultantes como propiedades de ventana para la ventana identificada por la variable hwndSubclass definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="447d4-111">The example then uses the [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) function to assign the resulting icon, cursor, and memory handles as window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="447d4-112">Las propiedades se identifican mediante el icono PROP de las cadenas \_ , el \_ cursor de propiedades y el búfer de propiedades \_ .</span><span class="sxs-lookup"><span data-stu-id="447d4-112">The properties are identified by the strings PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span>


```
#define BUFFER 4096 
 
HINSTANCE hinst;       // handle of current instance 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIcon, hCursor; 
HGLOBAL hMem; 
char *lpMem; 
TCHAR tchPath[] = "c:\\winnt\\samples\\winprop.c";
HRESULT hResult; 
 
// Load resources. 
 
hIcon = LoadIcon(hinst, MAKEINTRESOURCE(400)); 
hCursor = LoadCursor(hinst, MAKEINTRESOURCE(220)); 
 
// Allocate and fill a memory buffer. 
 
hMem = GlobalAlloc(GPTR, BUFFER); 
lpMem = GlobalLock(hMem);
if (lpMem == NULL)
{
// TODO: write error handler
}
hResult = StringCchCopy(lpMem, STRSAFE_MAX_CCH, tchPath);
if (FAILED(hResult))
{
// TO DO: write error handler if function fails.
} 
GlobalUnlock(hMem); 
 
// Set the window properties for hwndSubclass. 
 
SetProp(hwndSubclass, "PROP_ICON", hIcon); 
SetProp(hwndSubclass, "PROP_CURSOR", hCursor); 
SetProp(hwndSubclass, "PROP_BUFFER", hMem); 
```



## <a name="retrieving-a-window-property"></a><span data-ttu-id="447d4-113">Recuperación de una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-113">Retrieving a Window Property</span></span>

<span data-ttu-id="447d4-114">Una ventana puede crear identificadores para sus datos de propiedades de ventana y usar los datos para cualquier propósito.</span><span class="sxs-lookup"><span data-stu-id="447d4-114">A window can create handles to its window property data and use the data for any purpose.</span></span> <span data-ttu-id="447d4-115">En el ejemplo siguiente se usa [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) para obtener los identificadores de las propiedades de ventana identificadas por el icono de prop \_ , el cursor de propiedades y el búfer de \_ propiedades \_ .</span><span class="sxs-lookup"><span data-stu-id="447d4-115">The following example uses [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) to obtain handles to the window properties identified by PROP\_ICON, PROP\_CURSOR, and PROP\_BUFFER.</span></span> <span data-ttu-id="447d4-116">A continuación, en el ejemplo se muestra el contenido del búfer de memoria, el cursor y el icono recién obtenidos en el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="447d4-116">The example then displays the contents of the newly obtained memory buffer, cursor, and icon in the window's client area.</span></span>


```
#define PATHLENGTH 256 
 
HWND hwndSubclass;     // handle of a subclassed window 
HANDLE hIconProp, hCursProp; 
HGLOBAL hMemProp; 
char *lpFilename; 
TCHAR tchBuffer[PATHLENGTH]; 
size_t * nSize; 
HDC hdc;
HRESULT hResult; 
 
// Get the window properties, then use the data. 
 
hIconProp = (HICON) GetProp(hwndSubclass, "PROP_ICON"); 
TextOut(hdc, 10, 40, "PROP_ICON", 9); 
DrawIcon(hdc, 90, 40, hIconProp); 
 
hCursProp = (HCURSOR) GetProp(hwndSubclass, "PROP_CURSOR"); 
TextOut(hdc, 10, 85, "PROP_CURSOR", 9); 
DrawIcon(hdc, 110, 85, hCursProp); 
 
hMemProp = (HGLOBAL) GetProp(hwndSubclass, "PROP_BUFFER"); 
lpFilename = GlobalLock(hMemProp);
hResult = StringCchPrintf(tchBuffer, PATHLENGTH, 
    "Path to file:  %s", lpFilename);
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
hResult = StringCchLength(tchBuffer, PATHLENGTH, nSize)
if (FAILED(hResult))
{
// TODO: write error handler if function fails.
}
TextOut(hdc, 10, 10, tchBuffer, *nSize); 
```



## <a name="listing-window-properties-for-a-given-window"></a><span data-ttu-id="447d4-117">Enumerar las propiedades de la ventana de una ventana determinada</span><span class="sxs-lookup"><span data-stu-id="447d4-117">Listing Window Properties for a Given Window</span></span>

<span data-ttu-id="447d4-118">En el ejemplo siguiente, la función [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enumera los identificadores de cadena de las propiedades de ventana de la ventana identificada por la variable hwndSubclass definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="447d4-118">In the following example, the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function lists the string identifiers of the window properties for the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="447d4-119">Esta función se basa en la función de devolución de llamada definida por la aplicación WinPropProc para mostrar las cadenas en el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="447d4-119">This function relies on the application-defined callback function WinPropProc to display the strings in the window's client area.</span></span>


```
EnumPropsEx(hwndSubclass, WinPropProc, NULL); 
 
// WinPropProc is an application-defined callback function 
// that lists a window property. 
 
BOOL CALLBACK WinPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    static int nProp = 1;    // property counter 
    TCHAR tchBuffer[BUFFER]; // expanded-string buffer 
    size_t * nSize;          // size of string in buffer 
    HDC hdc;                 // device-context handle
    HRESULT hResult; 
 
    hdc = GetDC(hwndSubclass); 
 
    // Display window property string in client area.
    hResult = StringCchPrintf(tchBuffer, BUFFER, "WinProp %d:  %s", nProp++, lpszString);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    }
    hResult = StringCchLength(tchBuffer, BUFFER, nSize);
    if (FAILED(hResult))
    {
    // TO DO: write error handler if function fails.
    } 
    TextOut(hdc, 10, nProp * 20, tchBuffer, *nSize); 
 
    ReleaseDC(hwndSubclass, hdc); 
 
    return TRUE; 
} 
```



## <a name="deleting-a-window-property"></a><span data-ttu-id="447d4-120">Eliminar una propiedad de ventana</span><span class="sxs-lookup"><span data-stu-id="447d4-120">Deleting a Window Property</span></span>

<span data-ttu-id="447d4-121">Cuando se destruye una ventana, debe destruir las propiedades de ventana que establezca.</span><span class="sxs-lookup"><span data-stu-id="447d4-121">When a window is destroyed, it must destroy any window properties it set.</span></span> <span data-ttu-id="447d4-122">En el ejemplo siguiente se usa la función [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) y la función de devolución de llamada definida por la aplicación DelPropProc para destruir las propiedades asociadas a la ventana identificada por la variable hwndSubclass definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="447d4-122">The following example uses the [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) function and the application-defined callback function DelPropProc to destroy the properties associated with the window identified by the application-defined hwndSubclass variable.</span></span> <span data-ttu-id="447d4-123">También se muestra la función de devolución de llamada, que utiliza la función [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) .</span><span class="sxs-lookup"><span data-stu-id="447d4-123">The callback function, which uses the [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) function, is also shown.</span></span>


```
case WM_DESTROY: 
 
    EnumPropsEx(hwndSubclass, DelPropProc, NULL); 
 
    PostQuitMessage(0); 
    break; 
 
// DelPropProc is an application-defined callback function 
// that deletes a window property. 
 
BOOL CALLBACK DelPropProc( 
    HWND hwndSubclass,  // handle of window with property 
    LPCSTR lpszString,  // property string or atom 
    HANDLE hData)       // data handle 
{ 
    hData = RemoveProp(hwndSubclass, lpszString); 
//
// if appropriate, free the handle hData
//
 
    return TRUE; 
}
```



 

 
