---
description: Especifica el nivel de volumen medio deseado del contenido de audio de salida.
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: Propiedad MFPKEY_WMADRC_AVGTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4503161ac6e392a50fd7535592b84ea92d6136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276228"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a><span data-ttu-id="da77c-103">\_ \_ Propiedad AVGTARGET de MFPKEY WMADRC</span><span class="sxs-lookup"><span data-stu-id="da77c-103">MFPKEY\_WMADRC\_AVGTARGET Property</span></span>

<span data-ttu-id="da77c-104">Especifica el nivel de volumen medio deseado del contenido de audio de salida.</span><span class="sxs-lookup"><span data-stu-id="da77c-104">Specifies the desired average volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="da77c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="da77c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="da77c-106">g \_ wszWMADRCAverageTarget</span><span class="sxs-lookup"><span data-stu-id="da77c-106">g\_wszWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="da77c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="da77c-107">Data Type</span></span>

<span data-ttu-id="da77c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="da77c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="da77c-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="da77c-109">Default Value</span></span>

<span data-ttu-id="da77c-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="da77c-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="da77c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da77c-111">Remarks</span></span>

<span data-ttu-id="da77c-112">Puede establecer este valor en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="da77c-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

> [!Note]  
> <span data-ttu-id="da77c-113">No se recomienda establecer el valor de destino medio.</span><span class="sxs-lookup"><span data-stu-id="da77c-113">Setting the average target value is not recommended.</span></span> <span data-ttu-id="da77c-114">El ajuste del valor medio no afecta a la diferencia entre los sonidos fuertes y débiles.</span><span class="sxs-lookup"><span data-stu-id="da77c-114">Adjusting the average value does not affect the difference between loud and soft sounds.</span></span> <span data-ttu-id="da77c-115">En su lugar, corta o aumenta el volumen medio global, lo que puede provocar una distorsión no deseada durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="da77c-115">Instead, it cuts or boosts the overall average volume which may cause undesirable distortion during playback.</span></span>

 

<span data-ttu-id="da77c-116">Si solicita un control de intervalo dinámico desde el descodificador cuando no se establece esta propiedad, el códec calculará un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="da77c-116">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="da77c-117">Use las propiedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) y [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular los valores adecuados para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="da77c-117">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="da77c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da77c-118">Requirements</span></span>



| <span data-ttu-id="da77c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da77c-119">Requirement</span></span> | <span data-ttu-id="da77c-120">Value</span><span class="sxs-lookup"><span data-stu-id="da77c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da77c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da77c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da77c-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="da77c-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="da77c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da77c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da77c-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da77c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da77c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da77c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="da77c-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da77c-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da77c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="da77c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da77c-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da77c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




