---
description: Especifica si los tipos de medios se pueden cambiar en este nodo de topología.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: MF_TOPONODE_LOCKED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811024"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="e4756-103">MF \_ TOPONODE \_ atributo bloqueado</span><span class="sxs-lookup"><span data-stu-id="e4756-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="e4756-104">Especifica si los tipos de medios se pueden cambiar en este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="e4756-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4756-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e4756-105">Data type</span></span>

<span data-ttu-id="e4756-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e4756-106">**UINT32**</span></span>

<span data-ttu-id="e4756-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="e4756-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4756-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4756-108">Remarks</span></span>

<span data-ttu-id="e4756-109">Este atributo se aplica a todos los tipos de nodo.</span><span class="sxs-lookup"><span data-stu-id="e4756-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="e4756-110">Si el valor de este atributo es distinto de cero, el cargador de topología no cambiará los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="e4756-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="e4756-111">Este atributo se establece en **true** cuando el nodo está en uso.</span><span class="sxs-lookup"><span data-stu-id="e4756-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="e4756-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e4756-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4756-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4756-113">Requirements</span></span>



| <span data-ttu-id="e4756-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4756-114">Requirement</span></span> | <span data-ttu-id="e4756-115">Value</span><span class="sxs-lookup"><span data-stu-id="e4756-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4756-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4756-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e4756-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4756-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e4756-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4756-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e4756-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4756-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e4756-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4756-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4756-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4756-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4756-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4756-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4756-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4756-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e4756-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e4756-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e4756-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e4756-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e4756-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e4756-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e4756-127">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="e4756-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




