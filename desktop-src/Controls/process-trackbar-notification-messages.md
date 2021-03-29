---
title: Cómo procesar mensajes de notificación de TrackBar
description: Trackbars notifique a su ventana primaria de las acciones del usuario mediante el envío de un mensaje primario a WM \_ HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774544"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="ae8e1-103">Cómo procesar mensajes de notificación de TrackBar</span><span class="sxs-lookup"><span data-stu-id="ae8e1-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="ae8e1-104">Trackbars notifique a su ventana primaria de las acciones del usuario mediante el envío de un mensaje primario a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8e1-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ae8e1-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ae8e1-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ae8e1-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ae8e1-106">Technologies</span></span>

-   [<span data-ttu-id="ae8e1-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ae8e1-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ae8e1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae8e1-108">Prerequisites</span></span>

-   <span data-ttu-id="ae8e1-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ae8e1-109">C/C++</span></span>
-   <span data-ttu-id="ae8e1-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ae8e1-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ae8e1-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ae8e1-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="ae8e1-112">Procesar mensajes de notificación de TrackBar</span><span class="sxs-lookup"><span data-stu-id="ae8e1-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="ae8e1-113">El siguiente ejemplo de código es una función a la que se llama cuando la ventana primaria de la barra de control recibe un mensaje de [**\_ HSCROLL de WM**](wm-hscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8e1-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="ae8e1-114">La barra de error de este ejemplo tiene el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8e1-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="ae8e1-115">La posición del control deslizante se compara con el intervalo de selección, y el control deslizante se mueve a la posición inicial o final del intervalo de selección cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ae8e1-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="ae8e1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae8e1-116">Remarks</span></span>

<span data-ttu-id="ae8e1-117">Un cuadro de diálogo que contiene una barra de propiedades de estilo [**TBS \_ Vert**](trackbar-control-styles.md) puede utilizar esta función cuando recibe un mensaje de [**\_ VSCROLL de WM**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="ae8e1-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae8e1-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae8e1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae8e1-119">Usar controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="ae8e1-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




