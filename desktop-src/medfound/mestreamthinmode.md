---
description: Generado por un flujo multimedia cuando se inicia o detiene el ligero flujo de la secuencia. Para obtener información acerca del ligero, vea about Rate control.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705989"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="a48b8-104">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="a48b8-104">MEStreamThinMode event</span></span>

<span data-ttu-id="a48b8-105">Generado por un flujo multimedia cuando se inicia o detiene el ligero flujo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a48b8-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="a48b8-106">Para obtener información acerca del *ligero*, vea [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="a48b8-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="a48b8-107">Este evento se puede enviar como respuesta al método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) o al método [**IMFQualityAdvise:: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .</span><span class="sxs-lookup"><span data-stu-id="a48b8-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="a48b8-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a48b8-108">Event values</span></span>

<span data-ttu-id="a48b8-109">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a48b8-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a48b8-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a48b8-110">VARTYPE</span></span></th>
<th><span data-ttu-id="a48b8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a48b8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a48b8-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="a48b8-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="a48b8-113">Indica si se ha iniciado o detenido el ligero.</span><span class="sxs-lookup"><span data-stu-id="a48b8-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="a48b8-114">VARIANT_TRUE: los ejemplos que se entregan después de este evento se definan.</span><span class="sxs-lookup"><span data-stu-id="a48b8-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="a48b8-115">VARIANT_FALSE: los ejemplos que se entregan después de este evento no se simplifican.</span><span class="sxs-lookup"><span data-stu-id="a48b8-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="a48b8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a48b8-116">Requirements</span></span>



| <span data-ttu-id="a48b8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a48b8-117">Requirement</span></span> | <span data-ttu-id="a48b8-118">Value</span><span class="sxs-lookup"><span data-stu-id="a48b8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48b8-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a48b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a48b8-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a48b8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a48b8-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a48b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a48b8-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a48b8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a48b8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a48b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a48b8-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a48b8-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a48b8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a48b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48b8-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a48b8-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




