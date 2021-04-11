---
description: Especifica si el códec debe utilizar la optimización perceptual conservadora al codificar.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Propiedad MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276310"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="ba3ac-103">\_Propiedad PERCEPTUALOPTLEVEL de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ba3ac-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="ba3ac-104">Especifica si el códec debe utilizar la optimización perceptual conservadora al codificar.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ba3ac-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ba3ac-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ba3ac-106">g \_ wszWMVCPerceptualOptLevel</span><span class="sxs-lookup"><span data-stu-id="ba3ac-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="ba3ac-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ba3ac-107">Data Type</span></span>

<span data-ttu-id="ba3ac-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ba3ac-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ba3ac-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ba3ac-109">Default Value</span></span>

<span data-ttu-id="ba3ac-110">0</span><span class="sxs-lookup"><span data-stu-id="ba3ac-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="ba3ac-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba3ac-111">Remarks</span></span>

<span data-ttu-id="ba3ac-112">La optimización perceptual conservadora es un proceso por el cual el códec intenta identificar regiones "importantes" y "no importantes" en el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="ba3ac-113">Después de identificar estas regiones del fotograma, el códec dará una prioridad más alta a la calidad de las regiones importantes, a costa de la calidad de las regiones no importantes.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="ba3ac-114">La optimización perceptual hace hincapié en hacer que la imagen parezca correcta para el ojo humano en lugar de insistir en una precisión matemática estricta.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="ba3ac-115">Los resultados de la optimización variarán considerablemente según el tipo de vídeo que se está codificando.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="ba3ac-116">Esta característica puede ser adecuada para la codificación de baja velocidad y bajo nivel de bits (por ejemplo, transmisión por secuencias en Web), pero probablemente debe evitarse cuando se pretende tener una calidad de vídeo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ba3ac-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3ac-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba3ac-117">Requirements</span></span>



| <span data-ttu-id="ba3ac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba3ac-118">Requirement</span></span> | <span data-ttu-id="ba3ac-119">Value</span><span class="sxs-lookup"><span data-stu-id="ba3ac-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3ac-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3ac-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3ac-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ba3ac-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba3ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3ac-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba3ac-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba3ac-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba3ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba3ac-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba3ac-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba3ac-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba3ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3ac-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba3ac-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




