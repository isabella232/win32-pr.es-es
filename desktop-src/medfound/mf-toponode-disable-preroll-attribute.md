---
description: Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: MF_TOPONODE_DISABLE_PREROLL atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649239"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="a482b-103">MF \_ TOPONODE \_ deshabilitar \_ atributo de preroll</span><span class="sxs-lookup"><span data-stu-id="a482b-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="a482b-104">Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.</span><span class="sxs-lookup"><span data-stu-id="a482b-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="a482b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a482b-105">Data type</span></span>

<span data-ttu-id="a482b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a482b-106">**UINT32**</span></span>

<span data-ttu-id="a482b-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="a482b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a482b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a482b-108">Remarks</span></span>

<span data-ttu-id="a482b-109">Este atributo se aplica a los nodos de salida (**\_ nodo de \_ salida \_ de topología MF**).</span><span class="sxs-lookup"><span data-stu-id="a482b-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="a482b-110">Si el valor de este atributo es **true**, la sesión multimedia no revierte los datos en el receptor de medios, aunque el receptor de medios exponga la interfaz [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="a482b-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="a482b-111">Si el valor es **false**, la sesión multimedia preprocesa los datos si el receptor multimedia implementa **IMFMediaSinkPreroll**.</span><span class="sxs-lookup"><span data-stu-id="a482b-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="a482b-112">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a482b-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="a482b-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a482b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a482b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a482b-114">Requirements</span></span>



| <span data-ttu-id="a482b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a482b-115">Requirement</span></span> | <span data-ttu-id="a482b-116">Value</span><span class="sxs-lookup"><span data-stu-id="a482b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a482b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a482b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a482b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a482b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a482b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a482b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a482b-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a482b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a482b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a482b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a482b-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a482b-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a482b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a482b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a482b-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a482b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a482b-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a482b-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a482b-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a482b-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a482b-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a482b-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a482b-128">Atributos de nodo de topología</span><span class="sxs-lookup"><span data-stu-id="a482b-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




