---
description: Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Propiedad MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715539"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="b7f69-103">\_Propiedad MFPKEY WMADEC \_ FOLDDOWN \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="b7f69-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="b7f69-104">Especifica los coeficientes de subconjuntos proporcionados por el autor para descodificar el audio multicanal para menos canales de los que contiene la secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="b7f69-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b7f69-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b7f69-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b7f69-106">g \_ wszWMACFoldDownXToYChannels</span><span class="sxs-lookup"><span data-stu-id="b7f69-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="b7f69-107">g \_ wszWMACFoldXToYChannelsZ</span><span class="sxs-lookup"><span data-stu-id="b7f69-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="b7f69-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b7f69-108">Data Type</span></span>

<span data-ttu-id="b7f69-109">**\_Matriz VT \| VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b7f69-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f69-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7f69-110">Remarks</span></span>

<span data-ttu-id="b7f69-111">Un descodificador de audio puede actuar como un objeto multimedia de DirectX (DMO) o como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="b7f69-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="b7f69-112">Para obtener información sobre cuándo un descodificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="b7f69-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="b7f69-113">Cuando se usa un descodificador como DMO, el descodificador puede realizar un repliegue de canal y se pueden enumerar los tipos de medios de salida plegados mediante una llamada a [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="b7f69-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="b7f69-114">Cuando se usa un descodificador como MFT, el descodificador de forma predeterminada no realizará ningún repliegue y no ofrecerá tipos de medios de salida plegados.</span><span class="sxs-lookup"><span data-stu-id="b7f69-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="b7f69-115">Un descodificador que actúe como MFT solo realizará un repliegue si los coeficientes de subconjunto personalizado se establecen mediante la propiedad de **\_ \_ \_ matriz MFPKEY WMADEC FOLDDOWN** .</span><span class="sxs-lookup"><span data-stu-id="b7f69-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="b7f69-116">Si la propiedad MFPKEY de la **\_ matriz de WMADEC \_ FOLDDOWN \_** no se establece en la MFT del descodificador de audio y desea realizar un repliegue, puede usar (como MFT) el procesador de señal digital de remuestreador de audio.</span><span class="sxs-lookup"><span data-stu-id="b7f69-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="b7f69-117">El valor de esta propiedad es una cadena que contiene coeficientes de repliegue en una lista separada por comas de valores enteros.</span><span class="sxs-lookup"><span data-stu-id="b7f69-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="b7f69-118">La lista debe contener un número de enteros para cada canal en el contenido codificado igual al número de canales en el contenido descodificado.</span><span class="sxs-lookup"><span data-stu-id="b7f69-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="b7f69-119">Si el coeficiente es cero, el valor que se va a utilizar en la cadena debe ser "-2147483648"; en caso contrario, el valor se calcula con la ecuación: 20 \* 65536 \* log10 (x).</span><span class="sxs-lookup"><span data-stu-id="b7f69-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="b7f69-120">Los coeficientes se enumeran en el orden de máscara de canal, tal como se define en las constantes de máscara de canal que se incluyen en el archivo de encabezado mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="b7f69-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="b7f69-121">Por lo tanto, los dos primeros valores de un subconjunto de canal de 6 a 2 representan las partes del canal de salida de la izquierda y el canal de salida derecho que se compone del canal izquierdo central en el flujo de 6 canales.</span><span class="sxs-lookup"><span data-stu-id="b7f69-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="b7f69-122">Debe establecer esta propiedad solo si los valores de plegamiento proporcionados por el autor se conservan con el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="b7f69-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="b7f69-123">De lo contrario, deje que el descodificador realice sus propios cálculos.</span><span class="sxs-lookup"><span data-stu-id="b7f69-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="b7f69-124">Actualmente, el códec Windows Media Audio 10 Professional solo admite la reducción vertical de dos canales.</span><span class="sxs-lookup"><span data-stu-id="b7f69-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="b7f69-125">Si la propiedad [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) está establecida en **\_ envolved DSSPEAKER**, el códec omitirá los coeficientes de subconjuntos proporcionados por el autor y se doblará a una señal de 2 canales que puede ser procesada por el descodificador de matriz del receptor.</span><span class="sxs-lookup"><span data-stu-id="b7f69-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="b7f69-126">Esto permite que los equipos envolventes entreguen cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="b7f69-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="b7f69-127">Este modo solo se admite si el origen es 5,1.</span><span class="sxs-lookup"><span data-stu-id="b7f69-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="b7f69-128">El códec solo puede doblar 8 canales a 2 canales.</span><span class="sxs-lookup"><span data-stu-id="b7f69-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f69-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f69-129">Requirements</span></span>



| <span data-ttu-id="b7f69-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f69-130">Requirement</span></span> | <span data-ttu-id="b7f69-131">Value</span><span class="sxs-lookup"><span data-stu-id="b7f69-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f69-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f69-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f69-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b7f69-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7f69-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f69-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f69-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7f69-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7f69-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7f69-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f69-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7f69-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f69-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f69-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f69-139">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7f69-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
