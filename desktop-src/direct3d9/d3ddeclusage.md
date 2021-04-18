---
description: Identifica el uso previsto de los datos de vértices.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumeración D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721445"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="988ec-103">Enumeración D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="988ec-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="988ec-104">Identifica el uso previsto de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="988ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="988ec-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="988ec-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="988ec-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="988ec-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posición D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="988ec-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-108">Coloque los datos comprendidos entre (-1,-1) y (1,1).</span><span class="sxs-lookup"><span data-stu-id="988ec-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="988ec-109">Use \_ la posición D3DDECLUSAGE con un índice de uso de 0 para especificar la posición sin transformar para el procesamiento de vértices de función fija y el del teselador de n-patch.</span><span class="sxs-lookup"><span data-stu-id="988ec-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="988ec-110">Use \_ la posición D3DDECLUSAGE con un índice de uso de 1 para especificar la posición sin transformar en el sombreador de vértices de función fija para la interpolación de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="988ec-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-112">Mezclar datos de peso.</span><span class="sxs-lookup"><span data-stu-id="988ec-112">Blending weight data.</span></span> <span data-ttu-id="988ec-113">Use D3DDECLUSAGE \_ BLENDWEIGHT con un índice de uso de 0 para especificar los pesos de fusión utilizados en la mezcla de vértices indexados y no indexados.</span><span class="sxs-lookup"><span data-stu-id="988ec-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**</span><span class="sxs-lookup"><span data-stu-id="988ec-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-115">Mezclar datos de índices.</span><span class="sxs-lookup"><span data-stu-id="988ec-115">Blending indices data.</span></span> <span data-ttu-id="988ec-116">Use D3DDECLUSAGE \_ BLENDINDICES con un índice de uso de 0 para especificar índices de matriz para la numeración de paletas indizada.</span><span class="sxs-lookup"><span data-stu-id="988ec-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="988ec-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-118">Datos normales de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-118">Vertex normal data.</span></span> <span data-ttu-id="988ec-119">Use D3DDECLUSAGE \_ normal con un índice de uso de 0 para especificar las normales de vértices para el procesamiento de vértices de función fija y la del teselador de n-patch.</span><span class="sxs-lookup"><span data-stu-id="988ec-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="988ec-120">Use D3DDECLUSAGE \_ normal con un índice de uso de 1 para especificar las normales de vértices para el procesamiento de vértices de funciones fijas para la interpolación de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**</span><span class="sxs-lookup"><span data-stu-id="988ec-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-122">Datos de tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="988ec-122">Point size data.</span></span> <span data-ttu-id="988ec-123">Use D3DDECLUSAGE \_ PSIZE con un índice de uso de 0 para especificar el atributo de tamaño de punto que usa el motor de instalación del rasterizador para expandir un punto en un cuádruple para la funcionalidad de punto y Sprite.</span><span class="sxs-lookup"><span data-stu-id="988ec-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**</span><span class="sxs-lookup"><span data-stu-id="988ec-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-125">Datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="988ec-125">Texture coordinate data.</span></span> <span data-ttu-id="988ec-126">Use D3DDECLUSAGE \_ TEXCOORD, n para especificar coordenadas de textura en el procesamiento de vértices de función fija y en sombreadores de píxeles anteriores a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="988ec-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="988ec-127">Se pueden usar para pasar datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="988ec-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_Tangente D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="988ec-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-129">Datos de tangente de vértice.</span><span class="sxs-lookup"><span data-stu-id="988ec-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**\_BInormalización D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="988ec-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-131">Datos binormales de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**</span><span class="sxs-lookup"><span data-stu-id="988ec-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-133">Valor de punto flotante positivo único.</span><span class="sxs-lookup"><span data-stu-id="988ec-133">Single positive floating point value.</span></span> <span data-ttu-id="988ec-134">Use D3DDECLUSAGE \_ TESSFACTOR con un índice de uso de 0 para especificar un factor de teselación usado en la unidad de teselación para controlar la velocidad de teselación.</span><span class="sxs-lookup"><span data-stu-id="988ec-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="988ec-135">Para obtener más información sobre el tipo de datos, vea D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="988ec-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ posición**</span><span class="sxs-lookup"><span data-stu-id="988ec-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-137">Los datos de vértice contienen datos de posición transformados que van de (0,0) a (ancho de la ventanilla, alto de la ventanilla).</span><span class="sxs-lookup"><span data-stu-id="988ec-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="988ec-138">Utilice D3DDECLUSAGE \_ Position con un índice de uso de 0 para especificar la posición transformada.</span><span class="sxs-lookup"><span data-stu-id="988ec-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="988ec-139">Cuando se establece una declaración que contiene este, la canalización no realiza el procesamiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="988ec-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**COLOR de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="988ec-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-141">Los datos de vértice contienen colores difusos o especulares.</span><span class="sxs-lookup"><span data-stu-id="988ec-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="988ec-142">Use D3DDECLUSAGE \_ color con un índice de uso de 0 para especificar el color difuso en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="988ec-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="988ec-143">Use D3DDECLUSAGE \_ color con un índice de uso de 1 para especificar el color especular en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="988ec-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**Niebla de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="988ec-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-145">Los datos de vértice contienen datos de niebla.</span><span class="sxs-lookup"><span data-stu-id="988ec-145">Vertex data contains fog data.</span></span> <span data-ttu-id="988ec-146">Use \_ la niebla de D3DDECLUSAGE con un índice de uso de 0 para especificar un valor de mezcla de niebla usado después de que finalice el sombreado de píxeles.</span><span class="sxs-lookup"><span data-stu-id="988ec-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="988ec-147">Esto se aplica a los sombreadores de píxeles anteriores a la versión PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="988ec-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**Profundidad de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="988ec-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-149">Los datos de vértice contienen datos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="988ec-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="988ec-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**Ejemplo de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="988ec-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="988ec-151">Los datos de vértice contienen datos de muestra.</span><span class="sxs-lookup"><span data-stu-id="988ec-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="988ec-152">Use \_ el ejemplo D3DDECLUSAGE con un índice de uso de 0 para especificar el valor de desplazamiento que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="988ec-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="988ec-153">Solo se puede usar con D3DDECLUSAGE \_ LOOKUPPRESAMPLED o D3DDECLUSAGE \_ lookup.</span><span class="sxs-lookup"><span data-stu-id="988ec-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="988ec-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="988ec-154">Remarks</span></span>

<span data-ttu-id="988ec-155">Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="988ec-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="988ec-156">Cada elemento de la matriz contiene un tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="988ec-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="988ec-157">Para obtener más información sobre las declaraciones de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="988ec-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="988ec-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="988ec-158">Requirements</span></span>



| <span data-ttu-id="988ec-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="988ec-159">Requirement</span></span> | <span data-ttu-id="988ec-160">Value</span><span class="sxs-lookup"><span data-stu-id="988ec-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="988ec-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="988ec-161">Header</span></span><br/> | <dl> <span data-ttu-id="988ec-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="988ec-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="988ec-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="988ec-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988ec-164">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="988ec-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="988ec-165">Declaración de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="988ec-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




