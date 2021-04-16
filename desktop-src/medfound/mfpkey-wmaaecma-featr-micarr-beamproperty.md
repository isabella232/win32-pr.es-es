---
description: Especifica el rayo que usa el DSP de la captura de voz para el procesamiento de la matriz de micrófono.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696696"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="33bda-103">MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_</span><span class="sxs-lookup"><span data-stu-id="33bda-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="33bda-104">Especifica el rayo que usa el DSP de la captura de voz para el procesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="33bda-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="33bda-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="33bda-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="33bda-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="33bda-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="33bda-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="33bda-107">Data Type</span></span>

<span data-ttu-id="33bda-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="33bda-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="33bda-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="33bda-109">Applies To</span></span>

-   [<span data-ttu-id="33bda-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="33bda-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="33bda-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33bda-111">Remarks</span></span>

<span data-ttu-id="33bda-112">Establezca esta propiedad si el valor de la propiedad [MFPKEY \_ WMAAECMA \_ feat \_ \_ mode MICARR](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY \_ externo \_ viga.</span><span class="sxs-lookup"><span data-stu-id="33bda-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="33bda-113">Si el valor del [**\_ modo MFPKEY WMAAECMA \_ featr \_ MICARR \_**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY de \_ un solo \_ rayo, puede leer esta propiedad para consultar qué rayo ha seleccionado el DSP.</span><span class="sxs-lookup"><span data-stu-id="33bda-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="33bda-114">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="33bda-114">This property can have the following values.</span></span> <span data-ttu-id="33bda-115">Los valores están en horizontal.</span><span class="sxs-lookup"><span data-stu-id="33bda-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="33bda-116">Value</span><span class="sxs-lookup"><span data-stu-id="33bda-116">Value</span></span> | <span data-ttu-id="33bda-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="33bda-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="33bda-118">0</span><span class="sxs-lookup"><span data-stu-id="33bda-118">0</span></span>     | <span data-ttu-id="33bda-119">-50 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-119">-50 degrees.</span></span>             |
| <span data-ttu-id="33bda-120">1</span><span class="sxs-lookup"><span data-stu-id="33bda-120">1</span></span>     | <span data-ttu-id="33bda-121">-40 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-121">-40 degrees.</span></span>             |
| <span data-ttu-id="33bda-122">2</span><span class="sxs-lookup"><span data-stu-id="33bda-122">2</span></span>     | <span data-ttu-id="33bda-123">-30 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-123">-30 degrees.</span></span>             |
| <span data-ttu-id="33bda-124">3</span><span class="sxs-lookup"><span data-stu-id="33bda-124">3</span></span>     | <span data-ttu-id="33bda-125">-20 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-125">-20 degrees.</span></span>             |
| <span data-ttu-id="33bda-126">4</span><span class="sxs-lookup"><span data-stu-id="33bda-126">4</span></span>     | <span data-ttu-id="33bda-127">-10 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-127">-10 degrees.</span></span>             |
| <span data-ttu-id="33bda-128">5</span><span class="sxs-lookup"><span data-stu-id="33bda-128">5</span></span>     | <span data-ttu-id="33bda-129">0 grados (centro).</span><span class="sxs-lookup"><span data-stu-id="33bda-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="33bda-130">6</span><span class="sxs-lookup"><span data-stu-id="33bda-130">6</span></span>     | <span data-ttu-id="33bda-131">10 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-131">10 degrees.</span></span>              |
| <span data-ttu-id="33bda-132">7</span><span class="sxs-lookup"><span data-stu-id="33bda-132">7</span></span>     | <span data-ttu-id="33bda-133">20 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-133">20 degrees.</span></span>              |
| <span data-ttu-id="33bda-134">8</span><span class="sxs-lookup"><span data-stu-id="33bda-134">8</span></span>     | <span data-ttu-id="33bda-135">30 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-135">30 degrees.</span></span>              |
| <span data-ttu-id="33bda-136">9</span><span class="sxs-lookup"><span data-stu-id="33bda-136">9</span></span>     | <span data-ttu-id="33bda-137">40 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-137">40 degrees.</span></span>              |
| <span data-ttu-id="33bda-138">10</span><span class="sxs-lookup"><span data-stu-id="33bda-138">10</span></span>    | <span data-ttu-id="33bda-139">50 grados.</span><span class="sxs-lookup"><span data-stu-id="33bda-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="33bda-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33bda-140">Requirements</span></span>



| <span data-ttu-id="33bda-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="33bda-141">Requirement</span></span> | <span data-ttu-id="33bda-142">Value</span><span class="sxs-lookup"><span data-stu-id="33bda-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33bda-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33bda-143">Minimum supported client</span></span><br/> | <span data-ttu-id="33bda-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="33bda-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="33bda-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33bda-145">Minimum supported server</span></span><br/> | <span data-ttu-id="33bda-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="33bda-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33bda-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33bda-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bda-148"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33bda-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bda-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="33bda-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bda-150">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33bda-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="33bda-151">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="33bda-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
