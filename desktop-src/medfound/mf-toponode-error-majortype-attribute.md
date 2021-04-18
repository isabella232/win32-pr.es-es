---
description: Contiene el tipo de medio principal para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: MF_TOPONODE_ERROR_MAJORTYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715388"
---
# <a name="mf_toponode_error_majortype-attribute"></a><span data-ttu-id="a6baa-104">\_TOPONODE \_ error \_ MAJORTYPE de MF</span><span class="sxs-lookup"><span data-stu-id="a6baa-104">MF\_TOPONODE\_ERROR\_MAJORTYPE attribute</span></span>

<span data-ttu-id="a6baa-105">Contiene el tipo de medio principal para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="a6baa-105">Contains the major media type for a topology node.</span></span> <span data-ttu-id="a6baa-106">Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.</span><span class="sxs-lookup"><span data-stu-id="a6baa-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6baa-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a6baa-107">Data type</span></span>

<span data-ttu-id="a6baa-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a6baa-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a6baa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6baa-109">Remarks</span></span>

<span data-ttu-id="a6baa-110">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="a6baa-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="a6baa-111">El cargador de topología podría establecer el atributo.</span><span class="sxs-lookup"><span data-stu-id="a6baa-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="a6baa-112">Las aplicaciones normalmente leen este atributo pero no lo establecen.</span><span class="sxs-lookup"><span data-stu-id="a6baa-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="a6baa-113">Para obtener una lista de los valores posibles, consulte [tipos de medios principales](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a6baa-113">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="a6baa-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a6baa-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6baa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6baa-115">Requirements</span></span>



| <span data-ttu-id="a6baa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6baa-116">Requirement</span></span> | <span data-ttu-id="a6baa-117">Value</span><span class="sxs-lookup"><span data-stu-id="a6baa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6baa-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6baa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6baa-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6baa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6baa-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6baa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6baa-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6baa-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6baa-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6baa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6baa-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6baa-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6baa-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6baa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6baa-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6baa-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6baa-126">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="a6baa-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a6baa-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a6baa-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a6baa-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a6baa-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a6baa-129">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="a6baa-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




