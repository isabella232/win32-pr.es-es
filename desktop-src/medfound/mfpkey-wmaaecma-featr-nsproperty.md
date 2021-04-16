---
description: Especifica si el DSP de captura de voz realiza la supresión de ruido.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Propiedad MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705907"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="23dcf-103">\_ \_ \_ Propiedad NS del MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="23dcf-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="23dcf-104">Especifica si el DSP de captura de voz realiza la supresión de ruido.</span><span class="sxs-lookup"><span data-stu-id="23dcf-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="23dcf-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="23dcf-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="23dcf-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="23dcf-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="23dcf-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="23dcf-107">Data Type</span></span>

<span data-ttu-id="23dcf-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="23dcf-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="23dcf-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="23dcf-109">Default Value</span></span>

<span data-ttu-id="23dcf-110">1</span><span class="sxs-lookup"><span data-stu-id="23dcf-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="23dcf-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="23dcf-111">Applies To</span></span>

-   [<span data-ttu-id="23dcf-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="23dcf-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="23dcf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23dcf-113">Remarks</span></span>

<span data-ttu-id="23dcf-114">La supresión de ruidos es un componente de procesamiento de señal digital (DSP) que suprime o reduce el ruido de fondo estacionario en la señal de audio.</span><span class="sxs-lookup"><span data-stu-id="23dcf-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="23dcf-115">La supresión de ruido se aplica después de la cancelación del eco acústico (AEC) y el procesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="23dcf-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="23dcf-116">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="23dcf-116">This property can have the following values.</span></span>



| <span data-ttu-id="23dcf-117">Value</span><span class="sxs-lookup"><span data-stu-id="23dcf-117">Value</span></span> | <span data-ttu-id="23dcf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="23dcf-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="23dcf-119">0</span><span class="sxs-lookup"><span data-stu-id="23dcf-119">0</span></span>     | <span data-ttu-id="23dcf-120">Deshabilite la supresión de ruido.</span><span class="sxs-lookup"><span data-stu-id="23dcf-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="23dcf-121">1</span><span class="sxs-lookup"><span data-stu-id="23dcf-121">1</span></span>     | <span data-ttu-id="23dcf-122">Habilitar la supresión de ruido.</span><span class="sxs-lookup"><span data-stu-id="23dcf-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="23dcf-123">El valor predeterminado de esta propiedad es 1 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="23dcf-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="23dcf-124">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="23dcf-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="23dcf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23dcf-125">Requirements</span></span>



| <span data-ttu-id="23dcf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="23dcf-126">Requirement</span></span> | <span data-ttu-id="23dcf-127">Value</span><span class="sxs-lookup"><span data-stu-id="23dcf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23dcf-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23dcf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23dcf-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23dcf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23dcf-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23dcf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23dcf-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="23dcf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23dcf-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23dcf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="23dcf-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23dcf-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23dcf-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="23dcf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23dcf-135">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23dcf-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="23dcf-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="23dcf-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
