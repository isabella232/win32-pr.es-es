---
description: Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propiedad AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805822"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="d1a8b-103">Propiedad AVEncVideoOutputFrameRate</span><span class="sxs-lookup"><span data-stu-id="d1a8b-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="d1a8b-104">Especifica la velocidad de fotogramas en el flujo de salida del codificador, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="d1a8b-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1a8b-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d1a8b-106">Data type</span></span>

<span data-ttu-id="d1a8b-107">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="d1a8b-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d1a8b-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="d1a8b-108">Property GUID</span></span>

<span data-ttu-id="d1a8b-109">**CODECAPI \_ AVEncVideoOutputFrameRate**</span><span class="sxs-lookup"><span data-stu-id="d1a8b-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="d1a8b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d1a8b-110">Property value</span></span>

<span data-ttu-id="d1a8b-111">El valor de esta propiedad es una relación que define la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="d1a8b-112">Los 32 bits superiores contienen el numerador y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="d1a8b-113">En la tabla siguiente se muestran las velocidades de fotogramas comunes, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="d1a8b-114">Velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="d1a8b-114">Frame rate</span></span> | <span data-ttu-id="d1a8b-115">Proporción</span><span class="sxs-lookup"><span data-stu-id="d1a8b-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="d1a8b-116">23,97</span><span class="sxs-lookup"><span data-stu-id="d1a8b-116">23.97</span></span>      | <span data-ttu-id="d1a8b-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="d1a8b-117">24000/1001</span></span> |
| <span data-ttu-id="d1a8b-118">24</span><span class="sxs-lookup"><span data-stu-id="d1a8b-118">24</span></span>         | <span data-ttu-id="d1a8b-119">24/1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-119">24/1</span></span>       |
| <span data-ttu-id="d1a8b-120">25</span><span class="sxs-lookup"><span data-stu-id="d1a8b-120">25</span></span>         | <span data-ttu-id="d1a8b-121">25/1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-121">25/1</span></span>       |
| <span data-ttu-id="d1a8b-122">29,97</span><span class="sxs-lookup"><span data-stu-id="d1a8b-122">29.97</span></span>      | <span data-ttu-id="d1a8b-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="d1a8b-123">30000/1001</span></span> |
| <span data-ttu-id="d1a8b-124">30</span><span class="sxs-lookup"><span data-stu-id="d1a8b-124">30</span></span>         | <span data-ttu-id="d1a8b-125">30/1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-125">30/1</span></span>       |
| <span data-ttu-id="d1a8b-126">50</span><span class="sxs-lookup"><span data-stu-id="d1a8b-126">50</span></span>         | <span data-ttu-id="d1a8b-127">50/1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-127">50/1</span></span>       |
| <span data-ttu-id="d1a8b-128">59,94</span><span class="sxs-lookup"><span data-stu-id="d1a8b-128">59.94</span></span>      | <span data-ttu-id="d1a8b-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="d1a8b-129">60000/1001</span></span> |
| <span data-ttu-id="d1a8b-130">60</span><span class="sxs-lookup"><span data-stu-id="d1a8b-130">60</span></span>         | <span data-ttu-id="d1a8b-131">60/1</span><span class="sxs-lookup"><span data-stu-id="d1a8b-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="d1a8b-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1a8b-132">Remarks</span></span>

<span data-ttu-id="d1a8b-133">Las aplicaciones pueden establecer esta propiedad para especificar la velocidad de fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="d1a8b-134">Los codificadores también pueden devolver esta propiedad como una capacidad.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="d1a8b-135">Dependiendo del codificador, el valor puede estar restringido a la velocidad de fotogramas de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="d1a8b-136">En caso contrario, el codificador puede convertir la velocidad de fotogramas internamente.</span><span class="sxs-lookup"><span data-stu-id="d1a8b-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="d1a8b-137">Vea la [**propiedad AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="d1a8b-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="d1a8b-138">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="d1a8b-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a8b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a8b-139">Requirements</span></span>



| <span data-ttu-id="d1a8b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a8b-140">Requirement</span></span> | <span data-ttu-id="d1a8b-141">Value</span><span class="sxs-lookup"><span data-stu-id="d1a8b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a8b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1a8b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a8b-143">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a8b-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d1a8b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1a8b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a8b-145">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="d1a8b-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d1a8b-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1a8b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a8b-147"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a8b-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a8b-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1a8b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a8b-149">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="d1a8b-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d1a8b-150">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d1a8b-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

