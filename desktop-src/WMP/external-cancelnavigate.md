---
title: External. cancelNavigate (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. cancelNavigate (método)
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- método cancelNavigate de Windows Media Player
- método cancelNavigate de Windows Media Player, clase externa
- Clase externa Windows Media Player, método cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700030"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="6349b-107">External. cancelNavigate (método)</span><span class="sxs-lookup"><span data-stu-id="6349b-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="6349b-108">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="6349b-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6349b-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6349b-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6349b-110">El método **cancelNavigate** informa a Windows Media Player que no debe mostrar una nueva página de detección aunque la vista haya cambiado en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="6349b-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="6349b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6349b-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="6349b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6349b-112">Parameters</span></span>

<span data-ttu-id="6349b-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6349b-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6349b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6349b-114">Return value</span></span>

<span data-ttu-id="6349b-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6349b-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6349b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6349b-116">Remarks</span></span>

<span data-ttu-id="6349b-117">Cuando la vista cambia en Windows Media Player, el reproductor llama al complemento de la tienda en línea para determinar la página de detección que se va a mostrar a continuación.</span><span class="sxs-lookup"><span data-stu-id="6349b-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="6349b-118">En algunos casos, sin embargo, la tienda en línea podría querer que el reproductor continuara mostrando la página de detección existente.</span><span class="sxs-lookup"><span data-stu-id="6349b-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="6349b-119">El siguiente proceso determina si el reproductor muestra una nueva página de detección:</span><span class="sxs-lookup"><span data-stu-id="6349b-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="6349b-120">Una acción por parte del usuario, ya sea en la interfaz de usuario del reproductor o en la página de detección, solicita que el reproductor cambie su vista.</span><span class="sxs-lookup"><span data-stu-id="6349b-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="6349b-121">El reproductor llama al método [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del complemento para determinar qué página de detección se va a mostrar a continuación.</span><span class="sxs-lookup"><span data-stu-id="6349b-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="6349b-122">El reproductor almacena la dirección URL de la nueva página de detección, pero no muestra la nueva página de detección en este momento.</span><span class="sxs-lookup"><span data-stu-id="6349b-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="6349b-123">El reproductor genera el evento [OnViewChange](external-onviewchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="6349b-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="6349b-124">Si el controlador de eventos **OnViewChange** de la página de detección llama a **CancelNavigate**, el reproductor no muestra la nueva página de detección (determinada en el paso 2).</span><span class="sxs-lookup"><span data-stu-id="6349b-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="6349b-125">En su lugar, sigue mostrando la página de detección existente.</span><span class="sxs-lookup"><span data-stu-id="6349b-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="6349b-126">Si el controlador de eventos **OnViewChange** no llama a **CancelNavigate**, el reproductor muestra la nueva página de detección.</span><span class="sxs-lookup"><span data-stu-id="6349b-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="6349b-127">Por ejemplo, supongamos que el reproductor muestra actualmente la vista de un álbum con una determinada pista seleccionada.</span><span class="sxs-lookup"><span data-stu-id="6349b-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="6349b-128">Supongamos también que la página de detección actual es la página que representa el álbum completo.</span><span class="sxs-lookup"><span data-stu-id="6349b-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="6349b-129">Si el usuario hace clic en otra pista del mismo álbum, la vista del jugador cambia ligeramente para mostrar que la nueva pista está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="6349b-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="6349b-130">Sin embargo, no es necesario mostrar una nueva página de detección.</span><span class="sxs-lookup"><span data-stu-id="6349b-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="6349b-131">La página de detección que representa el álbum completo sigue siendo la página adecuada para que la muestre el reproductor.</span><span class="sxs-lookup"><span data-stu-id="6349b-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="6349b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6349b-132">Requirements</span></span>



| <span data-ttu-id="6349b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6349b-133">Requirement</span></span> | <span data-ttu-id="6349b-134">Value</span><span class="sxs-lookup"><span data-stu-id="6349b-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6349b-135">Versión</span><span class="sxs-lookup"><span data-stu-id="6349b-135">Version</span></span><br/> | <span data-ttu-id="6349b-136">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="6349b-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="6349b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6349b-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="6349b-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6349b-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6349b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6349b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6349b-140">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6349b-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6349b-141">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="6349b-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="6349b-142">**External. OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="6349b-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





