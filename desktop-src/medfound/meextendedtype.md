---
description: Tipo de evento personalizado.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Evento MEExtendedType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687227"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="241d8-103">Evento MEExtendedType</span><span class="sxs-lookup"><span data-stu-id="241d8-103">MEExtendedType event</span></span>

<span data-ttu-id="241d8-104">Tipo de evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="241d8-104">Custom event type.</span></span> <span data-ttu-id="241d8-105">Puede usar este tipo de evento para definir eventos personalizados para el componente.</span><span class="sxs-lookup"><span data-stu-id="241d8-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="241d8-106">Use el tipo de evento extendido para identificar el evento.</span><span class="sxs-lookup"><span data-stu-id="241d8-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="241d8-107">El tipo de evento extendido es un valor GUID asociado al evento.</span><span class="sxs-lookup"><span data-stu-id="241d8-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="241d8-108">Para obtener más información, vea [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="241d8-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="241d8-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="241d8-109">Event values</span></span>

<span data-ttu-id="241d8-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="241d8-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="241d8-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="241d8-111">VARTYPE</span></span>              | <span data-ttu-id="241d8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="241d8-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="241d8-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="241d8-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="241d8-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="241d8-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="241d8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="241d8-115">Requirements</span></span>



| <span data-ttu-id="241d8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="241d8-116">Requirement</span></span> | <span data-ttu-id="241d8-117">Value</span><span class="sxs-lookup"><span data-stu-id="241d8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="241d8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="241d8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="241d8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="241d8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="241d8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="241d8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="241d8-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="241d8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="241d8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="241d8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="241d8-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="241d8-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="241d8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="241d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241d8-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="241d8-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




