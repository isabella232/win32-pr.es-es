---
description: La hora de inicio de la presentación, en unidades de 100-nanosegundos, según lo medido por el reloj de la presentación.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: MF_EVENT_START_PRESENTATION_TIME atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083481"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="d4d24-103">\_Atributo de \_ hora de presentación de inicio de evento MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="d4d24-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="d4d24-104">La hora de inicio de la presentación, en unidades de 100-nanosegundos, según lo medido por el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="d4d24-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4d24-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d4d24-105">Data type</span></span>

<span data-ttu-id="d4d24-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d4d24-106">**UINT64**</span></span>

<span data-ttu-id="d4d24-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="d4d24-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d24-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4d24-108">Remarks</span></span>

<span data-ttu-id="d4d24-109">Este atributo se usa con el evento [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d24-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="d4d24-110">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="d4d24-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="d4d24-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d4d24-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d24-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d24-112">Requirements</span></span>



| <span data-ttu-id="d4d24-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d24-113">Requirement</span></span> | <span data-ttu-id="d4d24-114">Value</span><span class="sxs-lookup"><span data-stu-id="d4d24-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d24-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d24-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d24-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d24-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d4d24-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d24-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d24-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d24-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d4d24-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4d24-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d24-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d24-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d24-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4d24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d24-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4d24-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4d24-123">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="d4d24-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4d24-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="d4d24-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="d4d24-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="d4d24-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




