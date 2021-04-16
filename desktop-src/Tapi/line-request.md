---
description: El mensaje de solicitud de línea TAPI \_ se envía para informar de la llegada de una nueva solicitud desde otra aplicación.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Mensaje de LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690226"
---
# <a name="line_request-message"></a><span data-ttu-id="6d0f0-103">Mensaje de solicitud de línea \_</span><span class="sxs-lookup"><span data-stu-id="6d0f0-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="6d0f0-104">El mensaje **de \_ solicitud de línea** TAPI se envía para informar de la llegada de una nueva solicitud desde otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6d0f0-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d0f0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0f0-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6d0f0-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6d0f0-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6d0f0-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6d0f0-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6d0f0-109">Instancia de registro de la aplicación especificada en [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span><span class="sxs-lookup"><span data-stu-id="6d0f0-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="6d0f0-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6d0f0-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6d0f0-111">Modo de solicitud de la solicitud recién pendiente.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="6d0f0-112">Este parámetro usa las [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6d0f0-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d0f0-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6d0f0-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6d0f0-114">Las condiciones para este parámetro son, si *dwParam1* se establece en LINEREQUESTMODE \_ Drop, *dwParam2* contiene el *hWnd* de la aplicación que solicita la eliminación.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="6d0f0-115">De lo contrario, *dwParam2* no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="6d0f0-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6d0f0-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6d0f0-117">Si *dwParam1* se establece en LINEREQUESTMODE \_ Drop, la palabra de orden inferior de *dwParam3* contiene el *wRequestID* tal como lo especifica la aplicación que solicitó la eliminación.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="6d0f0-118">De lo contrario, *dwParam3* no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0f0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d0f0-119">Return value</span></span>

<span data-ttu-id="6d0f0-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0f0-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d0f0-121">Remarks</span></span>

<span data-ttu-id="6d0f0-122">El mensaje de **\_ solicitud de línea** se envía a la aplicación de prioridad más alta que se ha registrado para el modo de solicitud correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="6d0f0-123">Este mensaje indica la llegada de una solicitud de telefonía asistida del modo de solicitud especificado.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="6d0f0-124">Si *dwParam1* es LINEREQUESTMODE \_ MAKECALL, la aplicación puede invocar [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) mediante el modo de solicitud correspondiente para recibir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="6d0f0-125">Si *dwParam1* es LINEREQUESTMODE \_ Drop, el mensaje contiene todos los datos que el destinatario de la solicitud necesita para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d0f0-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0f0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d0f0-126">Requirements</span></span>



| <span data-ttu-id="6d0f0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d0f0-127">Requirement</span></span> | <span data-ttu-id="6d0f0-128">Value</span><span class="sxs-lookup"><span data-stu-id="6d0f0-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d0f0-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="6d0f0-129">TAPI version</span></span><br/> | <span data-ttu-id="6d0f0-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6d0f0-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6d0f0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d0f0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="6d0f0-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f0-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0f0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d0f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0f0-134">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="6d0f0-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="6d0f0-135">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="6d0f0-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="6d0f0-136">**tapiRequestMakeCall**</span><span class="sxs-lookup"><span data-stu-id="6d0f0-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




