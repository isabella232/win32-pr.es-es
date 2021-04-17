---
title: Evento external. OnSendMessageComplete
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Media Player de eventos external. OnSendMessageComplete de Windows
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698589"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="e2d76-105">Evento external. OnSendMessageComplete</span><span class="sxs-lookup"><span data-stu-id="e2d76-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="e2d76-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="e2d76-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e2d76-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e2d76-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e2d76-108">El evento **OnSendMessageComplete** se produce cuando la tienda en línea ha finalizado el procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2d76-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="e2d76-109">El script de la página de detección envió previamente el mensaje mediante una llamada a [external. SendMessage](external-sendmessage.md).</span><span class="sxs-lookup"><span data-stu-id="e2d76-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="e2d76-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e2d76-110">Possible Values</span></span>

<span data-ttu-id="e2d76-111">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="e2d76-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2d76-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2d76-112">Parameters</span></span>

<span data-ttu-id="e2d76-113">La función que controla este evento tiene los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="e2d76-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="e2d76-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Mensaje*</span><span class="sxs-lookup"><span data-stu-id="e2d76-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="e2d76-115">La misma cadena que se pasó en el parámetro **MSG** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="e2d76-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d76-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span><span class="sxs-lookup"><span data-stu-id="e2d76-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="e2d76-117">La misma cadena que se pasó en el parámetro **param** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="e2d76-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d76-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Da*</span><span class="sxs-lookup"><span data-stu-id="e2d76-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="e2d76-119">**Cadena** que contiene el resultado del control de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2d76-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="e2d76-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="e2d76-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2d76-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2d76-121">Remarks</span></span>

<span data-ttu-id="e2d76-122">El método **SendMessage** llama a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), que devuelve de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e2d76-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="e2d76-123">Es decir, se devuelve antes de que la tienda en línea termine de procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e2d76-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="e2d76-124">Cuando la tienda en línea termina de procesar el mensaje, llama a [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), que a su vez llama al controlador de eventos **OnSendMessageComplete** del script.</span><span class="sxs-lookup"><span data-stu-id="e2d76-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="e2d76-125">Cuando la tienda en línea llama a **IWMPContentPartnerCallback:: SendMessageComplete**, proporciona un código de resultado en el parámetro *bstrResult* .</span><span class="sxs-lookup"><span data-stu-id="e2d76-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="e2d76-126">Windows Media Player no interpreta ese código de resultado.</span><span class="sxs-lookup"><span data-stu-id="e2d76-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="e2d76-127">En su lugar, Windows Media Player pasa el código de resultado junto con el controlador de eventos **OnSendMessageComplete** en el parámetro *result* .</span><span class="sxs-lookup"><span data-stu-id="e2d76-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="e2d76-128">Windows Media Player interpreta ninguno de los parámetros (*MSG*, *param*, *result*) del controlador de eventos **OnSendMessageComplete** .</span><span class="sxs-lookup"><span data-stu-id="e2d76-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="e2d76-129">Los parámetros solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e2d76-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d76-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d76-130">Requirements</span></span>



| <span data-ttu-id="e2d76-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d76-131">Requirement</span></span> | <span data-ttu-id="e2d76-132">Value</span><span class="sxs-lookup"><span data-stu-id="e2d76-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d76-133">Versión</span><span class="sxs-lookup"><span data-stu-id="e2d76-133">Version</span></span><br/> | <span data-ttu-id="e2d76-134">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="e2d76-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="e2d76-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2d76-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2d76-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d76-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d76-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d76-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d76-138">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e2d76-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e2d76-139">**External. sendMessage**</span><span class="sxs-lookup"><span data-stu-id="e2d76-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="e2d76-140">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="e2d76-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="e2d76-141">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="e2d76-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





