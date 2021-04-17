---
description: Especifica si el códec debe utilizar el filtro de desbloqueo en bucle durante la codificación.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: Propiedad MFPKEY_LOOPFILTER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696942"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="ddbeb-103">\_Propiedad LOOPFILTER de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ddbeb-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="ddbeb-104">Especifica si el códec debe utilizar el filtro de desbloqueo en bucle durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ddbeb-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ddbeb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ddbeb-106">g \_ wszWMVCLoopFilter</span><span class="sxs-lookup"><span data-stu-id="ddbeb-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="ddbeb-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ddbeb-107">Data Type</span></span>

<span data-ttu-id="ddbeb-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="ddbeb-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="ddbeb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddbeb-109">Remarks</span></span>

<span data-ttu-id="ddbeb-110">El filtro en bucle es un método de desbloqueo que se aplica durante la codificación y la descodificación, para reducir los artefactos de bloqueo en el tiempo de codificación ("en el bucle") para que los fotogramas futuros y los fotogramas B no los lleven hacia delante.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="ddbeb-111">El efecto de aplicar el filtro en bucle es que los bordes de los bloques de macros de los fotogramas de vídeo de salida son menos perceptibles.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="ddbeb-112">Al mismo tiempo, la imagen puede ser más blanda.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="ddbeb-113">Aunque el filtro en bucle puede dar lugar a un detalle de la imagen reducida en algunos fotogramas, la calidad general del vídeo resultará muy ventajosa.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="ddbeb-114">El mayor inconveniente de usar el filtrado en bucle es el costo de rendimiento de la descodificación adicional.</span><span class="sxs-lookup"><span data-stu-id="ddbeb-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbeb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddbeb-115">Requirements</span></span>



| <span data-ttu-id="ddbeb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbeb-116">Requirement</span></span> | <span data-ttu-id="ddbeb-117">Value</span><span class="sxs-lookup"><span data-stu-id="ddbeb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbeb-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbeb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbeb-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ddbeb-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ddbeb-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddbeb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbeb-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ddbeb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ddbeb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddbeb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddbeb-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddbeb-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbeb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddbeb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbeb-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ddbeb-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




