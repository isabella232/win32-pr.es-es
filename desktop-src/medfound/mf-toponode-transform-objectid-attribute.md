---
description: Identificador de clase (CLSID) de la transformación de Media Foundation (MFT) asociada a este nodo de topología.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543251"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="b165f-103">MF \_ TOPONODE \_ Transform \_ atributo objectId</span><span class="sxs-lookup"><span data-stu-id="b165f-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="b165f-104">Identificador de clase (CLSID) de la transformación de Media Foundation (MFT) asociada a este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="b165f-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b165f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b165f-105">Data type</span></span>

<span data-ttu-id="b165f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b165f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b165f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b165f-107">Remarks</span></span>

<span data-ttu-id="b165f-108">Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="b165f-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="b165f-109">Las aplicaciones pueden utilizar este atributo para inicializar un nodo transfrom.</span><span class="sxs-lookup"><span data-stu-id="b165f-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="b165f-110">Si establece este atributo, no tiene que llamar a [**IMFTopologyNode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) con un puntero a un objeto MFT o de activación.</span><span class="sxs-lookup"><span data-stu-id="b165f-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="b165f-111">Por el contrario, si llama a **SetObject**, no es necesario establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="b165f-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="b165f-112">Para obtener más información, consulte [crear topologías](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b165f-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="b165f-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b165f-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b165f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b165f-114">Requirements</span></span>



| <span data-ttu-id="b165f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b165f-115">Requirement</span></span> | <span data-ttu-id="b165f-116">Value</span><span class="sxs-lookup"><span data-stu-id="b165f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b165f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b165f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b165f-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b165f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b165f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b165f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b165f-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b165f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b165f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b165f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b165f-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b165f-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b165f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b165f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b165f-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b165f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b165f-125">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="b165f-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b165f-126">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="b165f-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b165f-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b165f-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b165f-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b165f-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b165f-129">Crear topologías</span><span class="sxs-lookup"><span data-stu-id="b165f-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="b165f-130">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="b165f-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




