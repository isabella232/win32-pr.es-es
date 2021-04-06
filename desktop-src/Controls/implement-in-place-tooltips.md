---
title: Cómo implementar In-Place información sobre herramientas
description: La información sobre herramientas en contexto se usa para mostrar las cadenas de texto de los objetos que se han recortado. Para ver una ilustración, consulte Acerca de los controles de información sobre herramientas.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078630"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="740fd-104">Cómo implementar In-Place información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="740fd-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="740fd-105">La información sobre herramientas en contexto se usa para mostrar las cadenas de texto de los objetos que se han recortado.</span><span class="sxs-lookup"><span data-stu-id="740fd-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="740fd-106">Para ver una ilustración, consulte [acerca de los controles de información sobre herramientas](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="740fd-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="740fd-107">La diferencia entre la información sobre herramientas normal y en contexto es el posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="740fd-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="740fd-108">De forma predeterminada, cuando el puntero del mouse se mantiene sobre una región que tiene una información sobre herramientas asociada, la información sobre herramientas se muestra junto a la región.</span><span class="sxs-lookup"><span data-stu-id="740fd-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="740fd-109">Sin embargo, la información sobre herramientas es Windows y se pueden colocar en cualquier lugar que elija llamando a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="740fd-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="740fd-110">Crear una información sobre herramientas en contexto es cuestión de colocar la ventana de información sobre herramientas para que se superponga la cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="740fd-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="740fd-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="740fd-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="740fd-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="740fd-112">Technologies</span></span>

-   [<span data-ttu-id="740fd-113">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="740fd-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="740fd-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="740fd-114">Prerequisites</span></span>

-   <span data-ttu-id="740fd-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="740fd-115">C/C++</span></span>
-   <span data-ttu-id="740fd-116">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="740fd-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="740fd-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="740fd-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="740fd-118">Colocar una In-Place información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="740fd-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="740fd-119">Debe realizar un seguimiento de tres rectángulos al colocar una información sobre herramientas en contexto:</span><span class="sxs-lookup"><span data-stu-id="740fd-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="740fd-120">Rectángulo que rodea el texto de etiqueta completo.</span><span class="sxs-lookup"><span data-stu-id="740fd-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="740fd-121">Rectángulo que rodea el texto de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="740fd-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="740fd-122">El texto de la información sobre herramientas es idéntico al texto completo de la etiqueta y, normalmente, tiene el mismo tamaño y fuente.</span><span class="sxs-lookup"><span data-stu-id="740fd-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="740fd-123">Los dos rectángulos de texto suelen tener el mismo tamaño.</span><span class="sxs-lookup"><span data-stu-id="740fd-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="740fd-124">Rectángulo de la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="740fd-124">The tooltip window rectangle.</span></span> <span data-ttu-id="740fd-125">Este rectángulo es algo más grande que el rectángulo de texto de información sobre herramientas que se incluye.</span><span class="sxs-lookup"><span data-stu-id="740fd-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="740fd-126">Los tres rectángulos se muestran esquemáticamente en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="740fd-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="740fd-127">La parte oculta del texto de la etiqueta se indica con un fondo gris.</span><span class="sxs-lookup"><span data-stu-id="740fd-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![diagrama que muestra una cadena larga, la mitad de la cual tiene un fondo gris y, a continuación, la misma cadena dentro de un rectángulo más grande de la ventana de información sobre herramientas](images/inplace.png)

<span data-ttu-id="740fd-129">Para crear una información sobre herramientas en contexto, debe colocar el rectángulo de texto de información sobre herramientas para que se superponga el rectángulo de texto de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="740fd-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="740fd-130">El procedimiento para alinear los dos rectángulos es relativamente sencillo:</span><span class="sxs-lookup"><span data-stu-id="740fd-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="740fd-131">Defina el rectángulo de texto de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="740fd-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="740fd-132">Coloca la ventana de información sobre herramientas para que el rectángulo del texto de información sobre herramientas se superponga al rectángulo de texto de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="740fd-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="740fd-133">En la práctica, normalmente es suficiente para alinear la esquina superior izquierda de los dos rectángulos de texto.</span><span class="sxs-lookup"><span data-stu-id="740fd-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="740fd-134">Si intenta cambiar el tamaño del rectángulo de texto de información sobre herramientas para que coincida exactamente con el rectángulo de texto de la etiqueta, podrían producirse problemas con la presentación de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="740fd-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="740fd-135">El problema con este esquema simple es que no se puede colocar el rectángulo de texto de información sobre herramientas directamente.</span><span class="sxs-lookup"><span data-stu-id="740fd-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="740fd-136">En su lugar, debe colocar el rectángulo de la ventana de información sobre herramientas justo encima y a la izquierda del rectángulo de texto de la etiqueta para que las esquinas de los dos rectángulos de texto coincidan.</span><span class="sxs-lookup"><span data-stu-id="740fd-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="740fd-137">En otras palabras, debe conocer el desplazamiento entre el rectángulo de la ventana de información sobre herramientas y su rectángulo de texto delimitado.</span><span class="sxs-lookup"><span data-stu-id="740fd-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="740fd-138">En general, no hay ninguna forma sencilla de determinar este desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="740fd-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="740fd-139">Implementar In-Place información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="740fd-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="740fd-140">En el fragmento de código siguiente se muestra cómo usar un mensaje [**\_ ADJUSTRECT de TTM**](ttm-adjustrect.md) en un controlador [TTN \_ Show](ttn-show.md) para mostrar una información sobre herramientas en contexto.</span><span class="sxs-lookup"><span data-stu-id="740fd-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="740fd-141">La aplicación indica que el texto de la etiqueta se trunca estableciendo la variable Private *fMyStringIsTruncated* en **true**.</span><span class="sxs-lookup"><span data-stu-id="740fd-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="740fd-142">El controlador llama a una función definida por la aplicación, **GetMyItemRect**, para recuperar el rectángulo de texto de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="740fd-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="740fd-143">Este rectángulo se pasa al control ToolTip con **TTM \_ ADJUSTRECT**, que devuelve el rectángulo de ventana correspondiente.</span><span class="sxs-lookup"><span data-stu-id="740fd-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="740fd-144">A continuación, se llama a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para colocar la información sobre herramientas sobre la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="740fd-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="740fd-145">En este ejemplo no se cambia el tamaño de la información sobre herramientas, solo su posición.</span><span class="sxs-lookup"><span data-stu-id="740fd-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="740fd-146">Los dos rectángulos de texto se alinean en las esquinas superior izquierda, pero no necesariamente con las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="740fd-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="740fd-147">En la práctica, la diferencia suele ser pequeña y este enfoque se recomienda para la mayoría de los propósitos.</span><span class="sxs-lookup"><span data-stu-id="740fd-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="740fd-148">Aunque puede, en principio, usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para cambiar el tamaño y cambiar la posición de la información sobre herramientas, puede tener consecuencias imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="740fd-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="740fd-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="740fd-149">Remarks</span></span>

<span data-ttu-id="740fd-150">La [versión 5,80](common-control-versions.md) de los controles comunes simplifica el uso de la información sobre herramientas en contexto mediante la adición de un nuevo mensaje, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md).</span><span class="sxs-lookup"><span data-stu-id="740fd-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="740fd-151">Envíe este mensaje con las coordenadas del rectángulo de texto de la etiqueta que desea que la información sobre herramientas se superponga y devuelva las coordenadas de un rectángulo de la ventana de información sobre herramientas colocado correctamente.</span><span class="sxs-lookup"><span data-stu-id="740fd-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="740fd-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="740fd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="740fd-153">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="740fd-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 