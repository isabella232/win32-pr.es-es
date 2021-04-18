---
description: Especifica si el receptor de medios asociado a este nodo de topología tiene un número inestable.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715378"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="a28aa-103">\_Atributo sin \_ velocidad MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="a28aa-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="a28aa-104">Especifica si el receptor de medios asociado a este nodo de topología tiene un número inestable.</span><span class="sxs-lookup"><span data-stu-id="a28aa-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="a28aa-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a28aa-105">Data type</span></span>

<span data-ttu-id="a28aa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a28aa-106">**UINT32**</span></span>

<span data-ttu-id="a28aa-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="a28aa-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28aa-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a28aa-108">Remarks</span></span>

<span data-ttu-id="a28aa-109">Este atributo se aplica a los nodos de salida (**\_ nodo de \_ salida \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="a28aa-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="a28aa-110">Si el valor de este atributo es distinto de cero, la sesión multimedia trata al receptor de medios como un receptor sin velocidad, independientemente de si el receptor de medios devuelve la característica sin **\_ velocidad MEDIASINK** .</span><span class="sxs-lookup"><span data-stu-id="a28aa-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="a28aa-111">Si no se establece este atributo, se supone que el receptor de medios no tiene ninguna limitación.</span><span class="sxs-lookup"><span data-stu-id="a28aa-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="a28aa-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a28aa-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a28aa-113">Requirements</span></span>



| <span data-ttu-id="a28aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a28aa-114">Requirement</span></span> | <span data-ttu-id="a28aa-115">Value</span><span class="sxs-lookup"><span data-stu-id="a28aa-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a28aa-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a28aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a28aa-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a28aa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a28aa-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a28aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a28aa-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a28aa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a28aa-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a28aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28aa-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a28aa-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28aa-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a28aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28aa-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a28aa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a28aa-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a28aa-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a28aa-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a28aa-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a28aa-126">**IMFMediaSink::GetCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="a28aa-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="a28aa-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a28aa-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a28aa-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="a28aa-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




