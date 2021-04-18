---
description: Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Propiedad MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648305"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="c23f9-103">\_Propiedad NUMBFRAMES de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c23f9-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="c23f9-104">Especifica el número de fotogramas predictivos bidireccionales (fotogramas B).</span><span class="sxs-lookup"><span data-stu-id="c23f9-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c23f9-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c23f9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c23f9-106">g \_ wszWMVCNumBFrames</span><span class="sxs-lookup"><span data-stu-id="c23f9-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="c23f9-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c23f9-107">Data Type</span></span>

<span data-ttu-id="c23f9-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="c23f9-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c23f9-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c23f9-109">Default Value</span></span>

<span data-ttu-id="c23f9-110">0</span><span class="sxs-lookup"><span data-stu-id="c23f9-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="c23f9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c23f9-111">Remarks</span></span>

<span data-ttu-id="c23f9-112">De forma predeterminada, Windows Media Video 9 solo utiliza intragramas (fotogramas I), también conocidos como fotogramas clave o fotogramas delimitadores, que son fotogramas totalmente codificados, y marcos de predicción (fotogramas P), que se codifican como una diferencia respecto del fotograma I anterior.</span><span class="sxs-lookup"><span data-stu-id="c23f9-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="c23f9-113">Los fotogramas B son diferentes de los fotogramas P porque almacenan las diferencias con respecto al fotograma anterior y las diferencias con el siguiente fotograma.</span><span class="sxs-lookup"><span data-stu-id="c23f9-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="c23f9-114">Al configurar el códec para que use fotogramas B, usará el número especificado de fotogramas B entre cada par de fotogramas de tipo I o P.</span><span class="sxs-lookup"><span data-stu-id="c23f9-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="c23f9-115">Por ejemplo, si una secuencia de marcos sin fotogramas B es "IPPPPPPPPI", la misma codificación de secuencia con dos fotogramas B sería "IBBPBBPBBI".</span><span class="sxs-lookup"><span data-stu-id="c23f9-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="c23f9-116">Para la mayoría del contenido, uno o dos fotogramas B son adecuados.</span><span class="sxs-lookup"><span data-stu-id="c23f9-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="c23f9-117">Con una velocidad de datos superior, un fotograma B suele ser la opción óptima.</span><span class="sxs-lookup"><span data-stu-id="c23f9-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="c23f9-118">Tres o más no suelen ser útiles.</span><span class="sxs-lookup"><span data-stu-id="c23f9-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="c23f9-119">El intervalo válido de valores para esta propiedad es de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="c23f9-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="c23f9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c23f9-120">Requirements</span></span>



| <span data-ttu-id="c23f9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c23f9-121">Requirement</span></span> | <span data-ttu-id="c23f9-122">Value</span><span class="sxs-lookup"><span data-stu-id="c23f9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c23f9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c23f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c23f9-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c23f9-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c23f9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c23f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c23f9-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c23f9-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c23f9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c23f9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c23f9-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c23f9-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c23f9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c23f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c23f9-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c23f9-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




