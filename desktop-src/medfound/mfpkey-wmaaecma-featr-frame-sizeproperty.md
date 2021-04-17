---
description: Especifica el tamaño del fotograma de audio usado por el DSP de captura de voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Propiedad MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696697"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="70770-103">\_Propiedad de \_ tamaño de \_ marco \_ del MFPKEY de WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="70770-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="70770-104">Especifica el tamaño del fotograma de audio usado por el DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="70770-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="70770-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="70770-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="70770-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="70770-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="70770-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="70770-107">Data Type</span></span>

<span data-ttu-id="70770-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="70770-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="70770-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="70770-109">Default Value</span></span>

<span data-ttu-id="70770-110">0</span><span class="sxs-lookup"><span data-stu-id="70770-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="70770-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="70770-111">Applies To</span></span>

-   [<span data-ttu-id="70770-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="70770-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="70770-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70770-113">Remarks</span></span>

<span data-ttu-id="70770-114">El algoritmo de cancelación del eco acústico (AEC) procesa las muestras de audio PCM en un fotograma cada vez.</span><span class="sxs-lookup"><span data-stu-id="70770-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="70770-115">El valor de esta propiedad es el tamaño del fotograma de audio, en ejemplos.</span><span class="sxs-lookup"><span data-stu-id="70770-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="70770-116">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="70770-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="70770-117">El DSP de captura de voz admite los siguientes tamaños de fotogramas:</span><span class="sxs-lookup"><span data-stu-id="70770-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="70770-118">80</span><span class="sxs-lookup"><span data-stu-id="70770-118">80</span></span>
-   <span data-ttu-id="70770-119">128</span><span class="sxs-lookup"><span data-stu-id="70770-119">128</span></span>
-   <span data-ttu-id="70770-120">160</span><span class="sxs-lookup"><span data-stu-id="70770-120">160</span></span>
-   <span data-ttu-id="70770-121">240</span><span class="sxs-lookup"><span data-stu-id="70770-121">240</span></span>
-   <span data-ttu-id="70770-122">256</span><span class="sxs-lookup"><span data-stu-id="70770-122">256</span></span>
-   <span data-ttu-id="70770-123">320</span><span class="sxs-lookup"><span data-stu-id="70770-123">320</span></span>

<span data-ttu-id="70770-124">Si el valor de esta propiedad es cero, el DSP selecciona el tamaño del marco según el modo del sistema y el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="70770-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="70770-125">Sin embargo, para obtener el mejor rendimiento, se recomienda que las aplicaciones usen el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="70770-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="70770-126">Si el modo de procesamiento es solo una matriz de micrófono, el valor predeterminado es 320 ejemplos.</span><span class="sxs-lookup"><span data-stu-id="70770-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="70770-127">En todos los demás modos de procesamiento, el valor predeterminado es 160 ejemplos.</span><span class="sxs-lookup"><span data-stu-id="70770-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="70770-128">Para obtener más información acerca de los modos de procesamiento del DSP de captura de voz, consulte [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="70770-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="70770-129">Después de la primera llamada a [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), puede leer esta propiedad para obtener el tamaño real de los fotogramas en uso, aunque el [**modo de \_ \_ característica \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) sea false.</span><span class="sxs-lookup"><span data-stu-id="70770-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="70770-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70770-130">Requirements</span></span>



| <span data-ttu-id="70770-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70770-131">Requirement</span></span> | <span data-ttu-id="70770-132">Value</span><span class="sxs-lookup"><span data-stu-id="70770-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70770-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70770-133">Minimum supported client</span></span><br/> | <span data-ttu-id="70770-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70770-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="70770-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70770-135">Minimum supported server</span></span><br/> | <span data-ttu-id="70770-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70770-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70770-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70770-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="70770-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70770-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70770-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="70770-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70770-140">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70770-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="70770-141">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="70770-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
