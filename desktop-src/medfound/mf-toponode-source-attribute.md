---
description: Contiene un puntero al origen multimedia asociado a un nodo de topología.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: MF_TOPONODE_SOURCE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543254"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="e58ee-103">\_Atributo de \_ origen MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="e58ee-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="e58ee-104">Contiene un puntero al origen multimedia asociado a un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="e58ee-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e58ee-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e58ee-105">Data type</span></span>

<span data-ttu-id="e58ee-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e58ee-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="e58ee-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e58ee-107">Remarks</span></span>

<span data-ttu-id="e58ee-108">Este atributo se aplica a los nodos de origen (_ \* MF \_ Topology \_ SOURCESTREAM \_ node \* \*).</span><span class="sxs-lookup"><span data-stu-id="e58ee-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="e58ee-109">El valor del atributo es un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="e58ee-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="e58ee-110">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="e58ee-110">This attribute is required.</span></span>

<span data-ttu-id="e58ee-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e58ee-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58ee-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58ee-112">Requirements</span></span>



| <span data-ttu-id="e58ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58ee-113">Requirement</span></span> | <span data-ttu-id="e58ee-114">Value</span><span class="sxs-lookup"><span data-stu-id="e58ee-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e58ee-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e58ee-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e58ee-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e58ee-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e58ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e58ee-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e58ee-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e58ee-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e58ee-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58ee-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58ee-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58ee-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e58ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58ee-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e58ee-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e58ee-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="e58ee-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="e58ee-124">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="e58ee-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="e58ee-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e58ee-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e58ee-126">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="e58ee-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




