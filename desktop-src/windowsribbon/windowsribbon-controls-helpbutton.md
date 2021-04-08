---
title: Botón ayuda
description: El botón ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995273"
---
# <a name="help-button"></a><span data-ttu-id="96216-103">Botón ayuda</span><span class="sxs-lookup"><span data-stu-id="96216-103">Help Button</span></span>

<span data-ttu-id="96216-104">El botón ayuda es un control en el que el usuario puede hacer clic para mostrar el sistema de ayuda de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="96216-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="96216-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="96216-105">Details</span></span>](#details)
-   [<span data-ttu-id="96216-106">Propiedades del botón ayuda</span><span class="sxs-lookup"><span data-stu-id="96216-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="96216-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96216-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="96216-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="96216-108">Details</span></span>

<span data-ttu-id="96216-109">En la captura de pantalla siguiente se muestra el botón ayuda de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="96216-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![captura de pantalla que muestra el botón ayuda.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="96216-111">Propiedades del botón ayuda</span><span class="sxs-lookup"><span data-stu-id="96216-111">Help Button Properties</span></span>

<span data-ttu-id="96216-112">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de ayuda.</span><span class="sxs-lookup"><span data-stu-id="96216-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="96216-113">Normalmente, una propiedad del botón ayuda se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="96216-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="96216-114">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="96216-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="96216-115">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="96216-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="96216-116">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="96216-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="96216-117">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="96216-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="96216-118">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de ayuda.</span><span class="sxs-lookup"><span data-stu-id="96216-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="96216-119">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="96216-119">Property Key</span></span>                                                                                     | <span data-ttu-id="96216-120">Notas</span><span class="sxs-lookup"><span data-stu-id="96216-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="96216-121">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="96216-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="96216-122">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="96216-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="96216-123">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="96216-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="96216-124">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="96216-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="96216-125">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="96216-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="96216-126">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="96216-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="96216-127">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="96216-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="96216-128">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="96216-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="96216-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96216-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96216-130">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="96216-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="96216-131">**Elemento HelpButton**</span><span class="sxs-lookup"><span data-stu-id="96216-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 