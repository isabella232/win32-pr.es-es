---
description: Especifica el perfil de complejidad del contenido codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Propiedad MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908793"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="97c4a-103">\_Propiedad DECODERCOMPLEXITYPROFILE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="97c4a-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="97c4a-104">Especifica el perfil de complejidad del contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="97c4a-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="97c4a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="97c4a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="97c4a-106">g \_ wszWMVCDecoderComplexityProfile</span><span class="sxs-lookup"><span data-stu-id="97c4a-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="97c4a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="97c4a-107">Data Type</span></span>

<span data-ttu-id="97c4a-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="97c4a-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="97c4a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97c4a-109">Remarks</span></span>

<span data-ttu-id="97c4a-110">Este valor solo se puede leer una vez completada la codificación.</span><span class="sxs-lookup"><span data-stu-id="97c4a-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="97c4a-111">En el caso de audio, esta propiedad tiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="97c4a-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="97c4a-112">Value</span><span class="sxs-lookup"><span data-stu-id="97c4a-112">Value</span></span> | <span data-ttu-id="97c4a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="97c4a-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c4a-114">Nivel</span><span class="sxs-lookup"><span data-stu-id="97c4a-114">"L1"</span></span>  | <span data-ttu-id="97c4a-115">Codificación estándar con una velocidad de muestreo de 44,1 KHz y una velocidad de bits máxima de 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="97c4a-116">L2</span><span class="sxs-lookup"><span data-stu-id="97c4a-116">"L2"</span></span>  | <span data-ttu-id="97c4a-117">Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="97c4a-118">Caché</span><span class="sxs-lookup"><span data-stu-id="97c4a-118">"L3"</span></span>  | <span data-ttu-id="97c4a-119">Codificación estándar con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 385 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="97c4a-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="97c4a-120">"M0a"</span></span> | <span data-ttu-id="97c4a-121">Codificación profesional con velocidades de muestreo de hasta 48 KHz y velocidades de bits entre 48 y 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="97c4a-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="97c4a-122">"M0b"</span></span> | <span data-ttu-id="97c4a-123">Codificación profesional con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="97c4a-124">Conector</span><span class="sxs-lookup"><span data-stu-id="97c4a-124">"M1"</span></span>  | <span data-ttu-id="97c4a-125">Codificación profesional con velocidades de muestreo de hasta 48 KHz y una velocidad de bits máxima de 384 Kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="97c4a-126">²</span><span class="sxs-lookup"><span data-stu-id="97c4a-126">"M2"</span></span>  | <span data-ttu-id="97c4a-127">Codificación profesional con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 768 kbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="97c4a-128">M3</span><span class="sxs-lookup"><span data-stu-id="97c4a-128">"M3"</span></span>  | <span data-ttu-id="97c4a-129">Codificación profesional con velocidades de muestreo de hasta 96 KHz y una velocidad de bits máxima de 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="97c4a-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="97c4a-130">N1</span><span class="sxs-lookup"><span data-stu-id="97c4a-130">"N1"</span></span>  | <span data-ttu-id="97c4a-131">Codificación sin pérdida con velocidades de muestreo de hasta 48 KHz y un máximo de 2 canales.</span><span class="sxs-lookup"><span data-stu-id="97c4a-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="97c4a-132">N2</span><span class="sxs-lookup"><span data-stu-id="97c4a-132">"N2"</span></span>  | <span data-ttu-id="97c4a-133">Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 6 canales (5,1 envolvente).</span><span class="sxs-lookup"><span data-stu-id="97c4a-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="97c4a-134">N3</span><span class="sxs-lookup"><span data-stu-id="97c4a-134">"N3"</span></span>  | <span data-ttu-id="97c4a-135">Codificación sin pérdida con velocidades de muestreo de hasta 96 KHz y un máximo de 8 canales (7,1 envolvente).</span><span class="sxs-lookup"><span data-stu-id="97c4a-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="97c4a-136">En el caso de vídeo, esta propiedad tiene uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="97c4a-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="97c4a-137">Value</span><span class="sxs-lookup"><span data-stu-id="97c4a-137">Value</span></span> | <span data-ttu-id="97c4a-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="97c4a-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97c4a-139">AISLAMIENTO</span><span class="sxs-lookup"><span data-stu-id="97c4a-139">"AP"</span></span>  | <span data-ttu-id="97c4a-140">perfil avanzado (disponible solo en códec de perfil avanzado de Windows Media Video 9)</span><span class="sxs-lookup"><span data-stu-id="97c4a-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="97c4a-141">CP</span><span class="sxs-lookup"><span data-stu-id="97c4a-141">"CP"</span></span>  | <span data-ttu-id="97c4a-142">ya no se admite</span><span class="sxs-lookup"><span data-stu-id="97c4a-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="97c4a-143">MP</span><span class="sxs-lookup"><span data-stu-id="97c4a-143">"MP"</span></span>  | <span data-ttu-id="97c4a-144">Perfil principal</span><span class="sxs-lookup"><span data-stu-id="97c4a-144">main profile</span></span>                                                                      |
| <span data-ttu-id="97c4a-145">DAÑADO</span><span class="sxs-lookup"><span data-stu-id="97c4a-145">"SP"</span></span>  | <span data-ttu-id="97c4a-146">Perfil simple</span><span class="sxs-lookup"><span data-stu-id="97c4a-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="97c4a-147">Para el contenido de vídeo, puede solicitar un nivel de perfil estableciendo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) antes de comenzar la codificación.</span><span class="sxs-lookup"><span data-stu-id="97c4a-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="97c4a-148">El códec intentará codificar dentro de los parámetros del nivel de complejidad solicitado, pero los demás valores de configuración que configure tendrán prioridad.</span><span class="sxs-lookup"><span data-stu-id="97c4a-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="97c4a-149">Siempre debe comprobar el valor del perfil de complejidad real después de la codificación en caso de que no se pueda respetar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97c4a-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c4a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c4a-150">Requirements</span></span>



| <span data-ttu-id="97c4a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c4a-151">Requirement</span></span> | <span data-ttu-id="97c4a-152">Value</span><span class="sxs-lookup"><span data-stu-id="97c4a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c4a-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97c4a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="97c4a-154">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="97c4a-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97c4a-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97c4a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="97c4a-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="97c4a-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97c4a-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97c4a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="97c4a-158"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c4a-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c4a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="97c4a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c4a-160">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97c4a-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




