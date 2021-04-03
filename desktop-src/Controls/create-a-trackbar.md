---
title: Cómo crear un TrackBar
description: Cuando se crea la barra de inicio, se inicializan su intervalo y su intervalo de selección. También se establece el tamaño de página en este momento.
ms.assetid: FA110B4A-D3D7-49D8-A3DC-368099F6DA1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9468ff044b94837f54d04cda4a9105f15410692
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075298"
---
# <a name="how-to-create-a-trackbar"></a><span data-ttu-id="01d81-104">Cómo crear un TrackBar</span><span class="sxs-lookup"><span data-stu-id="01d81-104">How to Create a Trackbar</span></span>

<span data-ttu-id="01d81-105">Cuando se crea la barra de inicio, se inicializan su intervalo y su intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="01d81-105">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="01d81-106">También se establece el tamaño de página en este momento.</span><span class="sxs-lookup"><span data-stu-id="01d81-106">The page size is also set at this time.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="01d81-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="01d81-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="01d81-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="01d81-108">Technologies</span></span>

-   [<span data-ttu-id="01d81-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="01d81-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="01d81-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01d81-110">Prerequisites</span></span>

-   <span data-ttu-id="01d81-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="01d81-111">C/C++</span></span>
-   <span data-ttu-id="01d81-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="01d81-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="01d81-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="01d81-113">Instructions</span></span>

### <a name="create-a-trackbar"></a><span data-ttu-id="01d81-114">Crear un TrackBar</span><span class="sxs-lookup"><span data-stu-id="01d81-114">Create a Trackbar</span></span>

<span data-ttu-id="01d81-115">En el ejemplo siguiente se muestra cómo crear una barra de aumento con los estilos [**TBS \_ autoticks**](trackbar-control-styles.md) y [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="01d81-115">The following example shows how to create a trackbar with the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) and [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) styles.</span></span>


```
// CreateTrackbar - creates and initializes a trackbar. 
// 
// Global variable
//     g_hinst - instance handle
//
HWND WINAPI CreateTrackbar( 
    HWND hwndDlg,  // handle of dialog box (parent window) 
    UINT iMin,     // minimum value in trackbar range 
    UINT iMax,     // maximum value in trackbar range 
    UINT iSelMin,  // minimum value in trackbar selection 
    UINT iSelMax)  // maximum value in trackbar selection 
{ 

    InitCommonControls(); // loads common control's DLL 

    hwndTrack = CreateWindowEx( 
        0,                               // no extended styles 
        TRACKBAR_CLASS,                  // class name 
        "Trackbar Control",              // title (caption) 
        WS_CHILD | 
        WS_VISIBLE | 
        TBS_AUTOTICKS | 
        TBS_ENABLESELRANGE,              // style 
        10, 10,                          // position 
        200, 30,                         // size 
        hwndDlg,                         // parent window 
        ID_TRACKBAR,                     // control identifier 
        g_hinst,                         // instance 
        NULL                             // no WM_CREATE parameter 
        ); 

    SendMessage(hwndTrack, TBM_SETRANGE, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) MAKELONG(iMin, iMax));  // min. & max. positions
        
    SendMessage(hwndTrack, TBM_SETPAGESIZE, 
        0, (LPARAM) 4);                  // new page size 

    SendMessage(hwndTrack, TBM_SETSEL, 
        (WPARAM) FALSE,                  // redraw flag 
        (LPARAM) MAKELONG(iSelMin, iSelMax)); 
        
    SendMessage(hwndTrack, TBM_SETPOS, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) iSelMin); 

    SetFocus(hwndTrack); 

    return hwndTrack; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="01d81-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01d81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d81-117">Usar controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="01d81-117">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




