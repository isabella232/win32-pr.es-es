---
title: Cómo limitar el movimiento del control deslizante
description: Tal y como se describe en acerca de los controles TrackBar, es posible establecer una parte del intervalo de la barra de control como un intervalo de selección. Un propósito de un intervalo de selección puede ser limitar el movimiento del control deslizante, haciendo que algunas partes de los límites del intervalo completo estén desactivadas.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903255"
---
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="61c26-104">Cómo limitar el movimiento del control deslizante</span><span class="sxs-lookup"><span data-stu-id="61c26-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="61c26-105">Tal y como se describe en [acerca de los controles TrackBar](trackbar-controls.md), es posible establecer una parte del intervalo de la barra de control como un intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="61c26-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="61c26-106">Un propósito de un intervalo de selección puede ser limitar el movimiento del control deslizante, haciendo que algunas partes de los límites del intervalo completo estén desactivadas.</span><span class="sxs-lookup"><span data-stu-id="61c26-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61c26-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="61c26-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61c26-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="61c26-108">Technologies</span></span>

-   [<span data-ttu-id="61c26-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="61c26-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="61c26-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="61c26-110">Prerequisites</span></span>

-   <span data-ttu-id="61c26-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="61c26-111">C/C++</span></span>
-   <span data-ttu-id="61c26-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="61c26-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="61c26-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="61c26-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="61c26-114">Límite de movimiento del control deslizante</span><span class="sxs-lookup"><span data-stu-id="61c26-114">Limit Slider Movement</span></span>

<span data-ttu-id="61c26-115">En el siguiente código de ejemplo se limita el movimiento del control deslizante restableciendo la posición del control deslizante cada vez que se mueve fuera del intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="61c26-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a><span data-ttu-id="61c26-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61c26-116">Remarks</span></span>

<span data-ttu-id="61c26-117">Este fragmento de código formaría parte del procedimiento de ventana de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="61c26-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61c26-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61c26-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c26-119">Usar controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="61c26-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




