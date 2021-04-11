---
description: Especifica si un objeto de topología subyacente es un descodificador.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: MF_TOPONODE_DECODER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278921"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="09da4-103">\_Atributo de \_ descodificador MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="09da4-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="09da4-104">Especifica si el objeto subyacente de un nodo de topología es un descodificador.</span><span class="sxs-lookup"><span data-stu-id="09da4-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="09da4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="09da4-105">Data type</span></span>

<span data-ttu-id="09da4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="09da4-106">**UINT32**</span></span>

<span data-ttu-id="09da4-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="09da4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09da4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09da4-108">Remarks</span></span>

<span data-ttu-id="09da4-109">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="09da4-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="09da4-110">Si el valor de este atributo es distinto de cero, el objeto subyacente del nodo es un descodificador.</span><span class="sxs-lookup"><span data-stu-id="09da4-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="09da4-111">El cargador de topología establece este atributo cuando crea un nodo descodificador.</span><span class="sxs-lookup"><span data-stu-id="09da4-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="09da4-112">Una aplicación debe establecer este atributo si la aplicación agrega manualmente un descodificador a la topología.</span><span class="sxs-lookup"><span data-stu-id="09da4-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="09da4-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="09da4-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="09da4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09da4-114">Requirements</span></span>



| <span data-ttu-id="09da4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09da4-115">Requirement</span></span> | <span data-ttu-id="09da4-116">Value</span><span class="sxs-lookup"><span data-stu-id="09da4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09da4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09da4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09da4-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09da4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="09da4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09da4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09da4-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="09da4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09da4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09da4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09da4-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09da4-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09da4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="09da4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09da4-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09da4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09da4-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="09da4-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="09da4-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="09da4-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="09da4-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="09da4-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="09da4-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="09da4-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




