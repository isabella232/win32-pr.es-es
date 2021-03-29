---
title: Cómo implementar la información sobre herramientas de varias líneas
description: La información sobre herramientas multilínea permite que el texto se muestre en más de una línea.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774197"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="3fab2-103">Cómo implementar la información sobre herramientas de varias líneas</span><span class="sxs-lookup"><span data-stu-id="3fab2-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="3fab2-104">La información sobre herramientas multilínea permite que el texto se muestre en más de una línea.</span><span class="sxs-lookup"><span data-stu-id="3fab2-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="3fab2-105">Son compatibles con la [versión 4,70](common-control-versions.md) y versiones posteriores de los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="3fab2-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="3fab2-106">La aplicación crea una información sobre herramientas de varias líneas mediante el envío de un mensaje de [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , que especifica el ancho del rectángulo de presentación.</span><span class="sxs-lookup"><span data-stu-id="3fab2-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="3fab2-107">El texto que supera este ancho se ajusta a la línea siguiente en lugar de ensanchar la región de presentación.</span><span class="sxs-lookup"><span data-stu-id="3fab2-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="3fab2-108">El alto del rectángulo aumenta según sea necesario para dar cabida a las líneas adicionales.</span><span class="sxs-lookup"><span data-stu-id="3fab2-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="3fab2-109">El control ToolTip ajusta las líneas automáticamente, o puede utilizar una combinación de retorno de carro/avance de línea, \\ r \\ n, para forzar saltos de línea en ubicaciones concretas.</span><span class="sxs-lookup"><span data-stu-id="3fab2-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="3fab2-110">La presentación resultante se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="3fab2-110">The resulting display is shown in the following illustration.</span></span>

![captura de pantalla de un cuadro de diálogo con información sobre herramientas que contiene texto organizado como un párrafo de varias líneas](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="3fab2-112">El búfer de texto especificado por el miembro **szText** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) solo puede contener 80 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3fab2-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="3fab2-113">Si necesita usar una cadena más larga, apunte el miembro **lpszText** de **NMTTDISPINFO** a un búfer que contenga el texto deseado.</span><span class="sxs-lookup"><span data-stu-id="3fab2-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="3fab2-114">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="3fab2-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3fab2-115">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="3fab2-115">Technologies</span></span>

-   [<span data-ttu-id="3fab2-116">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="3fab2-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3fab2-117">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3fab2-117">Prerequisites</span></span>

-   <span data-ttu-id="3fab2-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="3fab2-118">C/C++</span></span>
-   <span data-ttu-id="3fab2-119">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="3fab2-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3fab2-120">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="3fab2-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="3fab2-121">Implementar información sobre herramientas de varias líneas</span><span class="sxs-lookup"><span data-stu-id="3fab2-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="3fab2-122">El siguiente fragmento de código es un ejemplo de un controlador de notificación simple de [TTN \_ GETDISPINFO](ttn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="3fab2-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="3fab2-123">Habilita una información sobre herramientas de varias líneas estableciendo el rectángulo de presentación en 150 píxeles.</span><span class="sxs-lookup"><span data-stu-id="3fab2-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="3fab2-124">Se inserta un salto de línea manual después de la primera palabra para mostrar que los saltos de línea pueden ser difíciles y flexibles.</span><span class="sxs-lookup"><span data-stu-id="3fab2-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="3fab2-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fab2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fab2-126">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="3fab2-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




