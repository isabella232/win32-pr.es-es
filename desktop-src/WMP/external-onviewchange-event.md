---
title: Evento external. OnViewChange
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El evento OnViewChange se produce cuando cambia la vista en Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Media Player de eventos external. OnViewChange de Windows
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698586"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="c48dd-106">Evento external. OnViewChange</span><span class="sxs-lookup"><span data-stu-id="c48dd-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="c48dd-107">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="c48dd-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c48dd-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="c48dd-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c48dd-109">El evento **OnViewChange** se produce cuando cambia la vista en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c48dd-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="c48dd-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c48dd-110">Possible Values</span></span>

<span data-ttu-id="c48dd-111">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="c48dd-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="c48dd-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c48dd-112">Parameters</span></span>

<span data-ttu-id="c48dd-113">La función que controla este evento no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="c48dd-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c48dd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c48dd-114">Remarks</span></span>

<span data-ttu-id="c48dd-115">La vista de Windows Media Player puede cambiar por cualquiera de los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="c48dd-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="c48dd-116">El usuario interactúa con la interfaz de usuario de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c48dd-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="c48dd-117">El usuario interactúa con una página de detección y el script en la página de detección llama a [external. changeView](external-changeview.md).</span><span class="sxs-lookup"><span data-stu-id="c48dd-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="c48dd-118">El usuario interactúa con una página de detección y el script en la página de detección llama a [external. changeViewOnlineList](external-changeviewonlinelist.md).</span><span class="sxs-lookup"><span data-stu-id="c48dd-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="c48dd-119">Cuando la vista cambia en Windows Media Player, el reproductor llama a [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) para obtener la dirección URL de la página de detección siguiente que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c48dd-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="c48dd-120">Sin embargo, antes de que el reproductor muestre la nueva página de detección, se genera el evento **OnViewChange** .</span><span class="sxs-lookup"><span data-stu-id="c48dd-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="c48dd-121">Si el controlador de eventos **OnViewChange** llama a [external. cancelNavigate](external-cancelnavigate.md), Windows Media Player no muestra la nueva página de detección.</span><span class="sxs-lookup"><span data-stu-id="c48dd-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="c48dd-122">En su lugar, sigue mostrando la página de detección actual.</span><span class="sxs-lookup"><span data-stu-id="c48dd-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48dd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c48dd-123">Requirements</span></span>



| <span data-ttu-id="c48dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c48dd-124">Requirement</span></span> | <span data-ttu-id="c48dd-125">Value</span><span class="sxs-lookup"><span data-stu-id="c48dd-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c48dd-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c48dd-126">Version</span></span><br/> | <span data-ttu-id="c48dd-127">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c48dd-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="c48dd-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c48dd-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c48dd-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c48dd-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48dd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c48dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48dd-131">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="c48dd-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c48dd-132">**External. changeView**</span><span class="sxs-lookup"><span data-stu-id="c48dd-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="c48dd-133">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="c48dd-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





