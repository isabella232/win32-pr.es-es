---
description: Generado por el origen de red cuando termina de abrir una dirección URL.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Evento MEConnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720416"
---
# <a name="meconnectend-event"></a><span data-ttu-id="10263-103">Evento MEConnectEnd</span><span class="sxs-lookup"><span data-stu-id="10263-103">MEConnectEnd event</span></span>

<span data-ttu-id="10263-104">Generado por el origen de red cuando termina de abrir una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="10263-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="10263-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="10263-105">Event values</span></span>

<span data-ttu-id="10263-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="10263-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="10263-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="10263-107">VARTYPE</span></span>              | <span data-ttu-id="10263-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="10263-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="10263-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="10263-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="10263-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="10263-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="10263-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10263-111">Remarks</span></span>

<span data-ttu-id="10263-112">El origen de red envía este evento directamente a la aplicación a través del método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) de la aplicación, no a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) habitual.</span><span class="sxs-lookup"><span data-stu-id="10263-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="10263-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10263-113">Requirements</span></span>



| <span data-ttu-id="10263-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10263-114">Requirement</span></span> | <span data-ttu-id="10263-115">Value</span><span class="sxs-lookup"><span data-stu-id="10263-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10263-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10263-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10263-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10263-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10263-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10263-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10263-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="10263-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10263-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10263-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10263-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10263-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10263-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="10263-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10263-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="10263-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="10263-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10263-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




