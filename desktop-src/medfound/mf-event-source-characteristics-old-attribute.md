---
description: Especifica las características anteriores del origen multimedia.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: MF_EVENT_SOURCE_CHARACTERISTICS_OLD atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659856"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="e338b-103">\_ \_ \_ Atributos anteriores de características de origen de eventos MF \_</span><span class="sxs-lookup"><span data-stu-id="e338b-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="e338b-104">Especifica las características anteriores del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="e338b-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="e338b-105">Los **datos de atributo son una operación OR** bit a bit de marcas de la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="e338b-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="e338b-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e338b-106">Data type</span></span>

<span data-ttu-id="e338b-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e338b-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e338b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e338b-108">Remarks</span></span>

<span data-ttu-id="e338b-109">Este atributo se usa con el evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e338b-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="e338b-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e338b-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e338b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e338b-111">Requirements</span></span>



| <span data-ttu-id="e338b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e338b-112">Requirement</span></span> | <span data-ttu-id="e338b-113">Value</span><span class="sxs-lookup"><span data-stu-id="e338b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e338b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e338b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e338b-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e338b-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e338b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e338b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e338b-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e338b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e338b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e338b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e338b-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e338b-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e338b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e338b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e338b-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e338b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e338b-122">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="e338b-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="e338b-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e338b-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e338b-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e338b-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e338b-125">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="e338b-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




