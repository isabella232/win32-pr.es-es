---
description: Especifica si el DSP de la captura de voz usa el modo de origen o el modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Propiedad MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275856"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="56442-103">Propiedad del modo de origen de MFPKEY \_ WMAAECMA \_ DMO \_ \_</span><span class="sxs-lookup"><span data-stu-id="56442-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="56442-104">Especifica si el DSP de la captura de voz usa el modo de origen o el modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="56442-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="56442-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="56442-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="56442-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="56442-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="56442-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="56442-107">Data Type</span></span>

<span data-ttu-id="56442-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="56442-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="56442-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="56442-109">Default Value</span></span>

<span data-ttu-id="56442-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="56442-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="56442-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="56442-111">Applies To</span></span>

-   [<span data-ttu-id="56442-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="56442-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="56442-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56442-113">Remarks</span></span>

<span data-ttu-id="56442-114">En el modo de origen, la aplicación no tiene que enviar datos de entrada al DSP, porque el DSP extrae automáticamente los datos de los dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="56442-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="56442-115">En el modo de filtro, la aplicación debe enviar los datos de entrada al DSP.</span><span class="sxs-lookup"><span data-stu-id="56442-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="56442-116">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="56442-116">This property can have the following values.</span></span>



| <span data-ttu-id="56442-117">Value</span><span class="sxs-lookup"><span data-stu-id="56442-117">Value</span></span>          | <span data-ttu-id="56442-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="56442-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="56442-119">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="56442-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="56442-120">Modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="56442-120">Filter mode.</span></span> |
| <span data-ttu-id="56442-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="56442-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="56442-122">Modo de origen.</span><span class="sxs-lookup"><span data-stu-id="56442-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="56442-123">Cuando DMO está en modo de origen, solo debe llamar a [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) para establecer el formato del flujo de salida y no llamar a [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para establecer formatos de flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="56442-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="56442-124">De lo contrario, se producirá un error al inicializar DMO</span><span class="sxs-lookup"><span data-stu-id="56442-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="56442-125">Si el valor de esta propiedad es VARIANT \_ true, el DSP tiene cero entradas.</span><span class="sxs-lookup"><span data-stu-id="56442-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="56442-126">Si el valor es VARIANT \_ false, el DSP tiene una o dos entradas, dependiendo del valor de la propiedad [MFPKEY \_ WMAAECMA \_ del \_ modo del sistema](mfpkey-wmaaecma-system-modeproperty.md) , como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="56442-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="56442-127">Value</span><span class="sxs-lookup"><span data-stu-id="56442-127">Value</span></span>                     | <span data-ttu-id="56442-128">Número de entradas</span><span class="sxs-lookup"><span data-stu-id="56442-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="56442-129">\_matriz OPTIBEAM \_ y \_ AEC</span><span class="sxs-lookup"><span data-stu-id="56442-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="56442-130">2</span><span class="sxs-lookup"><span data-stu-id="56442-130">2</span></span>                |
| <span data-ttu-id="56442-131">\_solo matriz \_ OPTIBEAM</span><span class="sxs-lookup"><span data-stu-id="56442-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="56442-132">1</span><span class="sxs-lookup"><span data-stu-id="56442-132">1</span></span>                |
| <span data-ttu-id="56442-133">\_AEC de canal único \_</span><span class="sxs-lookup"><span data-stu-id="56442-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="56442-134">2</span><span class="sxs-lookup"><span data-stu-id="56442-134">2</span></span>                |
| <span data-ttu-id="56442-135">\_NSAGC de canal único \_</span><span class="sxs-lookup"><span data-stu-id="56442-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="56442-136">1</span><span class="sxs-lookup"><span data-stu-id="56442-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="56442-137">Solo los modos con una sola entrada funcionarán con el filtro de contenedor DMO de la API de DirectShow 9,0.</span><span class="sxs-lookup"><span data-stu-id="56442-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56442-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56442-138">Requirements</span></span>



| <span data-ttu-id="56442-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="56442-139">Requirement</span></span> | <span data-ttu-id="56442-140">Value</span><span class="sxs-lookup"><span data-stu-id="56442-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56442-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56442-141">Minimum supported client</span></span><br/> | <span data-ttu-id="56442-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56442-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="56442-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56442-143">Minimum supported server</span></span><br/> | <span data-ttu-id="56442-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56442-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56442-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56442-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="56442-146"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56442-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56442-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="56442-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56442-148">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56442-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="56442-149">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="56442-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
