---
title: Barra de desplazamiento (referencia de elementos de interfaz de usuario de MSAA)
description: Las barras de desplazamiento permiten a un usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionados. El nombre de la clase de ventana de una barra de desplazamiento es \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078313"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="34deb-104">Barra de desplazamiento (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="34deb-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="34deb-105">En este tema se describen los objetos de **barra de desplazamiento** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="34deb-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="34deb-106">La forma de crear objetos de **barra de desplazamiento** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="34deb-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="34deb-107">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="34deb-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="34deb-108">Las barras de desplazamiento permiten a un usuario elegir la dirección y la distancia para desplazarse por la información en una ventana o un cuadro de lista relacionados.</span><span class="sxs-lookup"><span data-stu-id="34deb-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="34deb-109">El nombre de la clase de ventana de una barra de desplazamiento es "SCROLLBAR".</span><span class="sxs-lookup"><span data-stu-id="34deb-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="34deb-110">El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si la barra de desplazamiento es vertical u horizontal, y en cuál de las siguientes partes de la barra de desplazamiento está siendo consultada por el cliente:</span><span class="sxs-lookup"><span data-stu-id="34deb-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="34deb-111">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-111">The scroll bar itself</span></span>
-   <span data-ttu-id="34deb-112">Botón de flecha superior o derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-112">The top or right arrow button</span></span>
-   <span data-ttu-id="34deb-113">Botón de flecha inferior o izquierda</span><span class="sxs-lookup"><span data-stu-id="34deb-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="34deb-114">Cuadro de desplazamiento (Thumb)</span><span class="sxs-lookup"><span data-stu-id="34deb-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="34deb-115">La región de página arriba o derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-115">The page up or page right region</span></span>
-   <span data-ttu-id="34deb-116">La región de Av Pág o la página izquierda</span><span class="sxs-lookup"><span data-stu-id="34deb-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="34deb-117">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="34deb-117">IAccessible Methods</span></span>

<span data-ttu-id="34deb-118">Una barra de desplazamiento admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="34deb-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="34deb-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction): el propio objeto de barra de desplazamiento y el control de desplazamiento no admiten el método **accDoDefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="34deb-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="34deb-120">En el caso de las demás partes de la barra de desplazamiento de una barra de desplazamiento vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje de [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll) con *wParam* establecido en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34deb-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="34deb-121">Botón o región</span><span class="sxs-lookup"><span data-stu-id="34deb-121">Button/Region</span></span>       | <span data-ttu-id="34deb-122">Vaule</span><span class="sxs-lookup"><span data-stu-id="34deb-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="34deb-123">Botón de flecha superior</span><span class="sxs-lookup"><span data-stu-id="34deb-123">Top arrow button</span></span>    | <span data-ttu-id="34deb-124">\_línea SB</span><span class="sxs-lookup"><span data-stu-id="34deb-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="34deb-125">Botón de flecha abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-125">Bottom arrow button</span></span> | <span data-ttu-id="34deb-126">SB \_ LINEDOWN</span><span class="sxs-lookup"><span data-stu-id="34deb-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="34deb-127">Subir región</span><span class="sxs-lookup"><span data-stu-id="34deb-127">Page up region</span></span>      | <span data-ttu-id="34deb-128">\_Re Pág de SB</span><span class="sxs-lookup"><span data-stu-id="34deb-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="34deb-129">Zona abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-129">Page down region</span></span>    | <span data-ttu-id="34deb-130">reavpág SB \_</span><span class="sxs-lookup"><span data-stu-id="34deb-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="34deb-131">Para las demás partes de la barra de desplazamiento en una barra de desplazamiento horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje de [**\_ HSCROLL de WM**](/windows/desktop/Controls/wm-hscroll) con *wParam* establecido en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="34deb-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="34deb-132">Botón o región</span><span class="sxs-lookup"><span data-stu-id="34deb-132">Button/Region</span></span>      | <span data-ttu-id="34deb-133">Value</span><span class="sxs-lookup"><span data-stu-id="34deb-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="34deb-134">Botón de flecha izquierda</span><span class="sxs-lookup"><span data-stu-id="34deb-134">Left arrow button</span></span>  | <span data-ttu-id="34deb-135">SB \_ LINELEFT</span><span class="sxs-lookup"><span data-stu-id="34deb-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="34deb-136">Botón de flecha a la derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-136">Right arrow button</span></span> | <span data-ttu-id="34deb-137">SB \_ LINERIGHT</span><span class="sxs-lookup"><span data-stu-id="34deb-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="34deb-138">Región izquierda de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-138">Page left region</span></span>   | <span data-ttu-id="34deb-139">SB \_ PAGELEFT</span><span class="sxs-lookup"><span data-stu-id="34deb-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="34deb-140">Región derecha de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-140">Page right region</span></span>  | <span data-ttu-id="34deb-141">SB \_ anclada</span><span class="sxs-lookup"><span data-stu-id="34deb-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="34deb-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="34deb-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="34deb-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="34deb-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="34deb-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="34deb-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="34deb-145">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="34deb-145">IAccessible Properties</span></span>

