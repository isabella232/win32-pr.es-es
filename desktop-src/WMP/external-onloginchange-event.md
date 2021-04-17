---
title: Evento external. OnLoginChange
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Media Player de eventos external. OnLoginChange de Windows
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698590"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="0b742-105">Evento external. OnLoginChange</span><span class="sxs-lookup"><span data-stu-id="0b742-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="0b742-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="0b742-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0b742-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="0b742-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0b742-108">El evento **OnLoginChange** se produce cuando cambia el estado del inicio de sesión del usuario o cuando se produce un error al intentar iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="0b742-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="0b742-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0b742-109">Possible Values</span></span>

<span data-ttu-id="0b742-110">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="0b742-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b742-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b742-111">Parameters</span></span>

<span data-ttu-id="0b742-112">La función que controla este evento no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="0b742-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b742-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b742-113">Remarks</span></span>

<span data-ttu-id="0b742-114">Este evento se produce cada vez que el complemento de la tienda en línea llama a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="0b742-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="0b742-115">A veces, el complemento realiza esta llamada para notificar a Windows Media Player que se ha producido un cambio en el estado de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="0b742-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="0b742-116">En otras ocasiones, el complemento realiza esta llamada para notificar al reproductor que se produjo un error al intentar iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="0b742-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="0b742-117">El parámetro *pContext* del método **Notify** especifica si la notificación es para un cambio de estado de inicio de sesión o para un intento de inicio de sesión erróneo.</span><span class="sxs-lookup"><span data-stu-id="0b742-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="0b742-118">Dado que cada llamada a `Notify(wmpcnLoginStateChange, ...)` hace que Windows Media Player genere el evento **OnLoginChange** , a veces se llama al controlador de eventos **OnLoginChange** como resultado de un cambio en el estado de inicio de sesión y, a veces, como resultado de un intento de inicio de sesión erróneo.</span><span class="sxs-lookup"><span data-stu-id="0b742-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="0b742-119">Para determinar el estado de inicio de sesión actual del usuario, el controlador de eventos **OnLoginChange** debe llamar a [external. userLoggedIn](external-userloggedin.md).</span><span class="sxs-lookup"><span data-stu-id="0b742-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b742-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b742-120">Requirements</span></span>



| <span data-ttu-id="0b742-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b742-121">Requirement</span></span> | <span data-ttu-id="0b742-122">Value</span><span class="sxs-lookup"><span data-stu-id="0b742-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b742-123">Versión</span><span class="sxs-lookup"><span data-stu-id="0b742-123">Version</span></span><br/> | <span data-ttu-id="0b742-124">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="0b742-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="0b742-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b742-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b742-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b742-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b742-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b742-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b742-128">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="0b742-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0b742-129">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="0b742-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="0b742-130">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="0b742-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





