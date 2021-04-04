---
description: El flujo multimedia usa este evento para enviar metadatos específicos del sistema de protección al descodificador.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908255"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="dcbf1-103">Evento MEContentProtectionMetadata</span><span class="sxs-lookup"><span data-stu-id="dcbf1-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="dcbf1-104">El flujo multimedia usa este evento para enviar metadatos específicos del sistema de protección al descodificador.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="dcbf1-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="dcbf1-105">Event values</span></span>

<span data-ttu-id="dcbf1-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dcbf1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dcbf1-107">VARTYPE</span></span>              | <span data-ttu-id="dcbf1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcbf1-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="dcbf1-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="dcbf1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="dcbf1-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="dcbf1-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="dcbf1-111">Attributes</span></span>

<span data-ttu-id="dcbf1-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="dcbf1-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="dcbf1-113">Attribute</span></span>                                                                                              | <span data-ttu-id="dcbf1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcbf1-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcbf1-115">\_KEYDATA de \_ \_ metadatos del flujo de eventos MF \_</span><span class="sxs-lookup"><span data-stu-id="dcbf1-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="dcbf1-116">Es un atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-116">This is an optional attribute.</span></span> <span data-ttu-id="dcbf1-117">Datos específicos del sistema de protección.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="dcbf1-118">\_contenido de \_ metadatos del flujo de eventos MF \_ \_ \_ KEYIDS</span><span class="sxs-lookup"><span data-stu-id="dcbf1-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="dcbf1-119">Los identificadores de clave de contenido a los que está asociado el evento.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="dcbf1-120">\_SYSTEMID de \_ \_ metadatos del flujo de eventos MF \_</span><span class="sxs-lookup"><span data-stu-id="dcbf1-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="dcbf1-121">Es un atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-121">This is an optional attribute.</span></span> <span data-ttu-id="dcbf1-122">IDENTIFICADOR del sistema para el que se van a usar los datos de la clave.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="dcbf1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcbf1-123">Remarks</span></span>

<span data-ttu-id="dcbf1-124">Este evento se utiliza, por ejemplo, para el evento de rotación de claves de comunicación.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="dcbf1-125">En este caso, se debe enviar tan pronto como sea posible para dar tiempo al descodificador a la preparación antes de que lleguen los ejemplos cifrados con el nuevo ID. de clave.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbf1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcbf1-126">Requirements</span></span>



| <span data-ttu-id="dcbf1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcbf1-127">Requirement</span></span> | <span data-ttu-id="dcbf1-128">Value</span><span class="sxs-lookup"><span data-stu-id="dcbf1-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbf1-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcbf1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dcbf1-130">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="dcbf1-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dcbf1-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcbf1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dcbf1-132">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcbf1-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="dcbf1-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcbf1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcbf1-134"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcbf1-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbf1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcbf1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbf1-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dcbf1-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