<span data-ttu-id="34deb-146">Una barra de desplazamiento admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="34deb-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="34deb-147">[**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la propiedad **ChildCount** del objeto de barra de desplazamiento es cinco.</span><span class="sxs-lookup"><span data-stu-id="34deb-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="34deb-148">En el caso de las demás partes de la barra de desplazamiento, la propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="34deb-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="34deb-149">[**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction): el propio objeto de barra de desplazamiento y el control de desplazamiento no admiten la propiedad **DEFAULTACTION** .</span><span class="sxs-lookup"><span data-stu-id="34deb-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="34deb-150">La propiedad **DEFAULTACTION** de los botones de flecha y las áreas sombreadas situadas a cada lado del control de desplazamiento es "Press".</span><span class="sxs-lookup"><span data-stu-id="34deb-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="34deb-151">[**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription): la propiedad **Description** depende de la parte de la barra de desplazamiento que se consulta.</span><span class="sxs-lookup"><span data-stu-id="34deb-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="34deb-152">Las partes de una barra de desplazamiento vertical tienen las siguientes descripciones.</span><span class="sxs-lookup"><span data-stu-id="34deb-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="34deb-153">Parte</span><span class="sxs-lookup"><span data-stu-id="34deb-153">Part</span></span>                | <span data-ttu-id="34deb-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="34deb-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="34deb-155">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-155">Scroll bar itself</span></span>   | <span data-ttu-id="34deb-156">"Se usa para cambiar el área de visualización vertical"</span><span class="sxs-lookup"><span data-stu-id="34deb-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="34deb-157">Botón de flecha superior</span><span class="sxs-lookup"><span data-stu-id="34deb-157">Top arrow button</span></span>    | <span data-ttu-id="34deb-158">"Mueve la posición vertical una línea hacia arriba"</span><span class="sxs-lookup"><span data-stu-id="34deb-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="34deb-159">Botón de flecha abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-159">Bottom arrow button</span></span> | <span data-ttu-id="34deb-160">"Mueve la posición vertical una línea hacia abajo"</span><span class="sxs-lookup"><span data-stu-id="34deb-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="34deb-161">Control de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-161">Scroll thumb</span></span>        | <span data-ttu-id="34deb-162">"Indica la posición vertical actual y se puede arrastrar para cambiarla directamente"</span><span class="sxs-lookup"><span data-stu-id="34deb-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="34deb-163">Subir región</span><span class="sxs-lookup"><span data-stu-id="34deb-163">Page up region</span></span>      | <span data-ttu-id="34deb-164">"Mueve la posición vertical a un par de líneas"</span><span class="sxs-lookup"><span data-stu-id="34deb-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="34deb-165">Zona abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-165">Page down region</span></span>    | <span data-ttu-id="34deb-166">"Indica la posición vertical actual y se puede arrastrar para cambiarla directamente"</span><span class="sxs-lookup"><span data-stu-id="34deb-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="34deb-167">Las partes de una barra de desplazamiento horizontal tienen las siguientes descripciones.</span><span class="sxs-lookup"><span data-stu-id="34deb-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="34deb-168">Parte</span><span class="sxs-lookup"><span data-stu-id="34deb-168">Part</span></span>               | <span data-ttu-id="34deb-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="34deb-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="34deb-170">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-170">Scroll bar itself</span></span>  | <span data-ttu-id="34deb-171">"Se usa para cambiar el área de visualización horizontal"</span><span class="sxs-lookup"><span data-stu-id="34deb-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="34deb-172">Botón de flecha izquierda</span><span class="sxs-lookup"><span data-stu-id="34deb-172">Left arrow button</span></span>  | <span data-ttu-id="34deb-173">"Mueve la posición horizontal una columna hacia la izquierda"</span><span class="sxs-lookup"><span data-stu-id="34deb-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="34deb-174">Botón de flecha a la derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-174">Right arrow button</span></span> | <span data-ttu-id="34deb-175">' Mueve la posición horizontal una columna hacia la derecha '</span><span class="sxs-lookup"><span data-stu-id="34deb-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="34deb-176">Control de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-176">Scroll thumb</span></span>       | <span data-ttu-id="34deb-177">"Indica la posición horizontal actual y se puede arrastrar para cambiarla directamente"</span><span class="sxs-lookup"><span data-stu-id="34deb-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="34deb-178">Región izquierda de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-178">Page left region</span></span>   | <span data-ttu-id="34deb-179">"Mueve la posición horizontal a la izquierda un par de columnas"</span><span class="sxs-lookup"><span data-stu-id="34deb-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="34deb-180">Región derecha de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-180">Page right region</span></span>  | <span data-ttu-id="34deb-181">"Indica la posición vertical actual y se puede arrastrar para cambiarla directamente"</span><span class="sxs-lookup"><span data-stu-id="34deb-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="34deb-182">**obtener \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="34deb-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="34deb-183">**obtener \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="34deb-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="34deb-184">[**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propiedad **Name** depende de la parte de la barra de desplazamiento que se consulta.</span><span class="sxs-lookup"><span data-stu-id="34deb-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="34deb-185">Los elementos de una barra de desplazamiento vertical tienen los nombres siguientes.</span><span class="sxs-lookup"><span data-stu-id="34deb-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="34deb-186">Parte</span><span class="sxs-lookup"><span data-stu-id="34deb-186">Part</span></span>                | <span data-ttu-id="34deb-187">Nombre</span><span class="sxs-lookup"><span data-stu-id="34deb-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="34deb-188">Ventana de barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-188">Scroll bar window</span></span>   | <span data-ttu-id="34deb-189">Vertical</span><span class="sxs-lookup"><span data-stu-id="34deb-189">"Vertical"</span></span>  |
    | <span data-ttu-id="34deb-190">Botón de flecha superior</span><span class="sxs-lookup"><span data-stu-id="34deb-190">Top arrow button</span></span>    | <span data-ttu-id="34deb-191">"Alinear"</span><span class="sxs-lookup"><span data-stu-id="34deb-191">"Line up"</span></span>   |
    | <span data-ttu-id="34deb-192">Botón de flecha abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-192">Bottom arrow button</span></span> | <span data-ttu-id="34deb-193">"Línea abajo"</span><span class="sxs-lookup"><span data-stu-id="34deb-193">"Line down"</span></span> |
    | <span data-ttu-id="34deb-194">Control de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-194">Scroll thumb</span></span>        | <span data-ttu-id="34deb-195">Localización</span><span class="sxs-lookup"><span data-stu-id="34deb-195">"Position"</span></span>  |
    | <span data-ttu-id="34deb-196">Subir región</span><span class="sxs-lookup"><span data-stu-id="34deb-196">Page up region</span></span>      | <span data-ttu-id="34deb-197">"Re Pág"</span><span class="sxs-lookup"><span data-stu-id="34deb-197">"Page up"</span></span>   |
    | <span data-ttu-id="34deb-198">Zona abajo</span><span class="sxs-lookup"><span data-stu-id="34deb-198">Page down region</span></span>    | <span data-ttu-id="34deb-199">"Av Pág"</span><span class="sxs-lookup"><span data-stu-id="34deb-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="34deb-200">Los elementos de una barra de desplazamiento horizontal tienen los nombres siguientes.</span><span class="sxs-lookup"><span data-stu-id="34deb-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="34deb-201">Parte</span><span class="sxs-lookup"><span data-stu-id="34deb-201">Part</span></span>               | <span data-ttu-id="34deb-202">Nombre</span><span class="sxs-lookup"><span data-stu-id="34deb-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="34deb-203">Ventana de barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-203">Scroll bar window</span></span>  | <span data-ttu-id="34deb-204">Horizontal</span><span class="sxs-lookup"><span data-stu-id="34deb-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="34deb-205">Botón de flecha izquierda</span><span class="sxs-lookup"><span data-stu-id="34deb-205">Left arrow button</span></span>  | <span data-ttu-id="34deb-206">"Columna izquierda"</span><span class="sxs-lookup"><span data-stu-id="34deb-206">"Column left"</span></span>  |
    | <span data-ttu-id="34deb-207">Botón de flecha a la derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-207">Right arrow button</span></span> | <span data-ttu-id="34deb-208">"Columna derecha"</span><span class="sxs-lookup"><span data-stu-id="34deb-208">"Column right"</span></span> |
    | <span data-ttu-id="34deb-209">Control de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-209">Scroll thumb</span></span>       | <span data-ttu-id="34deb-210">Localización</span><span class="sxs-lookup"><span data-stu-id="34deb-210">"Position"</span></span>     |
    | <span data-ttu-id="34deb-211">Región derecha de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-211">Page right region</span></span>  | <span data-ttu-id="34deb-212">"Página derecha"</span><span class="sxs-lookup"><span data-stu-id="34deb-212">"Page right"</span></span>   |
    | <span data-ttu-id="34deb-213">Región izquierda de la página</span><span class="sxs-lookup"><span data-stu-id="34deb-213">Page left region</span></span>   | <span data-ttu-id="34deb-214">"Página izquierda"</span><span class="sxs-lookup"><span data-stu-id="34deb-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="34deb-215">[**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propiedad **primaria** de los botones de flecha, el control de desplazamiento y el área sombreada de cualquier lado del control es la ventana de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="34deb-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="34deb-216">La propiedad **primaria** de la ventana de la barra de desplazamiento es una ventana ( \_ ventana del sistema \_ de roles) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="34deb-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="34deb-217">[**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad **role** depende de la parte de la barra de desplazamiento que se consulta.</span><span class="sxs-lookup"><span data-stu-id="34deb-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="34deb-218">Las partes de una barra de desplazamiento tienen los siguientes roles.</span><span class="sxs-lookup"><span data-stu-id="34deb-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="34deb-219">Parte</span><span class="sxs-lookup"><span data-stu-id="34deb-219">Part</span></span>                                                  | <span data-ttu-id="34deb-220">Role</span><span class="sxs-lookup"><span data-stu-id="34deb-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="34deb-221">Barra de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="34deb-222">**\_barra de desplazamiento del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="34deb-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="34deb-223">Botones de flecha arriba, abajo, izquierda y derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="34deb-224">**\_PUSHBUTTON del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="34deb-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="34deb-225">Control de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="34deb-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="34deb-226">**\_indicador del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="34deb-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="34deb-227">Subir página, Av Pág, Av Pág y las regiones de la página a la derecha</span><span class="sxs-lookup"><span data-stu-id="34deb-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="34deb-228">**\_PUSHBUTTON del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="34deb-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="34deb-229">[**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la propiedad **Estado** de cada componente de barra de desplazamiento incluye una combinación de los [valores](object-state-constants.md)siguientes.</span><span class="sxs-lookup"><span data-stu-id="34deb-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="34deb-230">Estado</span><span class="sxs-lookup"><span data-stu-id="34deb-230">State</span></span>                                                                                 | <span data-ttu-id="34deb-231">Value</span><span class="sxs-lookup"><span data-stu-id="34deb-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="34deb-232">**sistema de estado \_ \_ invisible**</span><span class="sxs-lookup"><span data-stu-id="34deb-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="34deb-233">En la barra de desplazamiento, esto indica que la barra de desplazamiento vertical u horizontal especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="34deb-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="34deb-234">En el caso de las regiones Re Pág o Av Pág, esto indica que el control está colocado de forma que la región no exista.</span><span class="sxs-lookup"><span data-stu-id="34deb-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="34deb-235">**sistema de estado \_ \_ oculto**</span><span class="sxs-lookup"><span data-stu-id="34deb-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="34deb-236">Para la barra de desplazamiento en sí, esto indica que la ventana tiene el mismo tamaño que la barra de desplazamiento vertical u horizontal especificada no se muestra actualmente.</span><span class="sxs-lookup"><span data-stu-id="34deb-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="34deb-237">**sistema de estado \_ \_ presionado**</span><span class="sxs-lookup"><span data-stu-id="34deb-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="34deb-238">Se presiona el botón de flecha o el área de la página.</span><span class="sxs-lookup"><span data-stu-id="34deb-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="34deb-239">**ESTADO \_ del sistema \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="34deb-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="34deb-240">El componente está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="34deb-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="34deb-241">[**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propiedad **valor** de la ventana de la barra de desplazamiento indica la posición de la barra de desplazamiento y es una cadena que contiene un entero de "0" a "100".</span><span class="sxs-lookup"><span data-stu-id="34deb-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="34deb-242">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34deb-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34deb-243">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="34deb-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 