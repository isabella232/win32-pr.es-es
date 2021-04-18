---
description: Especifica las características actuales del origen de los medios.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: MF_EVENT_SOURCE_CHARACTERISTICS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659822"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="7c147-103">\_Atributo de \_ características del origen de eventos MF \_</span><span class="sxs-lookup"><span data-stu-id="7c147-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="7c147-104">Especifica las características actuales del origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="7c147-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c147-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7c147-105">Data type</span></span>

<span data-ttu-id="7c147-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7c147-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c147-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c147-107">Remarks</span></span>

<span data-ttu-id="7c147-108">El valor de este atributo es **una operación OR bit a bit** de marcas de la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="7c147-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="7c147-109">Este atributo se usa con el evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7c147-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="7c147-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7c147-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c147-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c147-111">Requirements</span></span>



| <span data-ttu-id="7c147-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c147-112">Requirement</span></span> | <span data-ttu-id="7c147-113">Value</span><span class="sxs-lookup"><span data-stu-id="7c147-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c147-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c147-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7c147-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7c147-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c147-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c147-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7c147-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c147-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c147-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c147-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c147-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c147-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c147-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c147-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c147-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c147-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c147-122">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="7c147-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c147-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7c147-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7c147-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7c147-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




