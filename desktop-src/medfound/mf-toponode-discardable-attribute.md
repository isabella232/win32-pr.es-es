---
description: Especifica si la canalización puede quitar ejemplos de un nodo de topología.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: MF_TOPONODE_DISCARDABLE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720724"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="0a36a-103">MF \_ TOPONODE \_ descartable (atributo)</span><span class="sxs-lookup"><span data-stu-id="0a36a-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="0a36a-104">Especifica si la canalización puede quitar ejemplos de un nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="0a36a-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a36a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0a36a-105">Data type</span></span>

<span data-ttu-id="0a36a-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="0a36a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="0a36a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a36a-107">Remarks</span></span>

<span data-ttu-id="0a36a-108">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="0a36a-108">This attribute applies to all node types.</span></span> <span data-ttu-id="0a36a-109">Normalmente se establece este atributo en los nodos Tee para indicar que las salidas secundarias no son esenciales.</span><span class="sxs-lookup"><span data-stu-id="0a36a-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="0a36a-110">El valor del atributo es una matriz de índices para los flujos de salida del nodo.</span><span class="sxs-lookup"><span data-stu-id="0a36a-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="0a36a-111">Si se establece este atributo, la canalización podría quitar muestras de los flujos de salida especificados, si la secuencia está retrasada.</span><span class="sxs-lookup"><span data-stu-id="0a36a-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="0a36a-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0a36a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a36a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a36a-113">Requirements</span></span>



| <span data-ttu-id="0a36a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a36a-114">Requirement</span></span> | <span data-ttu-id="0a36a-115">Value</span><span class="sxs-lookup"><span data-stu-id="0a36a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a36a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a36a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0a36a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a36a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0a36a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a36a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0a36a-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a36a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0a36a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a36a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a36a-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a36a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a36a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a36a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a36a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a36a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a36a-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="0a36a-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="0a36a-125">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="0a36a-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="0a36a-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="0a36a-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="0a36a-127">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="0a36a-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




