---
description: Enviado por la canalización al codificador MFTs en serie con muestras multimedia a través de IMFTransform::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Evento MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275976"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="e1f6d-103">Evento MEEncodingParameters</span><span class="sxs-lookup"><span data-stu-id="e1f6d-103">MEEncodingParameters event</span></span>

<span data-ttu-id="e1f6d-104">Enviado por la canalización al codificador MFTs en serie con muestras multimedia a través de [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="e1f6d-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="e1f6d-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e1f6d-105">Event values</span></span>

<span data-ttu-id="e1f6d-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e1f6d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e1f6d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1f6d-107">VARTYPE</span></span>              | <span data-ttu-id="e1f6d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f6d-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e1f6d-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="e1f6d-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e1f6d-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="e1f6d-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="e1f6d-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="e1f6d-111">Attributes</span></span>

<span data-ttu-id="e1f6d-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e1f6d-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e1f6d-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="e1f6d-113">Attribute</span></span>                                         | <span data-ttu-id="e1f6d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f6d-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1f6d-115">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="e1f6d-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="e1f6d-116">Contiene la nueva configuración basada en ICodecAPI que el codificador debería aplicar en los ejemplos de entrada posteriores.</span><span class="sxs-lookup"><span data-stu-id="e1f6d-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e1f6d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1f6d-117">Remarks</span></span>

<span data-ttu-id="e1f6d-118">La carga del evento es un almacén de atributos (puntero IMFAttributes) que contiene los nuevos valores de configuración basados en ICodecAPI que el codificador debe aplicar en los ejemplos posteriores entrantes.</span><span class="sxs-lookup"><span data-stu-id="e1f6d-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f6d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1f6d-119">Requirements</span></span>



| <span data-ttu-id="e1f6d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1f6d-120">Requirement</span></span> | <span data-ttu-id="e1f6d-121">Value</span><span class="sxs-lookup"><span data-stu-id="e1f6d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f6d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1f6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f6d-123">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e1f6d-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e1f6d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1f6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f6d-125">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1f6d-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e1f6d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1f6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1f6d-127"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f6d-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f6d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1f6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f6d-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1f6d-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




