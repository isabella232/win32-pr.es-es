---
description: La hora aproximada a la que la sesión multimedia generó un evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716492"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="84337-103">\_Atributo de \_ \_ tiempo de \_ repetición de evento \_ de sesión MF aprox.</span><span class="sxs-lookup"><span data-stu-id="84337-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="84337-104">La hora aproximada a la que la sesión multimedia generó un evento.</span><span class="sxs-lookup"><span data-stu-id="84337-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="84337-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="84337-105">Data type</span></span>

<span data-ttu-id="84337-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="84337-106">**UINT64**</span></span>

<span data-ttu-id="84337-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="84337-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84337-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84337-108">Remarks</span></span>

<span data-ttu-id="84337-109">Algunos eventos de la sesión multimedia tienen este atributo.</span><span class="sxs-lookup"><span data-stu-id="84337-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="84337-110">El valor proporciona el tiempo de presentación aproximado en que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="84337-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="84337-111">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="84337-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="84337-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="84337-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84337-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84337-113">Requirements</span></span>



| <span data-ttu-id="84337-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="84337-114">Requirement</span></span> | <span data-ttu-id="84337-115">Value</span><span class="sxs-lookup"><span data-stu-id="84337-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84337-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84337-116">Minimum supported client</span></span><br/> | <span data-ttu-id="84337-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="84337-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84337-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84337-118">Minimum supported server</span></span><br/> | <span data-ttu-id="84337-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="84337-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84337-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84337-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="84337-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="84337-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84337-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="84337-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84337-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84337-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84337-124">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="84337-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="84337-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="84337-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="84337-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="84337-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




