---
description: Especifica el nivel de volumen máximo deseado del contenido de audio de salida.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: Propiedad MFPKEY_WMADRC_PEAKTARGET (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696894"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="db844-103">\_ \_ Propiedad PEAKTARGET de MFPKEY WMADRC</span><span class="sxs-lookup"><span data-stu-id="db844-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="db844-104">Especifica el nivel de volumen máximo deseado del contenido de audio de salida.</span><span class="sxs-lookup"><span data-stu-id="db844-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="db844-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="db844-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="db844-106">g \_ wszWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="db844-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="db844-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="db844-107">Data Type</span></span>

<span data-ttu-id="db844-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="db844-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="db844-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="db844-109">Default Value</span></span>

<span data-ttu-id="db844-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="db844-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="db844-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db844-111">Remarks</span></span>

<span data-ttu-id="db844-112">Puede establecer este valor en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="db844-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="db844-113">Si solicita un control de intervalo dinámico desde el descodificador cuando no se establece esta propiedad, el códec calculará un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="db844-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="db844-114">Use las propiedades [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) y [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) para calcular los valores adecuados para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="db844-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="db844-115">Para obtener más información sobre el control de intervalo dinámico, vea el artículo Web [Windows Media Audio características de códecs profesionales](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="db844-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="db844-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db844-116">Requirements</span></span>



| <span data-ttu-id="db844-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db844-117">Requirement</span></span> | <span data-ttu-id="db844-118">Value</span><span class="sxs-lookup"><span data-stu-id="db844-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db844-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db844-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db844-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="db844-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db844-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db844-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db844-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db844-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db844-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db844-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db844-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db844-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db844-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="db844-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db844-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db844-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
