---
title: Control deslizante (referencia de elementos de interfaz de usuario de MSAA)
description: Un control deslizante, también denominado control TrackBar, permite a un usuario seleccionar un intervalo de valores moviendo un control deslizante. Los controles de volumen del sistema operativo Windows son controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076294"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="96db7-104">Control deslizante (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="96db7-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="96db7-105">En este tema se describen los objetos de **control deslizante** para fines de referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="96db7-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="96db7-106">Cómo crear objetos de **control deslizante** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="96db7-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="96db7-107">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="96db7-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="96db7-108">Un control deslizante, también denominado control TrackBar, permite a un usuario seleccionar un intervalo de valores moviendo un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="96db7-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="96db7-109">Los controles de volumen del sistema operativo Windows son controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="96db7-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="96db7-110">El nombre de la clase de ventana de un control deslizante es TRACKBAR \_ (clase), que se define como "msctls \_ TRACKBAR" en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="96db7-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="96db7-111">El contenido de las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de si el control deslizante es vertical u horizontal y en el que el cliente consulta las siguientes partes del control deslizante:</span><span class="sxs-lookup"><span data-stu-id="96db7-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="96db7-112">Ventana de control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-112">Slider window</span></span>
-   <span data-ttu-id="96db7-113">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-113">Slider thumb</span></span>
-   <span data-ttu-id="96db7-114">Área sombreada por encima (o hasta</span><span class="sxs-lookup"><span data-stu-id="96db7-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="96db7-115">Área sombreada debajo (o a la derecha del control deslizante)</span><span class="sxs-lookup"><span data-stu-id="96db7-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="96db7-116">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="96db7-116">IAccessible Methods</span></span>

<span data-ttu-id="96db7-117">Un control deslizante admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="96db7-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="96db7-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="96db7-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="96db7-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="96db7-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="96db7-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="96db7-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="96db7-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="96db7-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="96db7-122">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="96db7-122">IAccessible Properties</span></span>

<span data-ttu-id="96db7-123">Un control deslizante admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="96db7-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="96db7-124">**obtener \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="96db7-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="96db7-125">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="96db7-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="96db7-126">**obtener \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="96db7-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="96db7-127">**obtener \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="96db7-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="96db7-128">**obtener \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="96db7-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="96db7-129">[**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut): la propiedad **KeyboardShortcut** es la tecla de acceso de la ventana de control deslizante, que es un carácter subrayado en el texto de la etiqueta del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="96db7-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="96db7-130">La cadena devuelta contiene el carácter de tecla de acceso anexado a la cadena "Alt +".</span><span class="sxs-lookup"><span data-stu-id="96db7-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="96db7-131">[**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): la propiedad **Name** depende de la parte del control deslizante que se consulta.</span><span class="sxs-lookup"><span data-stu-id="96db7-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="96db7-132">Las partes de un control deslizante vertical tienen los nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="96db7-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="96db7-133">Elemento Slider</span><span class="sxs-lookup"><span data-stu-id="96db7-133">Slider part</span></span>                    | <span data-ttu-id="96db7-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="96db7-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="96db7-135">Ventana de control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-135">Slider window</span></span>                  | <span data-ttu-id="96db7-136">Control de texto estático utilizado como etiqueta</span><span class="sxs-lookup"><span data-stu-id="96db7-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="96db7-137">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-137">Slider thumb</span></span>                   | <span data-ttu-id="96db7-138">Localización</span><span class="sxs-lookup"><span data-stu-id="96db7-138">"Position"</span></span>                          |
    | <span data-ttu-id="96db7-139">Área sombreada encima del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="96db7-140">"Re Pág"</span><span class="sxs-lookup"><span data-stu-id="96db7-140">"Page up"</span></span>                           |
    | <span data-ttu-id="96db7-141">Área sombreada debajo del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="96db7-142">"Av Pág"</span><span class="sxs-lookup"><span data-stu-id="96db7-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="96db7-143">Las partes de un control deslizante horizontal tienen los nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="96db7-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="96db7-144">Elemento Slider</span><span class="sxs-lookup"><span data-stu-id="96db7-144">Slider part</span></span>                              | <span data-ttu-id="96db7-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="96db7-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="96db7-146">Ventana de control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-146">Slider window</span></span>                            | <span data-ttu-id="96db7-147">Control de texto estático utilizado como etiqueta</span><span class="sxs-lookup"><span data-stu-id="96db7-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="96db7-148">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-148">Slider thumb</span></span>                             | <span data-ttu-id="96db7-149">Localización</span><span class="sxs-lookup"><span data-stu-id="96db7-149">"Position"</span></span>                          |
    | <span data-ttu-id="96db7-150">Área sombreada a la izquierda de la miniatura del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="96db7-151">"Página izquierda"</span><span class="sxs-lookup"><span data-stu-id="96db7-151">"Page left"</span></span>                         |
    | <span data-ttu-id="96db7-152">Área sombreada a la derecha de la miniatura del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="96db7-153">"Página derecha"</span><span class="sxs-lookup"><span data-stu-id="96db7-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="96db7-154">[**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent): la propiedad **primaria** de los botones de flecha, el control de desplazamiento y el área sombreada de cualquier lado del control es la ventana de control deslizante.</span><span class="sxs-lookup"><span data-stu-id="96db7-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="96db7-155">La propiedad **primaria** de la ventana de control deslizante es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="96db7-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="96db7-156">[**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la propiedad **role** depende de la parte del control deslizante que se consulta.</span><span class="sxs-lookup"><span data-stu-id="96db7-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="96db7-157">Elemento Slider</span><span class="sxs-lookup"><span data-stu-id="96db7-157">Slider part</span></span>                                     | [<span data-ttu-id="96db7-158">Rol</span><span class="sxs-lookup"><span data-stu-id="96db7-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="96db7-159">Ventana de control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-159">Slider window</span></span>                                   | [<span data-ttu-id="96db7-160">**\_control deslizante del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="96db7-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="96db7-161">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-161">Slider thumb</span></span>                                    | [<span data-ttu-id="96db7-162">**\_indicador del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="96db7-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="96db7-163">Áreas sombreadas en cualquier lado del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="96db7-164">**\_PUSHBUTTON del sistema de roles \_**</span><span class="sxs-lookup"><span data-stu-id="96db7-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="96db7-165">[**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate):[los valores](object-state-constants.md) de la propiedad **State** dependen de la parte del control deslizante que se consulta.</span><span class="sxs-lookup"><span data-stu-id="96db7-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="96db7-166">Elemento Slider</span><span class="sxs-lookup"><span data-stu-id="96db7-166">Slider Part</span></span>                                     | <span data-ttu-id="96db7-167">Valores de estado posibles</span><span class="sxs-lookup"><span data-stu-id="96db7-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="96db7-168">Ventana de control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-168">Slider window</span></span>                                   | <span data-ttu-id="96db7-169">[**Estado \_ de sistema \_**](object-state-constants.md) de estado invisible del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) sistema de estado \| [**\_ \_ enfocable**](object-state-constants.md) del sistema estado de \| [**\_ \_ enfoque**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="96db7-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="96db7-170">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-170">Slider thumb</span></span>                                    | <span data-ttu-id="96db7-171">Cero (0), lo que significa que el objeto está visible o el sistema de [**estado \_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) del sistema</span><span class="sxs-lookup"><span data-stu-id="96db7-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="96db7-172">Áreas sombreadas en cualquier lado del control deslizante</span><span class="sxs-lookup"><span data-stu-id="96db7-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="96db7-173">Cero (0), lo que significa que el objeto está visible o el sistema de [**estado \_ \_ invisible**](object-state-constants.md) sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md) del sistema</span><span class="sxs-lookup"><span data-stu-id="96db7-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="96db7-174">[**obtener \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue): la propiedad **Value** de la ventana de control deslizante indica la posición del control Thumb y es una cadena que contiene un entero de "0" a "100".</span><span class="sxs-lookup"><span data-stu-id="96db7-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="96db7-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96db7-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96db7-176">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="96db7-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="96db7-177">**Barra de desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="96db7-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




