---
description: Especifica si la transformación asociada a un nodo de topología admite la aceleración de vídeo de DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498112"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="6d8f7-103">\_ \_ Atributo D3DAWARE de MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="6d8f7-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="6d8f7-104">Especifica si la transformación asociada a un nodo de topología admite la aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="6d8f7-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="6d8f7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6d8f7-105">Data type</span></span>

<span data-ttu-id="6d8f7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6d8f7-106">**UINT32**</span></span>

<span data-ttu-id="6d8f7-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8f7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d8f7-108">Remarks</span></span>

<span data-ttu-id="6d8f7-109">Este atributo se aplica a los nodos de transformación (**\_ nodo de \_ transformación \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="6d8f7-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="6d8f7-110">Normalmente, las aplicaciones no usan este atributo directamente.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="6d8f7-111">La sesión de medios establece este atributo en un nodo de transformación si la transformación de Media Foundation subyacente tiene el atributo [**MF \_ \_ \_ compatible**](mf-sa-d3d-aware-attribute.md) con el D3D de la SA.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="6d8f7-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6d8f7-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8f7-113">Requirements</span></span>



| <span data-ttu-id="6d8f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8f7-114">Requirement</span></span> | <span data-ttu-id="6d8f7-115">Value</span><span class="sxs-lookup"><span data-stu-id="6d8f7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8f7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8f7-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d8f7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d8f7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8f7-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d8f7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d8f7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d8f7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d8f7-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8f7-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8f7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d8f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8f7-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d8f7-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d8f7-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6d8f7-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6d8f7-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6d8f7-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6d8f7-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="6d8f7-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="6d8f7-127">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="6d8f7-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




