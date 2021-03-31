---
description: Lo genera un origen multimedia cuando actualiza sus metadatos.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001266"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="823be-103">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="823be-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="823be-104">Lo genera un origen multimedia cuando actualiza sus metadatos.</span><span class="sxs-lookup"><span data-stu-id="823be-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="823be-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="823be-105">Event values</span></span>

<span data-ttu-id="823be-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="823be-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="823be-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="823be-107">VARTYPE</span></span>              | <span data-ttu-id="823be-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="823be-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="823be-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="823be-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="823be-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="823be-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="823be-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="823be-111">Remarks</span></span>

<span data-ttu-id="823be-112">Si el origen multimedia no puede proporcionar todos los metadatos cuando el origen se crea por primera vez, debería producir este evento una vez que los metadatos estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="823be-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="823be-113">El origen multimedia debe crear un nuevo descriptor de presentación y copiar todos los atributos del descriptor de presentación (PD) en el objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="823be-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="823be-114">La aplicación puede utilizar el objeto de evento para enumerar los nuevos atributos PD.</span><span class="sxs-lookup"><span data-stu-id="823be-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="823be-115">En concreto, es posible que los valores de la [ \_ \_ duración de MF PD](mf-pd-duration-attribute.md) y el [ \_ \_ \_ \_ Tamaño total de archivo MF PD](mf-pd-total-file-size-attribute.md) sean desconocidos hasta que el archivo se descargue completamente.</span><span class="sxs-lookup"><span data-stu-id="823be-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="823be-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823be-116">Requirements</span></span>



| <span data-ttu-id="823be-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="823be-117">Requirement</span></span> | <span data-ttu-id="823be-118">Value</span><span class="sxs-lookup"><span data-stu-id="823be-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823be-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="823be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="823be-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="823be-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="823be-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="823be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="823be-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="823be-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="823be-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="823be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="823be-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="823be-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823be-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="823be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823be-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="823be-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="823be-127">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="823be-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




