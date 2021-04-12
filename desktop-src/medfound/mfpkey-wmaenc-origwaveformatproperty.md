---
description: Especifica la estructura WAVEFORMATEX que describe el contenido de audio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Propiedad MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276227"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="0e8bc-103">\_ \_ Propiedad ORIGWAVEFORMAT de MFPKEY WMAENC</span><span class="sxs-lookup"><span data-stu-id="0e8bc-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="0e8bc-104">Especifica la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que describe el contenido de audio de entrada.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0e8bc-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0e8bc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0e8bc-106">g \_ wszWMACOriginalWaveFormat</span><span class="sxs-lookup"><span data-stu-id="0e8bc-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="0e8bc-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0e8bc-107">Data Type</span></span>

<span data-ttu-id="0e8bc-108">VT \_ array \| VT \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como una matriz de bytes)</span><span class="sxs-lookup"><span data-stu-id="0e8bc-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="0e8bc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e8bc-109">Remarks</span></span>

<span data-ttu-id="0e8bc-110">Al transcodificar contenido basado en Windows Media Audio a una velocidad de bits más baja, puede pasar la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenido al códec para permitir que el códec optimice sus algoritmos.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="0e8bc-111">Esta característica, denominada recompresión inteligente, proporciona mejores resultados que descomprimir el contenido y, a continuación, volver a alimentar los ejemplos de PCM reconstruidos a través del códec.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="0e8bc-112">Al pasar la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , incluya cualquier byte adicional al final de la estructura especificada por **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="0e8bc-113">El codificador de audio solo acepta entradas y salidas para las que el número de canales, bits por muestra y velocidad de muestreo son idénticos.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="0e8bc-114">Puede transcodificar contenido solo a una velocidad de bits menor dentro de esos parámetros.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="0e8bc-115">En cualquier caso, debe descodificar el contenido y pasar los ejemplos sin comprimir como entrada al codificador.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="0e8bc-116">Al establecer esta propiedad, se proporciona al codificador alguna información sobre el procesamiento que ya se ha realizado en el contenido.</span><span class="sxs-lookup"><span data-stu-id="0e8bc-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e8bc-117">Requirements</span></span>



| <span data-ttu-id="0e8bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e8bc-118">Requirement</span></span> | <span data-ttu-id="0e8bc-119">Value</span><span class="sxs-lookup"><span data-stu-id="0e8bc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8bc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e8bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8bc-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0e8bc-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0e8bc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e8bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8bc-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e8bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e8bc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e8bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e8bc-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e8bc-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e8bc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e8bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8bc-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e8bc-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
