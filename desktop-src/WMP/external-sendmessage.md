---
title: External. sendMessage (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método sendMessage envía un mensaje al complemento de la tienda en línea.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- método sendMessage de Windows Media Player
- método sendMessage Windows Media Player, clase externa
- Clase externa Windows Media Player, método sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699727"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="3fdf2-108">External. sendMessage (método)</span><span class="sxs-lookup"><span data-stu-id="3fdf2-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="3fdf2-109">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3fdf2-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3fdf2-111">El método **SendMessage** envía un mensaje al complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fdf2-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fdf2-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="3fdf2-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fdf2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdf2-114">*Mensaje* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3fdf2-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fdf2-115">**Cadena** que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="3fdf2-116">*Parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fdf2-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fdf2-117">**Cadena** que contiene los parámetros asociados al mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fdf2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fdf2-118">Return value</span></span>

<span data-ttu-id="3fdf2-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fdf2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fdf2-120">Remarks</span></span>

<span data-ttu-id="3fdf2-121">El mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-121">The message is sent asynchronously.</span></span> <span data-ttu-id="3fdf2-122">Es decir, este método vuelve inmediatamente en lugar de esperar a que se procese el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="3fdf2-123">Cuando el complemento termina de procesar el mensaje, llama al método [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , que a su vez llama al controlador de eventos [OnSendMessageComplete](external-onsendmessagecomplete-event.md) del script.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdf2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fdf2-124">Requirements</span></span>



| <span data-ttu-id="3fdf2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fdf2-125">Requirement</span></span> | <span data-ttu-id="3fdf2-126">Value</span><span class="sxs-lookup"><span data-stu-id="3fdf2-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdf2-127">Versión</span><span class="sxs-lookup"><span data-stu-id="3fdf2-127">Version</span></span><br/> | <span data-ttu-id="3fdf2-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3fdf2-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="3fdf2-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fdf2-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fdf2-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fdf2-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fdf2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fdf2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fdf2-132">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="3fdf2-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3fdf2-133">**External. OnSendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="3fdf2-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="3fdf2-134">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="3fdf2-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="3fdf2-135">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="3fdf2-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





