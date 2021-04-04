---
description: Especifica si el códec usará la optimización del escalado de vídeo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Propiedad MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908657"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="e8e3d-103">MFPKEY \_ propiedad de VIDEOescalación</span><span class="sxs-lookup"><span data-stu-id="e8e3d-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="e8e3d-104">Especifica si el códec usará la optimización del escalado de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e8e3d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e8e3d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e8e3d-106">g \_ wszWMVCVideoScaling</span><span class="sxs-lookup"><span data-stu-id="e8e3d-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="e8e3d-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e8e3d-107">Data Type</span></span>

<span data-ttu-id="e8e3d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e8e3d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e8e3d-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="e8e3d-109">Default Value</span></span>

<span data-ttu-id="e8e3d-110">0</span><span class="sxs-lookup"><span data-stu-id="e8e3d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e3d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8e3d-111">Remarks</span></span>

<span data-ttu-id="e8e3d-112">El escalado de vídeo es un tipo de optimización perceptual que puede mejorar la calidad visual del vídeo codificado a velocidades de bits bajas.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="e8e3d-113">La optimización del escalado de vídeo reduce los artefactos pronunciados, pero puede sacrificar los detalles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="e8e3d-114">Esta optimización afecta al intervalo de luminancia del vídeo codificado como se describe a continuación, pero no afecta a la resolución física del vídeo de salida.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="e8e3d-115">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="e8e3d-116">Value</span><span class="sxs-lookup"><span data-stu-id="e8e3d-116">Value</span></span> | <span data-ttu-id="e8e3d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8e3d-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e3d-118">0</span><span class="sxs-lookup"><span data-stu-id="e8e3d-118">0</span></span>     | <span data-ttu-id="e8e3d-119">No se usará el escalado de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="e8e3d-120">1</span><span class="sxs-lookup"><span data-stu-id="e8e3d-120">1</span></span>     | <span data-ttu-id="e8e3d-121">El codificador usará la optimización del escalado de vídeo conservador.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="e8e3d-122">El intervalo de luminancia se escalará desde 0... 255 hasta 26... 229.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="e8e3d-123">2</span><span class="sxs-lookup"><span data-stu-id="e8e3d-123">2</span></span>     | <span data-ttu-id="e8e3d-124">El codificador usará una optimización de escalado de vídeo agresiva.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="e8e3d-125">El intervalo de luminancia se escalará de 0... 255 a 31... 224.</span><span class="sxs-lookup"><span data-stu-id="e8e3d-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e8e3d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8e3d-126">Requirements</span></span>



| <span data-ttu-id="e8e3d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8e3d-127">Requirement</span></span> | <span data-ttu-id="e8e3d-128">Value</span><span class="sxs-lookup"><span data-stu-id="e8e3d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e3d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e3d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e3d-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e3d-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e8e3d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8e3d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e3d-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e3d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8e3d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e3d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e3d-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e3d-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e3d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e3d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e3d-136">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8e3d-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




