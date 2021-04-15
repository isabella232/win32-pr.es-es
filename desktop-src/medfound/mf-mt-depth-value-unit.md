---
description: Valor que define las unidades de un valor de profundidad en un fotograma de vídeo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715649"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="163c2-103">\_Atributo de \_ unidad de valor de profundidad MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="163c2-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="163c2-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="163c2-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="163c2-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="163c2-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="163c2-106">Valor que define las unidades de un valor de profundidad en un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="163c2-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="163c2-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="163c2-107">Data type</span></span>

<span data-ttu-id="163c2-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="163c2-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="163c2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="163c2-109">Remarks</span></span>

<span data-ttu-id="163c2-110">El valor de unidad es un valor UINT64 en nanometros, en el intervalo 1E-9 metros.</span><span class="sxs-lookup"><span data-stu-id="163c2-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="163c2-111">Si este valor no está presente, el valor predeterminado de la unidad es 1E-3, lo que indica que cada nivel de píxel se mide en 1 milímetro en el espacio físico.</span><span class="sxs-lookup"><span data-stu-id="163c2-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="163c2-112">Las cámaras de profundidad no pueden detectar la profundidad de todos los píxeles.</span><span class="sxs-lookup"><span data-stu-id="163c2-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="163c2-113">Cuando la confianza de un píxel es baja, debido a material, oclusión o fuera del intervalo, etc., el valor de profundidad en ese píxel puede ser no válido.</span><span class="sxs-lookup"><span data-stu-id="163c2-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="163c2-114">Cuando un valor de píxel de profundidad es 0, el píxel no es válido.</span><span class="sxs-lookup"><span data-stu-id="163c2-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="163c2-115">Algunas cámaras de profundidad adjuntan metadatos de máscara de archivos para cada píxel, además del valor de profundidad, para representar la razón por la que la profundidad del píxel no es válida, debido a material, oclusión o fuera del intervalo, etc. Se recomienda evitar la Asociación de metadatos como bits en valor de profundidad, ya que normalmente dará lugar a dificultades al usar estos valores en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="163c2-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="163c2-116">En lugar.</span><span class="sxs-lookup"><span data-stu-id="163c2-116">Instead.</span></span> <span data-ttu-id="163c2-117">se recomienda usar un búfer de imagen 8 bits independiente con la misma resolución y adjuntarlo como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="163c2-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="163c2-118">Estos metadatos varían para cada proveedor de la cámara y no están estandarizados por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="163c2-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="163c2-119">Se recomienda usar 16 bits completos para el valor de profundidad a fin de facilitar el procesamiento de bajada y el uso de un valor fijo como 0 para la invalidación.</span><span class="sxs-lookup"><span data-stu-id="163c2-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="163c2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="163c2-120">Requirements</span></span>



| <span data-ttu-id="163c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="163c2-121">Requirement</span></span> | <span data-ttu-id="163c2-122">Value</span><span class="sxs-lookup"><span data-stu-id="163c2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="163c2-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="163c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="163c2-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="163c2-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="163c2-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="163c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="163c2-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="163c2-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="163c2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="163c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="163c2-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="163c2-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




