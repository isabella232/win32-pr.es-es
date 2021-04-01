---
description: Especifica si la topología de segmento actual está vacía.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: MF_EVENT_SOURCE_FAKE_START atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913737"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="467e7-103">\_Atributo de \_ \_ Inicio falso de origen de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="467e7-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="467e7-104">Especifica si la topología de segmento actual está vacía.</span><span class="sxs-lookup"><span data-stu-id="467e7-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="467e7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="467e7-105">Data type</span></span>

<span data-ttu-id="467e7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="467e7-106">**UINT32**</span></span>

<span data-ttu-id="467e7-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="467e7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="467e7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="467e7-108">Remarks</span></span>

<span data-ttu-id="467e7-109">Este atributo se usa con el evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="467e7-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="467e7-110">El origen del secuenciador establece este atributo en **true** si la topología del segmento actual está vacía.</span><span class="sxs-lookup"><span data-stu-id="467e7-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="467e7-111">Si este atributo es **true**, la reproducción todavía no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="467e7-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="467e7-112">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="467e7-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="467e7-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="467e7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="467e7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="467e7-114">Requirements</span></span>



| <span data-ttu-id="467e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="467e7-115">Requirement</span></span> | <span data-ttu-id="467e7-116">Value</span><span class="sxs-lookup"><span data-stu-id="467e7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="467e7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="467e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="467e7-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="467e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="467e7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="467e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="467e7-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="467e7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="467e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="467e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="467e7-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="467e7-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="467e7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="467e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467e7-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="467e7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="467e7-125">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="467e7-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="467e7-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="467e7-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="467e7-127">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="467e7-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




