---
description: Contiene un puntero al descriptor de presentación para el origen de medios.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: MF_TOPONODE_PRESENTATION_DESCRIPTOR atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811018"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="3552f-103">\_Atributo de \_ descriptor de presentación MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="3552f-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="3552f-104">Contiene un puntero al descriptor de presentación para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="3552f-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="3552f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3552f-105">Data type</span></span>

<span data-ttu-id="3552f-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="3552f-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3552f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3552f-107">Remarks</span></span>

<span data-ttu-id="3552f-108">Este atributo se aplica a los nodos de origen (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="3552f-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="3552f-109">El valor del atributo es un puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="3552f-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="3552f-110">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="3552f-110">This attribute is required.</span></span>

<span data-ttu-id="3552f-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3552f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3552f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3552f-112">Requirements</span></span>



| <span data-ttu-id="3552f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3552f-113">Requirement</span></span> | <span data-ttu-id="3552f-114">Value</span><span class="sxs-lookup"><span data-stu-id="3552f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3552f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3552f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3552f-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3552f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3552f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3552f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3552f-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3552f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3552f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3552f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3552f-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3552f-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3552f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3552f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3552f-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3552f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3552f-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="3552f-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="3552f-124">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="3552f-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="3552f-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3552f-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3552f-126">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3552f-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




