---
description: Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.
ms.assetid: 438938fe-37e7-45d6-b49a-d96698307f25
title: GUID de seguimiento (PerfStruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AUDIOBREAK
- GUID_DSHOW_CTL
- GUID_STREAMTRACE
- GUID_VIDEOREND
api_type:
- HeaderDef
api_location:
- PerfStruct.h
ms.openlocfilehash: 4b2f2a6a678c029d01d9bf55481837d81d48557e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671433"
---
# <a name="trace-guids"></a><span data-ttu-id="e8f4e-103">GUID de seguimiento</span><span class="sxs-lookup"><span data-stu-id="e8f4e-103">Trace GUIDs</span></span>

<span data-ttu-id="e8f4e-104">Los siguientes GUID se usan para el seguimiento de eventos en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-104">The following GUIDs are used for event tracing in DirectShow.</span></span>



| <span data-ttu-id="e8f4e-105">GUID</span><span class="sxs-lookup"><span data-stu-id="e8f4e-105">GUID</span></span>                                                                                                                                                                   | <span data-ttu-id="e8f4e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8f4e-106">Description</span></span>                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AUDIOBREAK"></span><span id="guid_audiobreak"></span><dl> <span data-ttu-id="e8f4e-107"><dt>**GUID \_ AUDIOBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8f4e-107"><dt>**GUID\_AUDIOBREAK**</dt></span></span> </dl>    | <span data-ttu-id="e8f4e-108">Evento de interrupción de audio.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-108">Audio break event.</span></span> <span data-ttu-id="e8f4e-109">Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ AUDIOBREAK**](perfinfo-dshow-audiobreak.md) para los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-109">Events of this type use the [**PERFINFO\_DSHOW\_AUDIOBREAK**](perfinfo-dshow-audiobreak.md) structure for event data.</span></span><br/>         |
| <span id="GUID_DSHOW_CTL"></span><span id="guid_dshow_ctl"></span><dl> <span data-ttu-id="e8f4e-110"><dt>**CTL del GUID de \_ DSHOW \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e8f4e-110"><dt>**GUID\_DSHOW\_CTL**</dt></span></span> </dl>      | <span data-ttu-id="e8f4e-111">Proveedor de eventos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-111">DirectShow event provider.</span></span><br/>                                                                                                                        |
| <span id="GUID_STREAMTRACE"></span><span id="guid_streamtrace"></span><dl> <span data-ttu-id="e8f4e-112"><dt>**GUID \_ STREAMTRACE**</dt></span><span class="sxs-lookup"><span data-stu-id="e8f4e-112"><dt>**GUID\_STREAMTRACE**</dt></span></span> </dl> | <span data-ttu-id="e8f4e-113">Evento general de streaming.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-113">General streaming event.</span></span> <span data-ttu-id="e8f4e-114">Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ STREAMTRACE**](perfinfo-dshow-streamtrace.md) para los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-114">Events of this type use the [**PERFINFO\_DSHOW\_STREAMTRACE**](perfinfo-dshow-streamtrace.md) structure for event data.</span></span><br/> |
| <span id="GUID_VIDEOREND"></span><span id="guid_videorend"></span><dl> <span data-ttu-id="e8f4e-115"><dt>**GUID \_ VIDEOREND**</dt></span><span class="sxs-lookup"><span data-stu-id="e8f4e-115"><dt>**GUID\_VIDEOREND**</dt></span></span> </dl>       | <span data-ttu-id="e8f4e-116">Evento de representación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-116">Video rendering event.</span></span> <span data-ttu-id="e8f4e-117">Los eventos de este tipo usan la estructura [**PERFINFO de \_ DSHOW \_ AVREND**](perfinfo-dshow-avrend.md) para los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="e8f4e-117">Events of this type use the [**PERFINFO\_DSHOW\_AVREND**](perfinfo-dshow-avrend.md) structure for event data.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="e8f4e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8f4e-118">Requirements</span></span>



| <span data-ttu-id="e8f4e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8f4e-119">Requirement</span></span> | <span data-ttu-id="e8f4e-120">Value</span><span class="sxs-lookup"><span data-stu-id="e8f4e-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f4e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8f4e-121">Header</span></span><br/> | <dl> <span data-ttu-id="e8f4e-122"><dt>PerfStruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8f4e-122"><dt>PerfStruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8f4e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8f4e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f4e-124">Seguimiento de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8f4e-124">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> </dl>

 

 




