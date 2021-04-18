---
description: Contiene un puntero al descriptor de flujo para el origen de medios.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705793"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="5e75c-103">\_Atributo de \_ descriptor de secuencia MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="5e75c-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="5e75c-104">Contiene un puntero al descriptor de flujo para el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="5e75c-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e75c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5e75c-105">Data type</span></span>

<span data-ttu-id="5e75c-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="5e75c-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="5e75c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e75c-107">Remarks</span></span>

<span data-ttu-id="5e75c-108">Este atributo se aplica a los nodos de origen (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="5e75c-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="5e75c-109">El valor del atributo es un puntero a la interfaz [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) del descriptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="5e75c-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="5e75c-110">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5e75c-110">This attribute is required.</span></span>

<span data-ttu-id="5e75c-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5e75c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e75c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e75c-112">Requirements</span></span>



| <span data-ttu-id="5e75c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e75c-113">Requirement</span></span> | <span data-ttu-id="5e75c-114">Value</span><span class="sxs-lookup"><span data-stu-id="5e75c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e75c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e75c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5e75c-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e75c-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e75c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e75c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5e75c-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e75c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e75c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e75c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e75c-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e75c-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e75c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e75c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e75c-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e75c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e75c-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="5e75c-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="5e75c-124">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="5e75c-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="5e75c-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="5e75c-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="5e75c-126">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="5e75c-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




