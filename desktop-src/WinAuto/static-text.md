---
title: Texto estático (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de texto estático proporcionan una manera cómoda de mostrar texto en los cuadros de diálogo y en otras ventanas. Los controles de texto estáticos suelen servir como etiquetas para otros controles.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f35581a9b305f28782d8faeac81105afb0d5147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903831"
---
# <a name="static-text-msaa-ui-element-reference"></a><span data-ttu-id="930d5-104">Texto estático (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="930d5-104">Static Text (MSAA UI Element Reference)</span></span>

<span data-ttu-id="930d5-105">Los controles de texto estático proporcionan una manera cómoda de mostrar texto en los cuadros de diálogo y en otras ventanas.</span><span class="sxs-lookup"><span data-stu-id="930d5-105">Static text controls provide a convenient way to display text on dialog boxes and other windows.</span></span> <span data-ttu-id="930d5-106">Los controles de texto estáticos suelen servir como etiquetas para otros controles.</span><span class="sxs-lookup"><span data-stu-id="930d5-106">Static text controls often serve as labels for other controls.</span></span>

<span data-ttu-id="930d5-107">El nombre de clase de ventana de un control de texto estático es "STATIC".</span><span class="sxs-lookup"><span data-stu-id="930d5-107">The window class name for a static text control is "STATIC".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="930d5-108">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="930d5-108">IAccessible Methods</span></span>

<span data-ttu-id="930d5-109">Los controles de texto estático admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="930d5-109">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="930d5-110">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="930d5-110">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="930d5-111">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="930d5-111">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="930d5-112">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="930d5-112">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="930d5-113">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="930d5-113">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="930d5-114">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="930d5-114">IAccessible Properties</span></span>

<span data-ttu-id="930d5-115">Los controles de texto estático admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="930d5-115">Static text controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="930d5-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="930d5-116">Property</span></span>                                                                             | <span data-ttu-id="930d5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="930d5-117">Comments</span></span>                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="930d5-118">**obtener \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="930d5-118">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="930d5-119">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="930d5-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="930d5-120">La propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="930d5-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="930d5-121">**obtener \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="930d5-121">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="930d5-122">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="930d5-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="930d5-123">**obtener \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="930d5-123">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="930d5-124">**obtener \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="930d5-124">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="930d5-125">**obtener \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="930d5-125">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="930d5-126">La propiedad **KeyboardShortcut** es la tecla de acceso, que es el carácter subrayado del texto que activa el control asociado al texto estático.</span><span class="sxs-lookup"><span data-stu-id="930d5-126">The **KeyboardShortcut** property is the access key, which is the underlined character in the text that activates the control associated with the static text.</span></span> <span data-ttu-id="930d5-127">La cadena devuelta contiene el carácter de tecla de acceso anexado a la cadena "Alt +".</span><span class="sxs-lookup"><span data-stu-id="930d5-127">The returned string contains the access key character appended to the string "Alt+".</span></span>                                           |
| [<span data-ttu-id="930d5-128">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="930d5-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="930d5-129">La propiedad **Name** es igual que el texto del control de texto estático.</span><span class="sxs-lookup"><span data-stu-id="930d5-129">The **Name** property is the same as the text in the static text control.</span></span>                                                                                                                                                                                                                     |
| [<span data-ttu-id="930d5-130">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="930d5-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="930d5-131">La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="930d5-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                   |
| [<span data-ttu-id="930d5-132">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="930d5-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="930d5-133">La propiedad **role** es [**\_ \_ STATICTEXT del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="930d5-133">The **Role** property is [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md).</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="930d5-134">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="930d5-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="930d5-135">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): sistema de estado de [**\_ \_ solo lectura**](object-state-constants.md) sistema de estado \| [**\_ \_ invisible**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="930d5-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="930d5-136">Notas</span><span class="sxs-lookup"><span data-stu-id="930d5-136">Notes</span></span>

-   <span data-ttu-id="930d5-137">El método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) devuelve el \_ \_ MEMBERNOTFOUND cuando se llama con [**SELFLAG \_ TAKEFOCUS**](selflag.md) en un objeto de texto estático.</span><span class="sxs-lookup"><span data-stu-id="930d5-137">The [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method returns DISP\_E\_MEMBERNOTFOUND when it is called with [**SELFLAG\_TAKEFOCUS**](selflag.md) on a static text object.</span></span>
-   <span data-ttu-id="930d5-138">Los controles estáticos con el \_ estilo de icono SS devuelven datos no válidos en la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="930d5-138">Static controls with the SS\_ICON style return invalid data in the **Name** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="930d5-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="930d5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="930d5-140">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="930d5-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





