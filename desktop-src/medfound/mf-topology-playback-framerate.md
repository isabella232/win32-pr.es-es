---
description: Especifica la frecuencia de actualización del monitor.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: MF_TOPOLOGY_PLAYBACK_FRAMERATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275943"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="564ee-103">Atributo de velocidad de reproducción de \_ topología MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="564ee-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="564ee-104">Especifica la frecuencia de actualización del monitor.</span><span class="sxs-lookup"><span data-stu-id="564ee-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="564ee-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="564ee-105">Data type</span></span>

<span data-ttu-id="564ee-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="564ee-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="564ee-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="564ee-107">Get/set</span></span>

<span data-ttu-id="564ee-108">Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="564ee-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="564ee-109">Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="564ee-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="564ee-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="564ee-110">Applies to</span></span>

[<span data-ttu-id="564ee-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="564ee-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="564ee-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="564ee-112">Remarks</span></span>

<span data-ttu-id="564ee-113">El cargador de topología utiliza este atributo para optimizar la canalización antes de que se inicie la reproducción.</span><span class="sxs-lookup"><span data-stu-id="564ee-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="564ee-114">Si establece este atributo, establezca también el atributo [de \_ \_ \_ \_ optimizaciones de reproducción estática de la topología MF](mf-topology-static-playback-optimizations.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="564ee-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="564ee-115">La velocidad de fotogramas se expresa como una proporción.</span><span class="sxs-lookup"><span data-stu-id="564ee-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="564ee-116">Los 32 superiores del valor del atributo contienen el numerador, y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="564ee-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="564ee-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="564ee-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="564ee-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="564ee-118">Requirements</span></span>



| <span data-ttu-id="564ee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="564ee-119">Requirement</span></span> | <span data-ttu-id="564ee-120">Value</span><span class="sxs-lookup"><span data-stu-id="564ee-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="564ee-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="564ee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="564ee-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="564ee-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="564ee-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="564ee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="564ee-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="564ee-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="564ee-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="564ee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="564ee-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="564ee-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="564ee-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="564ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="564ee-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="564ee-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="564ee-129">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="564ee-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="564ee-130">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="564ee-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




