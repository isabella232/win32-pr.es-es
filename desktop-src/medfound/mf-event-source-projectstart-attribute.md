---
description: Especifica la hora de inicio de una topología de segmento.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: MF_EVENT_SOURCE_PROJECTSTART atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913734"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="f4a39-103">\_ \_ PROJECTSTART atributo de origen de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="f4a39-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="f4a39-104">Especifica la hora de inicio de una topología de segmento.</span><span class="sxs-lookup"><span data-stu-id="f4a39-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4a39-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f4a39-105">Data type</span></span>

<span data-ttu-id="f4a39-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f4a39-106">**UINT64**</span></span>

<span data-ttu-id="f4a39-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="f4a39-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4a39-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4a39-108">Remarks</span></span>

<span data-ttu-id="f4a39-109">Este atributo se usa con el evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a39-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="f4a39-110">El origen del secuenciador establece este atributo cuando la topología del segmento actual tiene el atributo [**\_ \_ PROJECTSTART de la topología MF**](mf-topology-projectstart-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a39-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="f4a39-111">Los dos atributos tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="f4a39-111">The two attributes have the same value.</span></span>

<span data-ttu-id="f4a39-112">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="f4a39-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="f4a39-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f4a39-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4a39-114">Requirements</span></span>



| <span data-ttu-id="f4a39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4a39-115">Requirement</span></span> | <span data-ttu-id="f4a39-116">Value</span><span class="sxs-lookup"><span data-stu-id="f4a39-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a39-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4a39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a39-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4a39-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4a39-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4a39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a39-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4a39-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4a39-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4a39-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a39-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a39-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4a39-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4a39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a39-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4a39-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4a39-125">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="f4a39-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4a39-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f4a39-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f4a39-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f4a39-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




