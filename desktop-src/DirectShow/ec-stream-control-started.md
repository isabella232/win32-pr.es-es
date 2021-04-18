---
description: Un comando de inicio de control de secuencia ha surtido efecto.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653454"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="2c0b9-103">CONTROL de secuencia de EC \_ \_ \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="2c0b9-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="2c0b9-104">Un comando de inicio de control de secuencia ha surtido efecto.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c0b9-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c0b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0b9-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="2c0b9-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="2c0b9-107">(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN que inició la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="2c0b9-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="2c0b9-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="2c0b9-109">(**DWORD**) Valor definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="2c0b9-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="2c0b9-110">Default Action</span></span>

<span data-ttu-id="2c0b9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0b9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c0b9-112">Remarks</span></span>

<span data-ttu-id="2c0b9-113">Los filtros envían este evento en respuesta al método [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="2c0b9-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="2c0b9-114">Este método especifica un tiempo de referencia para que un código PIN empiece el streaming.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="2c0b9-115">Cuando se inicia la transmisión por secuencias, el filtro envía este evento.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="2c0b9-116">El parámetro *pSender* especifica el PIN que ejecuta el comando START.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="2c0b9-117">Dependiendo de la implementación, es posible que no sea el PIN que recibió la llamada [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="2c0b9-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="2c0b9-118">La aplicación especifica el parámetro *dwCookie* en el método [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="2c0b9-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="2c0b9-119">Este parámetro permite que la aplicación realice el seguimiento de varias llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="2c0b9-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0b9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c0b9-120">Requirements</span></span>



| <span data-ttu-id="2c0b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c0b9-121">Requirement</span></span> | <span data-ttu-id="2c0b9-122">Value</span><span class="sxs-lookup"><span data-stu-id="2c0b9-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0b9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c0b9-123">Header</span></span><br/> | <dl> <span data-ttu-id="2c0b9-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c0b9-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0b9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c0b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0b9-126">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="2c0b9-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2c0b9-127">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2c0b9-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




