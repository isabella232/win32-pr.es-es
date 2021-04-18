---
description: Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeración D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717731"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="ff122-103">Enumeración D3DXTANGENT</span><span class="sxs-lookup"><span data-stu-id="ff122-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="ff122-104">Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.</span><span class="sxs-lookup"><span data-stu-id="ff122-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff122-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff122-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="ff122-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ff122-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ff122-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="ff122-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-108">Los valores de las coordenadas de textura en la dirección u se encuentran entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="ff122-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="ff122-109">En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo.</span><span class="sxs-lookup"><span data-stu-id="ff122-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ff122-110">Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ff122-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff122-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="ff122-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-112">Los valores de las coordenadas de textura en la dirección v se encuentran entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="ff122-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="ff122-113">En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo.</span><span class="sxs-lookup"><span data-stu-id="ff122-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ff122-114">Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ff122-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff122-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ encapsulado \_ UV**</span><span class="sxs-lookup"><span data-stu-id="ff122-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-116">Los valores de las coordenadas de textura en ambas direcciones se encuentran entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="ff122-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="ff122-117">En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo.</span><span class="sxs-lookup"><span data-stu-id="ff122-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ff122-118">Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ff122-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff122-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ no \_ normalizar las \_ partes parciales**</span><span class="sxs-lookup"><span data-stu-id="ff122-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-120">No normalice las derivadas parciales con respecto a las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ff122-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="ff122-121">Si no se normaliza, la escala de los derivados parciales es proporcional a la escala del modelo 3D dividida por la escala del triángulo en el espacio (u, v).</span><span class="sxs-lookup"><span data-stu-id="ff122-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="ff122-122">Este valor de escala proporciona una medida de cuánto se estira la textura en una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="ff122-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="ff122-123">La longitud del vector resultante es una suma ponderada de las longitudes de los derivados parciales.</span><span class="sxs-lookup"><span data-stu-id="ff122-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT no se \_ \_ corortogonal**</span><span class="sxs-lookup"><span data-stu-id="ff122-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-125">No transforme las coordenadas de textura en coordenadas cartesianas ortogonales.</span><span class="sxs-lookup"><span data-stu-id="ff122-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="ff122-126">Es mutuamente excluyente con D3DXTANGENT \_ ortogonal \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V.</span><span class="sxs-lookup"><span data-stu-id="ff122-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ortogonal \_ desde \_ V**</span><span class="sxs-lookup"><span data-stu-id="ff122-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-128">Calcule el derivado parcial con respecto a la coordenada de textura v independientemente para cada vértice y, a continuación, calcule el derivado parcial con respecto a usted como el producto cruzado de la derivada parcial con respecto a v y el vector normal.</span><span class="sxs-lookup"><span data-stu-id="ff122-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="ff122-129">Mutuamente excluyente con D3DXTANGENT no se ortogonala \_ \_ y D3DXTANGENT se \_ ortogonala \_ desde \_ U.</span><span class="sxs-lookup"><span data-stu-id="ff122-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ortogonal \_ desde \_ U**</span><span class="sxs-lookup"><span data-stu-id="ff122-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-131">Calcule el derivado parcial con respecto a la coordenada de textura u de forma independiente para cada vértice y, a continuación, calcule el derivado parcial con respecto a v como el producto cruzado del vector normal y el derivado parcial con respecto a usted.</span><span class="sxs-lookup"><span data-stu-id="ff122-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="ff122-132">Mutuamente excluyente con D3DXTANGENT no se ha \_ \_ ortogonal y D3DXTANGENT \_ ortogonal \_ desde \_ V.</span><span class="sxs-lookup"><span data-stu-id="ff122-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Peso \_ de D3DXTANGENT por \_ área**</span><span class="sxs-lookup"><span data-stu-id="ff122-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-134">Ponderación de la dirección del vector calculado por vértices normal o derivado parcial calculado según las áreas de los triángulos adjuntas a ese vértice.</span><span class="sxs-lookup"><span data-stu-id="ff122-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="ff122-135">Es mutuamente excluyente con el peso de D3DXTANGENT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ff122-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**Peso de D3DXTANGENT \_ \_ igual**</span><span class="sxs-lookup"><span data-stu-id="ff122-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-137">Calcula un vector normal de longitud de unidad para cada triángulo de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff122-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="ff122-138">Es mutuamente excluyente con el peso de D3DXTANGENT \_ \_ por \_ área.</span><span class="sxs-lookup"><span data-stu-id="ff122-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT de \_ viento \_ CW**</span><span class="sxs-lookup"><span data-stu-id="ff122-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-140">Los vértices se ordenan en sentido de las agujas del reloj alrededor de cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="ff122-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="ff122-141">Por lo tanto, la dirección del vector normal calculado se invierte 180 grados de la dirección calculada mediante el orden de vértices en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="ff122-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calcular \_ normales**</span><span class="sxs-lookup"><span data-stu-id="ff122-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-143">Calcule el vector normal por vértice para cada triángulo de la malla de entrada y omita los vectores normales que ya se encuentren en la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff122-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ff122-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ generar \_ en \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="ff122-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="ff122-145">Los resultados se almacenan en la malla de entrada original y no se usa la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="ff122-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff122-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff122-146">Requirements</span></span>



| <span data-ttu-id="ff122-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff122-147">Requirement</span></span> | <span data-ttu-id="ff122-148">Value</span><span class="sxs-lookup"><span data-stu-id="ff122-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff122-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff122-149">Header</span></span><br/> | <dl> <span data-ttu-id="ff122-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff122-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff122-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff122-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff122-152">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="ff122-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="ff122-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="ff122-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




