---
title: GetSamplePosition (objeto de textura de HLSL de DirectX)
description: Obtiene la posición del ejemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419889"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="f8d6a-103">GetSamplePosition (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="f8d6a-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="f8d6a-104">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="f8d6a-105">RET Object. GetSamplePosition (int s);</span><span class="sxs-lookup"><span data-stu-id="f8d6a-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f8d6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8d6a-106">Parameters</span></span>



| <span data-ttu-id="f8d6a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f8d6a-107">Item</span></span>                                                                                           | <span data-ttu-id="f8d6a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8d6a-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d6a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="f8d6a-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="f8d6a-110">Un tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="f8d6a-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="f8d6a-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="f8d6a-112">\[en \] el índice de ejemplo basado en cero.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="f8d6a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8d6a-113">Return Value</span></span>

<span data-ttu-id="f8d6a-114">Devuelve la posición de ejemplo (x, y), un vector de punto flotante de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f8d6a-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f8d6a-115">Minimum Shader Model</span></span>

<span data-ttu-id="f8d6a-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f8d6a-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8d6a-117">vs\_4\_0</span></span> | <span data-ttu-id="f8d6a-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8d6a-118">vs\_4\_1</span></span>  | <span data-ttu-id="f8d6a-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8d6a-119">ps\_4\_0</span></span> | <span data-ttu-id="f8d6a-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8d6a-120">ps\_4\_1</span></span>  | <span data-ttu-id="f8d6a-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8d6a-121">gs\_4\_0</span></span> | <span data-ttu-id="f8d6a-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8d6a-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="f8d6a-123">x</span><span class="sxs-lookup"><span data-stu-id="f8d6a-123">x</span></span>         |          | <span data-ttu-id="f8d6a-124">x</span><span class="sxs-lookup"><span data-stu-id="f8d6a-124">x</span></span>         |          | <span data-ttu-id="f8d6a-125">x</span><span class="sxs-lookup"><span data-stu-id="f8d6a-125">x</span></span>         |



 

-   <span data-ttu-id="f8d6a-126">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8d6a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8d6a-127">Remarks</span></span>

<span data-ttu-id="f8d6a-128">Un sombreador de píxeles se puede evaluar con una frecuencia de muestreo (ejecutar un sombreador de píxeles una vez por ejemplo) o con una frecuencia de píxeles (ejecutar un sombreador de píxeles una vez por píxel).</span><span class="sxs-lookup"><span data-stu-id="f8d6a-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="f8d6a-129">Adjunte la \_ semántica de VP SampleIndex a una entrada de sombreador de píxeles para invocar un sombreador de píxeles a la frecuencia de muestreo; a continuación, el valor de entrada se utiliza como índice de ejemplo al realizar el muestreo del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="f8d6a-130">Puede interpolar una entrada del sombreador de píxeles de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="f8d6a-131">Para interpolar en:</span><span class="sxs-lookup"><span data-stu-id="f8d6a-131">To interpolate at:</span></span>

-   <span data-ttu-id="f8d6a-132">Un centro de píxeles, no use ninguna semántica.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="f8d6a-133">Un ejemplo, use la \_ semántica de SAMPLEINDEX VP.</span><span class="sxs-lookup"><span data-stu-id="f8d6a-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="f8d6a-134">Una ubicación centroide, use el modificador [ \_ centroide](dx-graphics-hlsl-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="f8d6a-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8d6a-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8d6a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8d6a-136">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="f8d6a-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





