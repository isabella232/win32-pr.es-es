---
description: Tipo de evento desconocido. Puede usar este valor para inicializar variables de tipo MediaEventType, pero un componente nunca debe generar el evento MEUnknown.
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: Evento MEUnknown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a768fde2939b7e32ed8d1007d2988c2e54cc6726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001512"
---
# <a name="meunknown-event"></a><span data-ttu-id="3756e-104">Evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="3756e-104">MEUnknown event</span></span>

<span data-ttu-id="3756e-105">Tipo de evento desconocido.</span><span class="sxs-lookup"><span data-stu-id="3756e-105">Unknown event type.</span></span> <span data-ttu-id="3756e-106">Puede usar este valor para inicializar variables de tipo **MediaEventType**, pero un componente nunca debe generar el evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="3756e-106">You can use this value to initialize variables of type **MediaEventType**, but a component should never raise the MEUnknown event</span></span>

## <a name="event-values"></a><span data-ttu-id="3756e-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="3756e-107">Event values</span></span>

<span data-ttu-id="3756e-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3756e-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3756e-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3756e-109">VARTYPE</span></span>              | <span data-ttu-id="3756e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3756e-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3756e-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="3756e-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3756e-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="3756e-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3756e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3756e-113">Requirements</span></span>



| <span data-ttu-id="3756e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3756e-114">Requirement</span></span> | <span data-ttu-id="3756e-115">Value</span><span class="sxs-lookup"><span data-stu-id="3756e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3756e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3756e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3756e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3756e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3756e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3756e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3756e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3756e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3756e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3756e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3756e-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3756e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3756e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3756e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3756e-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3756e-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




