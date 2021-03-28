---
title: Modelo de sombreador HLSL 6,4
description: Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914262"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="dcc20-103">Modelo de sombreador HLSL 6,4</span><span class="sxs-lookup"><span data-stu-id="dcc20-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="dcc20-104">Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4.</span><span class="sxs-lookup"><span data-stu-id="dcc20-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="dcc20-105">Modelo de sombreador 6,4</span><span class="sxs-lookup"><span data-stu-id="dcc20-105">Shader Model 6.4</span></span>
<span data-ttu-id="dcc20-106">Estos intrínsecos son una característica necesaria o compatible del modelo de sombreador 6,4.</span><span class="sxs-lookup"><span data-stu-id="dcc20-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="dcc20-107">Por consiguiente, no se requiere ninguna comprobación de bits de funcionalidad independiente, más allá de garantizar el uso del modelo de sombreador 6,4.</span><span class="sxs-lookup"><span data-stu-id="dcc20-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="dcc20-108">El cliente mínimo admitido para estas rutinas es Windows 10, versión 1903.</span><span class="sxs-lookup"><span data-stu-id="dcc20-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="dcc20-109">Intrínsecos del lenguaje de sombreado</span><span class="sxs-lookup"><span data-stu-id="dcc20-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="dcc20-110">Entero sin signo Dot-Product de 4 elementos y acumular</span><span class="sxs-lookup"><span data-stu-id="dcc20-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="dcc20-111">Entero sin signo de 4 dimensiones-producto con agregar.</span><span class="sxs-lookup"><span data-stu-id="dcc20-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="dcc20-112">Multiplica cada par correspondiente de bytes int sin signo de 8 bits en los dos DWORDs de entrada y suma los resultados en el acumulador de enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="dcc20-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="dcc20-113">Esta instrucción funciona en una única calle de SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="dcc20-114">También se supone que las entradas son cantidades de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="dcc20-115">Entero con signo Dot-Product de 4 elementos y acumular</span><span class="sxs-lookup"><span data-stu-id="dcc20-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="dcc20-116">Entero de cuatro dimensiones con signo de un producto con agregar.</span><span class="sxs-lookup"><span data-stu-id="dcc20-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="dcc20-117">Multiplica juntos cada par correspondiente de bytes int con signo de 8 bits en los dos DWORDs de entrada y suma los resultados en el acumulador de enteros con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="dcc20-118">Esta instrucción funciona en una única calle de SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="dcc20-119">También se supone que las entradas son cantidades de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="dcc20-120">Punto flotante de precisión simple de 2 elementos Dot-Product y acumulado</span><span class="sxs-lookup"><span data-stu-id="dcc20-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="dcc20-121">Producto de punto flotante de 2 dimensiones de vectores half2 con Add.</span><span class="sxs-lookup"><span data-stu-id="dcc20-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="dcc20-122">Multiplica los elementos de los dos vectores de entrada Float de media precisión y suma los resultados en el acumulador de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="dcc20-123">Estas instrucciones operan en una única calle de SIMD de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dcc20-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="dcc20-124">Las entradas son cantidades de 16 bits empaquetadas en la misma calle.</span><span class="sxs-lookup"><span data-stu-id="dcc20-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="dcc20-125">Esto se trata en el bit de características de baja precisión (lo que indica que la compatibilidad media y corta nativa está presente).</span><span class="sxs-lookup"><span data-stu-id="dcc20-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="dcc20-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="dcc20-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="dcc20-127">Entero sin signo que representa el número de píxeles de destino escritos por cada invocación del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dcc20-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="dcc20-128">Los valores válidos pertenecen al conjunto de valores de enumeración [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="dcc20-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="dcc20-129">Este valor del sistema está disponible en plataformas [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o superior.</span><span class="sxs-lookup"><span data-stu-id="dcc20-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="dcc20-130">Se puede escribir como máximo una de las fases del sombreador de vértices o de geometría.</span><span class="sxs-lookup"><span data-stu-id="dcc20-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="dcc20-131">Se puede leer desde la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dcc20-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="dcc20-132">Para obtener más información, vea el [sombreado de velocidad variable](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="dcc20-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>