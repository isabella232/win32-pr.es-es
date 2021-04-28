---
description: 'MFPKEY_COMPLEXITYEX propiedad : especifica la complejidad del algoritmo del codificador.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087613"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="64548-103">Propiedad MFPKEY \_ COMPLEXITYEX</span><span class="sxs-lookup"><span data-stu-id="64548-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="64548-104">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="64548-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="64548-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="64548-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="64548-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="64548-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="64548-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="64548-107">Data Type</span></span>

<span data-ttu-id="64548-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="64548-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="64548-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="64548-109">Default Value</span></span>

<span data-ttu-id="64548-110">El valor predeterminado depende de la versión del codificador de vídeo, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="64548-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="64548-111">Versión del codificador</span><span class="sxs-lookup"><span data-stu-id="64548-111">Encoder version</span></span>                 | <span data-ttu-id="64548-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="64548-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="64548-113">Windows Media Video codificador 9</span><span class="sxs-lookup"><span data-stu-id="64548-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="64548-114">3</span><span class="sxs-lookup"><span data-stu-id="64548-114">3</span></span>             |
| <span data-ttu-id="64548-115">Windows Media Video codificador 7/8</span><span class="sxs-lookup"><span data-stu-id="64548-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="64548-116">1</span><span class="sxs-lookup"><span data-stu-id="64548-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="64548-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="64548-117">Possible Values</span></span>

<span data-ttu-id="64548-118">Los valores posibles dependen de la versión del codificador de vídeo, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="64548-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="64548-119">Versión del codificador</span><span class="sxs-lookup"><span data-stu-id="64548-119">Encoder version</span></span>                 | <span data-ttu-id="64548-120">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="64548-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="64548-121">Windows Media Video codificador 9</span><span class="sxs-lookup"><span data-stu-id="64548-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="64548-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="64548-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="64548-123">Windows Media Video codificador 7/8</span><span class="sxs-lookup"><span data-stu-id="64548-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="64548-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="64548-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="64548-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64548-125">Remarks</span></span>

<span data-ttu-id="64548-126">Los valores más bajos hacen que el códec use algoritmos de codificación menos complicados.</span><span class="sxs-lookup"><span data-stu-id="64548-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="64548-127">Aunque los algoritmos más sencillos generan resultados de menor calidad, el proceso de codificación es más rápido y requiere menos capacidad de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="64548-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="64548-128">Esto puede ser importante al codificar contenido desde un origen en directo porque el codificador debe procesar las entradas lo suficientemente rápido como para mantenerse al día con el origen.</span><span class="sxs-lookup"><span data-stu-id="64548-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="64548-129">Cualquier valor asignado a esta propiedad se omitirá si la propiedad [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="64548-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="64548-130">En ese caso, MFPKEY \_ COMPLEXITYEX se establece automáticamente en 3.</span><span class="sxs-lookup"><span data-stu-id="64548-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="64548-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64548-131">Requirements</span></span>



| <span data-ttu-id="64548-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="64548-132">Requirement</span></span> | <span data-ttu-id="64548-133">Valor</span><span class="sxs-lookup"><span data-stu-id="64548-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64548-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64548-134">Minimum supported client</span></span><br/> | <span data-ttu-id="64548-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64548-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="64548-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64548-136">Minimum supported server</span></span><br/> | <span data-ttu-id="64548-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64548-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="64548-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64548-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="64548-139"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="64548-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64548-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="64548-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64548-141">Media Foundation propiedades</span><span class="sxs-lookup"><span data-stu-id="64548-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




