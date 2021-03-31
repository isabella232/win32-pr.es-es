---
title: Propiedades de ambiente para controles
description: Propiedades de ambiente para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418823"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="c18c3-103">Propiedades de ambiente para controles</span><span class="sxs-lookup"><span data-stu-id="c18c3-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="c18c3-104">Si un control admite cualquier propiedad de ambiente, debe respetar al menos los valores de las siguientes propiedades de ambiente en las condiciones indicadas en la siguiente tabla con los DISPID estándar.</span><span class="sxs-lookup"><span data-stu-id="c18c3-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="c18c3-105">Propiedad Ambient</span><span class="sxs-lookup"><span data-stu-id="c18c3-105">Ambient Property</span></span>            | <span data-ttu-id="c18c3-106">DISPID</span><span class="sxs-lookup"><span data-stu-id="c18c3-106">Dispid</span></span>          | <span data-ttu-id="c18c3-107">Comentario y condiciones para su uso</span><span class="sxs-lookup"><span data-stu-id="c18c3-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c18c3-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="c18c3-108">LocaleID</span></span><br/>         | <span data-ttu-id="c18c3-109">-705</span><span class="sxs-lookup"><span data-stu-id="c18c3-109">-705</span></span><br/> | <span data-ttu-id="c18c3-110">Si la configuración regional es significativa para el control, por ejemplo, para la salida de texto</span><span class="sxs-lookup"><span data-stu-id="c18c3-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="c18c3-111">En modo usuario</span><span class="sxs-lookup"><span data-stu-id="c18c3-111">UserMode</span></span> <br/>        | <span data-ttu-id="c18c3-112">-709</span><span class="sxs-lookup"><span data-stu-id="c18c3-112">-709</span></span><br/> | <span data-ttu-id="c18c3-113">Si el control se comporta de forma diferente en modo de usuario (diseño) y modo de ejecución</span><span class="sxs-lookup"><span data-stu-id="c18c3-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="c18c3-114">UIDead</span><span class="sxs-lookup"><span data-stu-id="c18c3-114">UIDead</span></span><br/>           | <span data-ttu-id="c18c3-115">-710</span><span class="sxs-lookup"><span data-stu-id="c18c3-115">-710</span></span><br/> | <span data-ttu-id="c18c3-116">Si el control reacciona a los eventos de la interfaz de usuario, debe respetar esta propiedad de ambiente</span><span class="sxs-lookup"><span data-stu-id="c18c3-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="c18c3-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="c18c3-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="c18c3-118">-711</span><span class="sxs-lookup"><span data-stu-id="c18c3-118">-711</span></span><br/> | <span data-ttu-id="c18c3-119">Si el control admite el cambio de tamaño en contexto de sí mismo</span><span class="sxs-lookup"><span data-stu-id="c18c3-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="c18c3-120">ShowHatching</span><span class="sxs-lookup"><span data-stu-id="c18c3-120">ShowHatching</span></span><br/>     | <span data-ttu-id="c18c3-121">-712</span><span class="sxs-lookup"><span data-stu-id="c18c3-121">-712</span></span><br/> | <span data-ttu-id="c18c3-122">Si el control admite la activación en contexto y la activación de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c18c3-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="c18c3-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="c18c3-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="c18c3-124">-713</span><span class="sxs-lookup"><span data-stu-id="c18c3-124">-713</span></span><br/> | <span data-ttu-id="c18c3-125">Solo si el control está marcado como OLEMISC \_ ACTSLIKEBUTTON (lo que significa que se proporciona compatibilidad con teclas de método abreviado, por lo que se debe implementar [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) y [**IOleControl::**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) ).</span><span class="sxs-lookup"><span data-stu-id="c18c3-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="c18c3-126">Tal y como se ha descrito anteriormente, el uso de los ambiente requiere [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como mínimo), así como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) y [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="c18c3-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="c18c3-127">\_Es posible que un contenedor no admita necesariamente el bit OLEMISC SETCLIENTSITEFIRST.</span><span class="sxs-lookup"><span data-stu-id="c18c3-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="c18c3-128">En estas circunstancias, un control debe recurrir a los valores predeterminados para las propiedades de ambiente que requiere.</span><span class="sxs-lookup"><span data-stu-id="c18c3-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c18c3-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c18c3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c18c3-130">Controles</span><span class="sxs-lookup"><span data-stu-id="c18c3-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





