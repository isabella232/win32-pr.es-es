---
description: Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita el ligero. Para obtener una definición de simplificación, vea about Rate control.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: MF_EVENT_DO_THINNING atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001262"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="4bd6b-104">\_Atributo de \_ \_ refinamiento de evento MF</span><span class="sxs-lookup"><span data-stu-id="4bd6b-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="4bd6b-105">Cuando un origen multimedia solicita una nueva velocidad de reproducción, este atributo especifica si el origen también solicita el ligero.</span><span class="sxs-lookup"><span data-stu-id="4bd6b-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="4bd6b-106">Para obtener una definición de simplificación, vea [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6b-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="4bd6b-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4bd6b-107">Data type</span></span>

<span data-ttu-id="4bd6b-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4bd6b-108">**UINT32**</span></span>

<span data-ttu-id="4bd6b-109">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="4bd6b-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd6b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bd6b-110">Remarks</span></span>

<span data-ttu-id="4bd6b-111">Este atributo se usa con el evento [MESourceRateChangeRequested](mesourceratechangerequested.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd6b-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="4bd6b-112">Si el valor es **true**, el origen de medios solicita un cambio a la reproducción simplificada.</span><span class="sxs-lookup"><span data-stu-id="4bd6b-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="4bd6b-113">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4bd6b-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="4bd6b-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4bd6b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd6b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bd6b-115">Requirements</span></span>



| <span data-ttu-id="4bd6b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd6b-116">Requirement</span></span> | <span data-ttu-id="4bd6b-117">Value</span><span class="sxs-lookup"><span data-stu-id="4bd6b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd6b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bd6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd6b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bd6b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4bd6b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bd6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd6b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bd6b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4bd6b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bd6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bd6b-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bd6b-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd6b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bd6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd6b-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4bd6b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4bd6b-126">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="4bd6b-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4bd6b-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4bd6b-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4bd6b-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4bd6b-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




