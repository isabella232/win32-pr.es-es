---
description: Especifica el grado en el que el códec debe reducir el intervalo de color efectivo del vídeo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Propiedad MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706210"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="19251-103">\_Propiedad RANGEREDUX de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="19251-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="19251-104">Especifica el grado en el que el códec debe reducir el intervalo de color efectivo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="19251-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="19251-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="19251-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="19251-106">g \_ wszWMVCRangeRedux</span><span class="sxs-lookup"><span data-stu-id="19251-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="19251-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="19251-107">Data Type</span></span>

<span data-ttu-id="19251-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="19251-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="19251-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="19251-109">Default Value</span></span>

<span data-ttu-id="19251-110">0</span><span class="sxs-lookup"><span data-stu-id="19251-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="19251-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19251-111">Remarks</span></span>

<span data-ttu-id="19251-112">Reducción del intervalo especifica el grado en el que el códec debe reducir el intervalo de luminancia y de croma del vídeo.</span><span class="sxs-lookup"><span data-stu-id="19251-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="19251-113">Al reducir el intervalo se reduce el tamaño de los fotogramas de vídeo codificados, pero también se reduce el detalle de color del vídeo.</span><span class="sxs-lookup"><span data-stu-id="19251-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="19251-114">La reducción del intervalo consiste en la reducción durante la codificación y la expansión durante la descodificación.</span><span class="sxs-lookup"><span data-stu-id="19251-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="19251-115">Es posible hacer que los factores de expansión sean distintos de los factores de reducción, pero esto no se recomienda en la mayoría de los escenarios en los que resulta útil volver a asignar intervalos.</span><span class="sxs-lookup"><span data-stu-id="19251-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="19251-116">La reducción y la expansión del rango se realizan por separado en los canales de luminancia y croma.</span><span class="sxs-lookup"><span data-stu-id="19251-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="19251-117">Reducir el intervalo puede ser una manera eficaz de reducir la complejidad del vídeo de baja velocidad de bits sin sacrificar el detalle de la imagen.</span><span class="sxs-lookup"><span data-stu-id="19251-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="19251-118">Al establecer los cuatro valores en 8, se reduce la cantidad de información de luminancia y cromas a la mitad, lo que hace que se dirija más bits para conservar los detalles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="19251-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="19251-119">El códec puede optar por usar automáticamente la reducción del intervalo al codificar vídeo a velocidades de bits muy bajas.</span><span class="sxs-lookup"><span data-stu-id="19251-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="19251-120">Al establecer los cuatro valores en 0, se deshabilita completamente la reducción del intervalo incluso en escenarios de velocidad de bits bajo.</span><span class="sxs-lookup"><span data-stu-id="19251-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="19251-121">Al reducir el intervalo de colores se reduce el tamaño codificado de los fotogramas de vídeo, pero se puede introducir un desenfoque en los fotogramas descodificados.</span><span class="sxs-lookup"><span data-stu-id="19251-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="19251-122">Si no se establece esta propiedad, el códec determina si se va a usar la reducción del intervalo en el tiempo de codificación.</span><span class="sxs-lookup"><span data-stu-id="19251-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="19251-123">Normalmente, el códec selecciona esta opción solo a velocidades de bits bajas.</span><span class="sxs-lookup"><span data-stu-id="19251-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="19251-124">El valor de esta propiedad es una combinación de cuatro componentes, separados por ceros, con el formato 0x0M0m0N0n, donde:</span><span class="sxs-lookup"><span data-stu-id="19251-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="19251-125">M es el factor de reducción del intervalo de codificación del componente Y.</span><span class="sxs-lookup"><span data-stu-id="19251-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="19251-126">m es el factor de expansión del intervalo de descodificación del componente Y (normalmente igual que M).</span><span class="sxs-lookup"><span data-stu-id="19251-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="19251-127">N es el factor de reducción del intervalo de codificación del componente UV.</span><span class="sxs-lookup"><span data-stu-id="19251-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="19251-128">n es el factor de expansión del intervalo de descodificación del componente UV (lo que suele ser el mismo que N).</span><span class="sxs-lookup"><span data-stu-id="19251-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="19251-129">Cada factor es un dígito comprendido entre 0 y 8, donde 0 es sin reducción o expansión y 8 es la reducción o expansión máxima.</span><span class="sxs-lookup"><span data-stu-id="19251-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="19251-130">Si establece el valor en 0x00000000, la reducción del intervalo se deshabilita completamente.</span><span class="sxs-lookup"><span data-stu-id="19251-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="19251-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19251-131">Requirements</span></span>



| <span data-ttu-id="19251-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="19251-132">Requirement</span></span> | <span data-ttu-id="19251-133">Value</span><span class="sxs-lookup"><span data-stu-id="19251-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19251-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19251-134">Minimum supported client</span></span><br/> | <span data-ttu-id="19251-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="19251-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="19251-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19251-136">Minimum supported server</span></span><br/> | <span data-ttu-id="19251-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="19251-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19251-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19251-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="19251-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19251-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19251-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="19251-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19251-141">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19251-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




