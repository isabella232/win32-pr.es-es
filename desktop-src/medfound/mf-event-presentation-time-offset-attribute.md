---
description: Desplazamiento entre el tiempo de presentación y las marcas de tiempo de los orígenes de medios.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: MF_EVENT_PRESENTATION_TIME_OFFSET atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908145"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="ffe45-103">\_Atributo de \_ desplazamiento de tiempo de presentación de eventos MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffe45-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="ffe45-104">Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="ffe45-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffe45-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ffe45-105">Data type</span></span>

<span data-ttu-id="ffe45-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ffe45-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe45-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffe45-107">Remarks</span></span>

<span data-ttu-id="ffe45-108">El desplazamiento se calcula de la siguiente manera: desplazamiento = tiempo de presentación − hora de origen.</span><span class="sxs-lookup"><span data-stu-id="ffe45-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="ffe45-109">Este atributo se utiliza con los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="ffe45-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="ffe45-110">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="ffe45-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="ffe45-111">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="ffe45-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="ffe45-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ffe45-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe45-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffe45-113">Requirements</span></span>



| <span data-ttu-id="ffe45-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffe45-114">Requirement</span></span> | <span data-ttu-id="ffe45-115">Value</span><span class="sxs-lookup"><span data-stu-id="ffe45-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe45-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffe45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe45-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ffe45-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ffe45-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffe45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe45-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffe45-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ffe45-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffe45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffe45-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe45-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe45-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffe45-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe45-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffe45-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffe45-124">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="ffe45-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffe45-125">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ffe45-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="ffe45-126">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="ffe45-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




