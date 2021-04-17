---
description: Especifica el estado de una topología durante la reproducción.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: MF_EVENT_TOPOLOGY_STATUS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697864"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="c3b9a-103">Atributo de estado de la \_ topología de eventos MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="c3b9a-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="c3b9a-104">Especifica el estado de una topología durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3b9a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c3b9a-105">Data type</span></span>

<span data-ttu-id="c3b9a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3b9a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b9a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3b9a-107">Remarks</span></span>

<span data-ttu-id="c3b9a-108">El valor de este atributo es un miembro de la enumeración [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .</span><span class="sxs-lookup"><span data-stu-id="c3b9a-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="c3b9a-109">Este atributo se usa con el evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="c3b9a-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="c3b9a-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b9a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3b9a-111">Requirements</span></span>



| <span data-ttu-id="c3b9a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3b9a-112">Requirement</span></span> | <span data-ttu-id="c3b9a-113">Value</span><span class="sxs-lookup"><span data-stu-id="c3b9a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b9a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3b9a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b9a-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3b9a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3b9a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3b9a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b9a-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3b9a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c3b9a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3b9a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3b9a-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3b9a-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b9a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3b9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b9a-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3b9a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3b9a-122">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="c3b9a-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3b9a-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c3b9a-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c3b9a-124">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c3b9a-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




