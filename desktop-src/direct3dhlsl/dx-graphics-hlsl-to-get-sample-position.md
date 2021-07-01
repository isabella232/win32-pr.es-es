---
title: GetSamplePosition (objeto de textura HLSL de DirectX)
description: Obtiene la posición del ejemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118590"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="04651-103">GetSamplePosition (objeto de textura HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="04651-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="04651-104">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="04651-104">Gets the position of the specified sample.</span></span>

<span data-ttu-id="04651-105">ret Object.GetSamplePosition( int s );</span><span class="sxs-lookup"><span data-stu-id="04651-105">ret Object.GetSamplePosition( int s );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="04651-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04651-106">Parameters</span></span>



| <span data-ttu-id="04651-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="04651-107">Item</span></span>                                                                                           | <span data-ttu-id="04651-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="04651-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04651-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="04651-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="04651-110">Un tipo de objeto de textura [](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="04651-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="04651-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="04651-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="04651-112">\[en \] el índice de ejemplo de base cero.</span><span class="sxs-lookup"><span data-stu-id="04651-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="04651-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04651-113">Return Value</span></span>

<span data-ttu-id="04651-114">Devuelve la posición de ejemplo (x,y), un vector de punto flotante de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="04651-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="04651-115">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="04651-115">Minimum Shader Model</span></span>

<span data-ttu-id="04651-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="04651-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04651-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04651-117">vs\_4\_0</span></span> | <span data-ttu-id="04651-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="04651-118">vs\_4\_1</span></span>  | <span data-ttu-id="04651-119">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04651-119">ps\_4\_0</span></span> | <span data-ttu-id="04651-120">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="04651-120">ps\_4\_1</span></span>  | <span data-ttu-id="04651-121">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04651-121">gs\_4\_0</span></span> | <span data-ttu-id="04651-122">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="04651-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="04651-123">x</span><span class="sxs-lookup"><span data-stu-id="04651-123">x</span></span>         |          | <span data-ttu-id="04651-124">x</span><span class="sxs-lookup"><span data-stu-id="04651-124">x</span></span>         |          | <span data-ttu-id="04651-125">x</span><span class="sxs-lookup"><span data-stu-id="04651-125">x</span></span>         |



 

-   <span data-ttu-id="04651-126">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="04651-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="04651-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04651-127">Remarks</span></span>

<span data-ttu-id="04651-128">Un sombreador de píxeles se puede evaluar con frecuencia de ejemplo (ejecutar un sombreador de píxeles una vez por muestra) o con frecuencia de píxeles (ejecutar un sombreador de píxeles una vez por píxel).</span><span class="sxs-lookup"><span data-stu-id="04651-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="04651-129">Adjunte la semántica de SV SampleIndex a una entrada de sombreador de píxeles para invocar un sombreador de píxeles con frecuencia de muestra. A continuación, el valor de entrada se usa como índice de ejemplo al muestrear el destino \_ de representación.</span><span class="sxs-lookup"><span data-stu-id="04651-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="04651-130">Puede interpolar una entrada de sombreador de píxeles de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="04651-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="04651-131">Para interpolar en:</span><span class="sxs-lookup"><span data-stu-id="04651-131">To interpolate at:</span></span>

-   <span data-ttu-id="04651-132">Un centro de píxeles, no use ninguna semántica.</span><span class="sxs-lookup"><span data-stu-id="04651-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="04651-133">Un ejemplo, use la semántica \_ SV SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="04651-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="04651-134">Una ubicación de centroide, use el [ \_ modificador centroide.](dx-graphics-hlsl-struct.md)</span><span class="sxs-lookup"><span data-stu-id="04651-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04651-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04651-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04651-136">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="04651-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





