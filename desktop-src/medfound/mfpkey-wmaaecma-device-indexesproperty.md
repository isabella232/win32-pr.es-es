---
description: Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Propiedad MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908385"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="fb7cb-103">Propiedad de los índices de dispositivo de MFPKEY \_ WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb7cb-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="fb7cb-104">Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fb7cb-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fb7cb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fb7cb-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="fb7cb-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="fb7cb-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb7cb-107">Data Type</span></span>

<span data-ttu-id="fb7cb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fb7cb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="fb7cb-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="fb7cb-109">Default Value</span></span>

<span data-ttu-id="fb7cb-110">(-1,-1).</span><span class="sxs-lookup"><span data-stu-id="fb7cb-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fb7cb-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="fb7cb-111">Applies To</span></span>

-   [<span data-ttu-id="fb7cb-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="fb7cb-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="fb7cb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb7cb-113">Remarks</span></span>

<span data-ttu-id="fb7cb-114">Establezca esta propiedad si usa el DSP en modo de origen.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="fb7cb-115">El DSP omite esta propiedad en modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="fb7cb-116">El valor de la propiedad es una **palabra** de 2 16 bits empaquetada en un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="fb7cb-117">Los 16 bits superiores especifican el dispositivo de representación de audio (normalmente un orador) y los 16 bits inferiores especifican el dispositivo de captura (normalmente un micrófono).</span><span class="sxs-lookup"><span data-stu-id="fb7cb-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="fb7cb-118">Cada dispositivo se especifica como un índice en la recopilación de dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="fb7cb-119">Si el índice es-1, se usa el dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="fb7cb-120">El índice del dispositivo corresponde al índice de la colección que se usa en la interfaz [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) .</span><span class="sxs-lookup"><span data-stu-id="fb7cb-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="fb7cb-121">La aplicación debe reproducir la voz de un extremo a través del dispositivo de representación seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="fb7cb-122">(La voz de extremo final es la voz de la persona en el otro extremo de la línea de teléfono, que se reproduce a través del altavoz en el equipo del usuario). Si el dispositivo de representación seleccionado no tiene un flujo activo, el DSP no puede procesar ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="fb7cb-123">El valor predeterminado de esta propiedad es (-1,-1).</span><span class="sxs-lookup"><span data-stu-id="fb7cb-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="fb7cb-124">En el ejemplo siguiente se muestra cómo inicializar **PROPVARIANT** para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="fb7cb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb7cb-125">Requirements</span></span>



| <span data-ttu-id="fb7cb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb7cb-126">Requirement</span></span> | <span data-ttu-id="fb7cb-127">Value</span><span class="sxs-lookup"><span data-stu-id="fb7cb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7cb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7cb-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb7cb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fb7cb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7cb-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb7cb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb7cb-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb7cb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb7cb-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb7cb-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb7cb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb7cb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7cb-135">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb7cb-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fb7cb-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="fb7cb-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
