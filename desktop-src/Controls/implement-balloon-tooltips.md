---
title: Cómo implementar la información sobre herramientas de globo
description: La información sobre herramientas de globos es similar a la información sobre herramientas estándar, pero se muestra en un globo 0034 de estilo animado \ 0034; con una tallo que apunta a la herramienta.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774203"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="63aa9-103">Cómo implementar la información sobre herramientas de globo</span><span class="sxs-lookup"><span data-stu-id="63aa9-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="63aa9-104">La información sobre herramientas de globo es similar a la información sobre herramientas estándar, pero se muestra en un "globo" de estilo animado con una tallo que apunta a la herramienta.</span><span class="sxs-lookup"><span data-stu-id="63aa9-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="63aa9-105">La información sobre herramientas de globo puede ser de una o varias líneas.</span><span class="sxs-lookup"><span data-stu-id="63aa9-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="63aa9-106">Se crean y se administran de forma muy similar a la información sobre herramientas estándar.</span><span class="sxs-lookup"><span data-stu-id="63aa9-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="63aa9-107">En la ilustración siguiente se muestra la posición predeterminada de la tallo y el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="63aa9-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="63aa9-108">Si la herramienta está demasiado cerca de la parte superior de la pantalla, la información sobre herramientas aparece debajo y a la derecha del rectángulo de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="63aa9-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="63aa9-109">Si la herramienta está demasiado cerca del lado derecho de la pantalla, se aplican principios similares, pero la información sobre herramientas aparece a la izquierda del rectángulo de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="63aa9-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas de globo con una línea de texto aparece encima y a la derecha del destino.](images/tt-balloon.png)

<span data-ttu-id="63aa9-111">Puede cambiar la posición predeterminada estableciendo la marca **ttf \_ CENTERTIP** en el miembro **UFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="63aa9-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="63aa9-112">En ese caso, el tallo normalmente apunta al centro del borde inferior del rectángulo de la herramienta y el rectángulo de texto se muestra directamente debajo de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="63aa9-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="63aa9-113">El tallo se adjunta al rectángulo de texto en el centro del borde superior.</span><span class="sxs-lookup"><span data-stu-id="63aa9-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="63aa9-114">Si la herramienta está demasiado cerca de la parte inferior de la pantalla, el rectángulo de texto se centra encima de la herramienta y el tallo se adjunta al centro del borde inferior.</span><span class="sxs-lookup"><span data-stu-id="63aa9-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="63aa9-115">En la ilustración siguiente se muestra una información sobre herramientas que está centrada en la herramienta.</span><span class="sxs-lookup"><span data-stu-id="63aa9-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas de globo con una línea de texto aparece centrada debajo del destino](images/tt-ballooncenter.png)

<span data-ttu-id="63aa9-117">Si desea especificar dónde están los puntos de tallo, establezca la marca de **\_ seguimiento ttf** en el miembro **uFlags** de la estructura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="63aa9-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="63aa9-118">A continuación, especifique la coordenada mediante el envío de un mensaje [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) , con las coordenadas x e y en el valor *lParam* .</span><span class="sxs-lookup"><span data-stu-id="63aa9-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="63aa9-119">Si también se establece **ttf \_ CENTERTIP** , el tallo sigue señalando a la posición especificada por el mensaje **TTM \_ TRACKPOSITION** .</span><span class="sxs-lookup"><span data-stu-id="63aa9-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="63aa9-120">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="63aa9-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="63aa9-121">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="63aa9-121">Technologies</span></span>

-   [<span data-ttu-id="63aa9-122">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="63aa9-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="63aa9-123">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63aa9-123">Prerequisites</span></span>

-   <span data-ttu-id="63aa9-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="63aa9-124">C/C++</span></span>
-   <span data-ttu-id="63aa9-125">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="63aa9-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="63aa9-126">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="63aa9-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="63aa9-127">Implementar la información sobre herramientas de globo</span><span class="sxs-lookup"><span data-stu-id="63aa9-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="63aa9-128">En el ejemplo de código siguiente se muestra cómo implementar una información sobre herramientas de globo centrado mediante el estilo de control ToolTip **\_ Balloon** ToolTip.</span><span class="sxs-lookup"><span data-stu-id="63aa9-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="63aa9-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63aa9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63aa9-130">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="63aa9-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="63aa9-131">**Estilos de información sobre herramientas**</span><span class="sxs-lookup"><span data-stu-id="63aa9-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




