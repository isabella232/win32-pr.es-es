---
description: Especifica si el DSP de la captura de voz realiza el preprocesamiento de la matriz de micrófono.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705909"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="e3701-103">MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ Preproc (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e3701-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="e3701-104">Especifica si el DSP de la captura de voz realiza el preprocesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="e3701-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3701-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e3701-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3701-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e3701-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3701-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e3701-107">Data Type</span></span>

<span data-ttu-id="e3701-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="e3701-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="e3701-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="e3701-109">Default Value</span></span>

<span data-ttu-id="e3701-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="e3701-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="e3701-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e3701-111">Applies To</span></span>

-   [<span data-ttu-id="e3701-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="e3701-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="e3701-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3701-113">Remarks</span></span>

<span data-ttu-id="e3701-114">El preprocesamiento puede quitar los tonos estacionales que interfieren con el procesamiento, como un tono con un tono fijo.</span><span class="sxs-lookup"><span data-stu-id="e3701-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="e3701-115">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e3701-115">This property can have the following values.</span></span>



| <span data-ttu-id="e3701-116">Value</span><span class="sxs-lookup"><span data-stu-id="e3701-116">Value</span></span>          | <span data-ttu-id="e3701-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3701-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="e3701-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="e3701-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="e3701-119">Deshabilitar el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="e3701-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="e3701-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="e3701-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="e3701-121">Habilite el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="e3701-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="e3701-122">El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="e3701-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="e3701-123">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="e3701-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="e3701-124">El DSP usa esta propiedad solo cuando está habilitado el procesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="e3701-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3701-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3701-125">Requirements</span></span>



| <span data-ttu-id="e3701-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3701-126">Requirement</span></span> | <span data-ttu-id="e3701-127">Value</span><span class="sxs-lookup"><span data-stu-id="e3701-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3701-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3701-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3701-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3701-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3701-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3701-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3701-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3701-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3701-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3701-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3701-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3701-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3701-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3701-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3701-135">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3701-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e3701-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="e3701-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
