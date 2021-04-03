---
title: Propiedades del control
description: Propiedades del control
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903852"
---
# <a name="control-properties"></a><span data-ttu-id="ad816-103">Propiedades del control</span><span class="sxs-lookup"><span data-stu-id="ad816-103">Control Properties</span></span>

<span data-ttu-id="ad816-104">Además de las propiedades definidas e implementadas por el propio control, la tecnología de controles ActiveX también implica:</span><span class="sxs-lookup"><span data-stu-id="ad816-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="ad816-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propiedades de ambiente</span><span class="sxs-lookup"><span data-stu-id="ad816-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="ad816-106">Los expone el contenedor a través de un sitio de cliente de control para proporcionar valores de entorno que se aplican a todos los controles insertados en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="ad816-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="ad816-107">Por ejemplo, un contenedor puede proporcionar un color de fondo predeterminado o una fuente predeterminada que el control puede utilizar.</span><span class="sxs-lookup"><span data-stu-id="ad816-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="ad816-108">Las propiedades de ambiente se exponen a través de **IDispatch** implementadas en el objeto de sitio de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ad816-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="ad816-109">El contenedor llama al método [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) del control cuando alguna de sus propiedades de ambiente cambian de valor.</span><span class="sxs-lookup"><span data-stu-id="ad816-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="ad816-110">En respuesta, es posible que un control tenga que actualizar su propio estado interno o visual en respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad816-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="ad816-111">El contenedor indica qué propiedad ambiente cambió con el parámetro DISPID o puede pasar DISPID \_ Unknown para indicar que han cambiado varias propiedades de ambiente.</span><span class="sxs-lookup"><span data-stu-id="ad816-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="ad816-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propiedades extendidas</span><span class="sxs-lookup"><span data-stu-id="ad816-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="ad816-113">En realidad, los implementa un contenedor para encapsular los controles que contiene para proporcionar propiedades administradas por contenedores que aparecen como si fueran propiedades de control nativas.</span><span class="sxs-lookup"><span data-stu-id="ad816-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="ad816-114">El contenedor puede Agregar el control agregando las propiedades extendidas para complementar o reemplazar las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="ad816-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="ad816-115">El objeto agregado se denomina control extendido.</span><span class="sxs-lookup"><span data-stu-id="ad816-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="ad816-116">En el contenedor, el control extendido aparece como el control en sí y las propiedades extendidas parecen expuestas por el control.</span><span class="sxs-lookup"><span data-stu-id="ad816-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="ad816-117">El contenedor admite un control extendido a través de su método de sitio de cliente [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="ad816-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="ad816-118">El método **GetExtendedControl** permite que los controles naveguen por el sitio hasta el objeto de control extendido proporcionado por el contenedor, si el contenedor es compatible con esta característica.</span><span class="sxs-lookup"><span data-stu-id="ad816-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="ad816-119">Un contenedor también puede optar por mostrar las páginas de propiedades de sus controles extendidos además de las páginas que un control especificaría normalmente a través de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span><span class="sxs-lookup"><span data-stu-id="ad816-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="ad816-120">Por este motivo, un control tiene que pedir a un contenedor que muestre un marco de propiedades antes de que el control intente hacerlo.</span><span class="sxs-lookup"><span data-stu-id="ad816-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="ad816-121">El control llama a [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="ad816-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="ad816-122">Si el contenedor implementa esta función, muestra el propio marco de propiedades; Si el método devuelve un error, el control puede mostrar el marco de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ad816-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="ad816-123">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ad816-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ad816-124">Propiedades estándar</span><span class="sxs-lookup"><span data-stu-id="ad816-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="ad816-125">Objeto de fuente estándar</span><span class="sxs-lookup"><span data-stu-id="ad816-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="ad816-126">Objeto de imagen estándar</span><span class="sxs-lookup"><span data-stu-id="ad816-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="ad816-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad816-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad816-128">Métodos de control</span><span class="sxs-lookup"><span data-stu-id="ad816-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




