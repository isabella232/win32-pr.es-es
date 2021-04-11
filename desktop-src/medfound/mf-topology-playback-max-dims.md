---
description: Especifica el tamaño de la ventana de destino para la reproducción de vídeo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275942"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="62f54-103">Atributo de reproducción de la \_ topología MF \_ \_ Max \_ DiMS</span><span class="sxs-lookup"><span data-stu-id="62f54-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="62f54-104">Especifica el tamaño de la ventana de destino para la reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62f54-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="62f54-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62f54-105">Data type</span></span>

<span data-ttu-id="62f54-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="62f54-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="62f54-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="62f54-107">Get/set</span></span>

<span data-ttu-id="62f54-108">Para obtener este atributo, llame a [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="62f54-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="62f54-109">Para establecer este atributo, llame a [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span><span class="sxs-lookup"><span data-stu-id="62f54-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="62f54-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="62f54-110">Applies to</span></span>

[<span data-ttu-id="62f54-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="62f54-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="62f54-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62f54-112">Remarks</span></span>

<span data-ttu-id="62f54-113">El cargador de topología utiliza este atributo para optimizar la canalización antes de que se inicie la reproducción.</span><span class="sxs-lookup"><span data-stu-id="62f54-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="62f54-114">Si establece este atributo, establezca también el atributo [de \_ \_ \_ \_ optimizaciones de reproducción estática de la topología MF](mf-topology-static-playback-optimizations.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="62f54-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="62f54-115">Los 32 superiores del valor del atributo contienen el ancho y los bits inferiores 32 contienen el alto, ambos en píxeles.</span><span class="sxs-lookup"><span data-stu-id="62f54-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="62f54-116">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="62f54-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f54-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62f54-117">Requirements</span></span>



| <span data-ttu-id="62f54-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f54-118">Requirement</span></span> | <span data-ttu-id="62f54-119">Value</span><span class="sxs-lookup"><span data-stu-id="62f54-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62f54-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f54-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62f54-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="62f54-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="62f54-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f54-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62f54-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="62f54-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="62f54-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62f54-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f54-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f54-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f54-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="62f54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f54-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62f54-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62f54-128">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="62f54-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="62f54-129">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="62f54-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




