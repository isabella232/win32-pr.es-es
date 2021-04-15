---
description: Especifica un ancho de marco intermedio para el vídeo codificado.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Propiedad MFPKEY_FORCEFRAMEWIDTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544918"
---
# <a name="mfpkey_forceframewidth-property"></a><span data-ttu-id="e6a3b-103">\_Propiedad FORCEFRAMEWIDTH de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="e6a3b-103">MFPKEY\_FORCEFRAMEWIDTH Property</span></span>

<span data-ttu-id="e6a3b-104">Especifica un ancho de marco intermedio para el vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="e6a3b-104">Specifies an intermediate frame width for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e6a3b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e6a3b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e6a3b-106">g \_ wszWMVCForceFrameWidth</span><span class="sxs-lookup"><span data-stu-id="e6a3b-106">g\_wszWMVCForceFrameWidth</span></span>

## <a name="data-type"></a><span data-ttu-id="e6a3b-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e6a3b-107">Data Type</span></span>

<span data-ttu-id="e6a3b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e6a3b-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a3b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6a3b-109">Remarks</span></span>

<span data-ttu-id="e6a3b-110">Puede establecer este valor y la propiedad [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) para obligar al codificador a codificar el flujo de vídeo con un tamaño de fotograma menor que los tamaños de fotogramas de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="e6a3b-110">You can set this value and the [MFPKEY\_FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="e6a3b-111">Al descodificar, el vídeo cambiará de tamaño a su resolución de entrada original.</span><span class="sxs-lookup"><span data-stu-id="e6a3b-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="e6a3b-112">Las dimensiones de fotogramas válidas en cualquiera de los ejes son de 2 a 8192 píxeles.</span><span class="sxs-lookup"><span data-stu-id="e6a3b-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="e6a3b-113">Las dimensiones del marco deben ser divisibles en 2.</span><span class="sxs-lookup"><span data-stu-id="e6a3b-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a3b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6a3b-114">Requirements</span></span>



| <span data-ttu-id="e6a3b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a3b-115">Requirement</span></span> | <span data-ttu-id="e6a3b-116">Value</span><span class="sxs-lookup"><span data-stu-id="e6a3b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a3b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6a3b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a3b-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a3b-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6a3b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6a3b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a3b-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a3b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6a3b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6a3b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a3b-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a3b-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a3b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6a3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a3b-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6a3b-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




