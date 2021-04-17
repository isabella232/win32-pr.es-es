---
description: Especifica la geometría de la matriz de micrófono para el DSP de captura de voz.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Propiedad MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696692"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="14249-103">MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR</span><span class="sxs-lookup"><span data-stu-id="14249-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="14249-104">Especifica la geometría de la matriz de micrófono para el DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="14249-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="14249-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="14249-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="14249-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="14249-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="14249-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="14249-107">Data Type</span></span>

<span data-ttu-id="14249-108">BLOB de VT \_</span><span class="sxs-lookup"><span data-stu-id="14249-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="14249-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="14249-109">Applies To</span></span>

-   [<span data-ttu-id="14249-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="14249-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="14249-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14249-111">Remarks</span></span>

<span data-ttu-id="14249-112">El valor de esta propiedad es una estructura de geometría de la [**\_ \_ matriz \_ KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) .</span><span class="sxs-lookup"><span data-stu-id="14249-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="14249-113">Esta estructura se define en el archivo de encabezado KsMedia. h.</span><span class="sxs-lookup"><span data-stu-id="14249-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="14249-114">Para obtener la geometría de la matriz de micrófono, consulte el dispositivo de audio para la \_ propiedad Geometry de la matriz KSPROPERTY audio \_ MIC llamando \_ \_ al método **IKsControl:: KSPROPERTY** en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14249-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="14249-115">Para obtener más información acerca de las matrices de micrófono, descargue las notas del producto [Cómo crear y usar matrices de micrófonos para Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span><span class="sxs-lookup"><span data-stu-id="14249-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="14249-116">Establezca esta propiedad si usa el DSP en modo de filtro y el procesamiento de matriz de micrófono está habilitado.</span><span class="sxs-lookup"><span data-stu-id="14249-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="14249-117">Si usa el DSP en modo de origen, el DSP consulta automáticamente la información de geometría en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14249-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="14249-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14249-118">Requirements</span></span>



| <span data-ttu-id="14249-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14249-119">Requirement</span></span> | <span data-ttu-id="14249-120">Value</span><span class="sxs-lookup"><span data-stu-id="14249-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14249-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14249-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14249-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14249-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="14249-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14249-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14249-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="14249-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14249-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14249-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14249-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="14249-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14249-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="14249-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14249-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14249-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="14249-129">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="14249-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
