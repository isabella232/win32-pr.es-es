---
description: Contiene el subtipo de medio para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_TOPONODE_ERROR_SUBTYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715387"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="85cbe-104">\_Atributo de \_ subtipo de error MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="85cbe-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="85cbe-105">Contiene el subtipo de medio para un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="85cbe-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="85cbe-106">Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.</span><span class="sxs-lookup"><span data-stu-id="85cbe-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="85cbe-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="85cbe-107">Data type</span></span>

<span data-ttu-id="85cbe-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="85cbe-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="85cbe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85cbe-109">Remarks</span></span>

<span data-ttu-id="85cbe-110">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="85cbe-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="85cbe-111">El cargador de topología podría establecer el atributo.</span><span class="sxs-lookup"><span data-stu-id="85cbe-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="85cbe-112">Las aplicaciones normalmente leen este atributo pero no lo establecen.</span><span class="sxs-lookup"><span data-stu-id="85cbe-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="85cbe-113">Para obtener una lista de los valores posibles, consulte [GUID de tipo de medio](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="85cbe-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="85cbe-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="85cbe-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85cbe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85cbe-115">Requirements</span></span>



| <span data-ttu-id="85cbe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cbe-116">Requirement</span></span> | <span data-ttu-id="85cbe-117">Value</span><span class="sxs-lookup"><span data-stu-id="85cbe-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85cbe-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cbe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85cbe-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="85cbe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85cbe-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85cbe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85cbe-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="85cbe-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85cbe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85cbe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85cbe-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85cbe-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85cbe-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="85cbe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cbe-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85cbe-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85cbe-126">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="85cbe-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="85cbe-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="85cbe-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="85cbe-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="85cbe-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="85cbe-129">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="85cbe-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




