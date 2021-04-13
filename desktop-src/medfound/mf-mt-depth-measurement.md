---
description: Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564633"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="0fffb-103">\_Atributo de \_ medición de profundidad MF MT \_</span><span class="sxs-lookup"><span data-stu-id="0fffb-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="0fffb-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0fffb-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0fffb-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0fffb-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0fffb-106">Valor que define el sistema de medida para un valor de profundidad en un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0fffb-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="0fffb-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0fffb-107">Data type</span></span>

<span data-ttu-id="0fffb-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0fffb-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0fffb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fffb-109">Remarks</span></span>

<span data-ttu-id="0fffb-110">Este valor es un miembro de la enumeración [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)</span><span class="sxs-lookup"><span data-stu-id="0fffb-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="0fffb-111">Si este atributo no está presente, se supone que es **DistanceToFocalPlane**.</span><span class="sxs-lookup"><span data-stu-id="0fffb-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="0fffb-112">Normalmente, la distancia al plano focal es más fácil de consumir en un sistema de coordenadas euclidiana 3D.</span><span class="sxs-lookup"><span data-stu-id="0fffb-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![Ilustración de distancetofocalplane](images/distance-to-focal-plane.png)

<span data-ttu-id="0fffb-114">El formato de distancia al centro focal es normalmente datos sin procesar del sensor, como la hora de las cámaras de vuelo.</span><span class="sxs-lookup"><span data-stu-id="0fffb-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![Ilustración de distancetoopticalcenter](images/distance-to-optical-center.png)

<span data-ttu-id="0fffb-116">Las cámaras de profundidad no pueden detectar la profundidad de todos los píxeles.</span><span class="sxs-lookup"><span data-stu-id="0fffb-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="0fffb-117">Cuando la confianza de un píxel es baja, debido a material, oclusión o fuera del intervalo, etc., el valor de profundidad en ese píxel puede ser no válido.</span><span class="sxs-lookup"><span data-stu-id="0fffb-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="0fffb-118">Cuando un valor de píxel de profundidad es 0, el píxel no es válido.</span><span class="sxs-lookup"><span data-stu-id="0fffb-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="0fffb-119">Algunas cámaras de profundidad adjuntan metadatos de máscara de archivos para cada píxel, además del valor de profundidad, para representar la razón por la que la profundidad del píxel no es válida, debido a material, oclusión o fuera del intervalo, etc. Se recomienda evitar la Asociación de metadatos como bits en valor de profundidad, ya que normalmente dará lugar a dificultades al usar estos valores en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0fffb-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="0fffb-120">En lugar.</span><span class="sxs-lookup"><span data-stu-id="0fffb-120">Instead.</span></span> <span data-ttu-id="0fffb-121">se recomienda usar un búfer de imagen 8 bits independiente con la misma resolución y adjuntarlo como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="0fffb-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="0fffb-122">Estos metadatos varían para cada proveedor de la cámara y no están estandarizados por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0fffb-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="0fffb-123">Se recomienda usar 16 bits completos para el valor de profundidad a fin de facilitar el procesamiento de bajada y el uso de un valor fijo como 0 para la invalidación.</span><span class="sxs-lookup"><span data-stu-id="0fffb-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fffb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fffb-124">Requirements</span></span>



| <span data-ttu-id="0fffb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fffb-125">Requirement</span></span> | <span data-ttu-id="0fffb-126">Value</span><span class="sxs-lookup"><span data-stu-id="0fffb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fffb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fffb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0fffb-128">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fffb-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fffb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fffb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0fffb-130">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0fffb-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="0fffb-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fffb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fffb-132"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fffb-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




