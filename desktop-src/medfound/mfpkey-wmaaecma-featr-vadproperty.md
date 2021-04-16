---
description: Especifica el tipo de detección de la actividad de voz que realiza el DSP de la captura de voz.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Propiedad MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705906"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="6e693-103">MFPKEY \_ WMAAECMA \_ feat \_ VAD (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6e693-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="6e693-104">Especifica el tipo de detección de la actividad de voz que realiza el DSP de la captura de voz.</span><span class="sxs-lookup"><span data-stu-id="6e693-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6e693-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6e693-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6e693-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="6e693-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="6e693-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6e693-107">Data Type</span></span>

<span data-ttu-id="6e693-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6e693-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="6e693-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="6e693-109">Default Value</span></span>

<span data-ttu-id="6e693-110">0</span><span class="sxs-lookup"><span data-stu-id="6e693-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="6e693-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="6e693-111">Applies To</span></span>

-   [<span data-ttu-id="6e693-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="6e693-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="6e693-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e693-113">Remarks</span></span>

<span data-ttu-id="6e693-114">El valor de esta propiedad es un miembro de la enumeración de [ \_ \_ modo VAD de AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) .</span><span class="sxs-lookup"><span data-stu-id="6e693-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="6e693-115">La salida de la detección de actividad de voz es un número del 0 al 3, calculado para cada fotograma de audio.</span><span class="sxs-lookup"><span data-stu-id="6e693-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="6e693-116">El DSP codifica el resultado en el bit más bajo de las dos primeras muestras de audio en cada fotograma de audio.</span><span class="sxs-lookup"><span data-stu-id="6e693-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="6e693-117">El significado del valor depende del modo especificado.</span><span class="sxs-lookup"><span data-stu-id="6e693-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="6e693-118">En el código siguiente se muestra cómo extraer los resultados de los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="6e693-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="6e693-119">En este ejemplo, *pOutput* es un puntero al inicio de una trama de audio en los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="6e693-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="6e693-120">El valor predeterminado de esta propiedad es 0 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="6e693-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="6e693-121">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="6e693-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e693-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e693-122">Requirements</span></span>



| <span data-ttu-id="6e693-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e693-123">Requirement</span></span> | <span data-ttu-id="6e693-124">Value</span><span class="sxs-lookup"><span data-stu-id="6e693-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e693-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e693-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6e693-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6e693-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e693-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e693-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6e693-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e693-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e693-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e693-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e693-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e693-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e693-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e693-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e693-132">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e693-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
