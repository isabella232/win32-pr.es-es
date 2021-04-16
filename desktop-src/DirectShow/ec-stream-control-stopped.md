---
description: Un comando de detención del control de secuencias ha surtido efecto.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690284"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="05cda-103">CONTROL de secuencia de EC \_ \_ \_ detenido</span><span class="sxs-lookup"><span data-stu-id="05cda-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="05cda-104">Un comando de detención del control de secuencias ha surtido efecto.</span><span class="sxs-lookup"><span data-stu-id="05cda-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="05cda-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05cda-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05cda-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="05cda-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="05cda-107">(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN que detuvo la secuencia.</span><span class="sxs-lookup"><span data-stu-id="05cda-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="05cda-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="05cda-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="05cda-109">(**DWORD**) Valor definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="05cda-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="05cda-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="05cda-110">Default Action</span></span>

<span data-ttu-id="05cda-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05cda-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="05cda-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05cda-112">Remarks</span></span>

<span data-ttu-id="05cda-113">Los filtros envían este evento en respuesta al método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="05cda-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="05cda-114">El método **StopAt** especifica un tiempo de referencia para que un código PIN detenga el streaming.</span><span class="sxs-lookup"><span data-stu-id="05cda-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="05cda-115">Cuando se detiene el streaming, el filtro envía este evento.</span><span class="sxs-lookup"><span data-stu-id="05cda-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="05cda-116">El parámetro *pSender* especifica el PIN que ejecuta el comando STOP.</span><span class="sxs-lookup"><span data-stu-id="05cda-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="05cda-117">Dependiendo de la implementación, es posible que no sea el PIN que recibió la llamada [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="05cda-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="05cda-118">La aplicación especifica el parámetro *dwCookie* en el método [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="05cda-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="05cda-119">Este parámetro permite que la aplicación realice el seguimiento de varias llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="05cda-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="05cda-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05cda-120">Requirements</span></span>



| <span data-ttu-id="05cda-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05cda-121">Requirement</span></span> | <span data-ttu-id="05cda-122">Value</span><span class="sxs-lookup"><span data-stu-id="05cda-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05cda-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05cda-123">Header</span></span><br/> | <dl> <span data-ttu-id="05cda-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="05cda-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05cda-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="05cda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05cda-126">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="05cda-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="05cda-127">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="05cda-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




