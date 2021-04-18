---
description: Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Propiedad CODECAPI_AVEncMaxFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652355"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="f53af-103">\_Propiedad AVEncMaxFrameRate de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="f53af-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="f53af-104">Establece la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador.</span><span class="sxs-lookup"><span data-stu-id="f53af-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="f53af-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f53af-105">Data type</span></span>

<span data-ttu-id="f53af-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="f53af-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f53af-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="f53af-107">Property GUID</span></span>

<span data-ttu-id="f53af-108">**CODECAPI \_ AVEncMaxFrameRate**</span><span class="sxs-lookup"><span data-stu-id="f53af-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="f53af-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f53af-109">Remarks</span></span>

<span data-ttu-id="f53af-110">Esta propiedad permite al llamador especificar la velocidad de entrada máxima en tiempo real de los fotogramas de vídeo que se alimentan al codificador.</span><span class="sxs-lookup"><span data-stu-id="f53af-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="f53af-111">Esto proporciona al codificador una indicación de la frecuencia con la que será necesario procesar los fotogramas entrantes.</span><span class="sxs-lookup"><span data-stu-id="f53af-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="f53af-112">Esto resulta útil para los codificadores que se establecen en una configuración de estado de energía determinada en función de la resolución y la velocidad de fotogramas del vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="f53af-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="f53af-113">La velocidad de fotogramas se expresa como una proporción.</span><span class="sxs-lookup"><span data-stu-id="f53af-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="f53af-114">Los 32 superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="f53af-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="f53af-115">Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1.</span><span class="sxs-lookup"><span data-stu-id="f53af-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="f53af-116">Si la velocidad de fotogramas es 29,97 fps, la relación es 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="f53af-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="f53af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f53af-117">Requirements</span></span>



| <span data-ttu-id="f53af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f53af-118">Requirement</span></span> | <span data-ttu-id="f53af-119">Value</span><span class="sxs-lookup"><span data-stu-id="f53af-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f53af-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f53af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f53af-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f53af-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f53af-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f53af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f53af-123">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="f53af-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f53af-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f53af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f53af-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f53af-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f53af-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f53af-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f53af-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f53af-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f53af-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f53af-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

