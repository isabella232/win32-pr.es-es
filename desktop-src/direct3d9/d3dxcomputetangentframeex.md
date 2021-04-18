---
description: Realiza cálculos de fotogramas tangentes en una malla. Se generan vectores de tangente, binormalización y, opcionalmente, normales. Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Función D3DXComputeTangentFrameEx (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717639"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="48e3b-105">D3DXComputeTangentFrameEx función)</span><span class="sxs-lookup"><span data-stu-id="48e3b-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="48e3b-106">Realiza cálculos de fotogramas tangentes en una malla.</span><span class="sxs-lookup"><span data-stu-id="48e3b-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="48e3b-107">Se generan vectores de tangente, binormalización y, opcionalmente, normales.</span><span class="sxs-lookup"><span data-stu-id="48e3b-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="48e3b-108">Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices.</span><span class="sxs-lookup"><span data-stu-id="48e3b-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e3b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48e3b-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="48e3b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48e3b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e3b-111">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-112">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="48e3b-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="48e3b-113">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="48e3b-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-114">*dwTextureInSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-116">Especifica la semántica de entrada de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="48e3b-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="48e3b-117">Si \_ el valor predeterminado de D3DX es, la función supone que no hay ninguna coordenadas de textura y se producirá un error en la función a menos que se especifique el cálculo del vector normal.</span><span class="sxs-lookup"><span data-stu-id="48e3b-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-118">*dwTextureInIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-120">Si una malla tiene varias coordenadas de textura, especifica la coordenada de textura que se va a usar para los cálculos de fotogramas tangentes.</span><span class="sxs-lookup"><span data-stu-id="48e3b-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="48e3b-121">Si el valor es cero, la malla solo tiene una coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="48e3b-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-122">*dwUPartialOutSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-124">Especifica la semántica de salida para el tipo, normalmente D3DDECLUSAGE \_ tangente, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura U.</span><span class="sxs-lookup"><span data-stu-id="48e3b-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="48e3b-125">Si \_ el valor predeterminado de D3DX es, este derivado parcial no se almacenará.</span><span class="sxs-lookup"><span data-stu-id="48e3b-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-126">*dwUPartialOutIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-128">Especifica el índice semántico en el que se almacena el derivado parcial con respecto a la coordenada de textura U.</span><span class="sxs-lookup"><span data-stu-id="48e3b-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-129">*dwVPartialOutSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-131">Especifica el tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , normalmente D3DDECLUSAGE \_ binormal, que describe dónde se almacenará el derivado parcial con respecto a la coordenada de textura V.</span><span class="sxs-lookup"><span data-stu-id="48e3b-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="48e3b-132">Si \_ el valor predeterminado de D3DX es, este derivado parcial no se almacenará.</span><span class="sxs-lookup"><span data-stu-id="48e3b-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-133">*dwVPartialOutIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-135">Especifica el índice semántico en el que se almacena el derivado parcial con respecto a la coordenada de textura V.</span><span class="sxs-lookup"><span data-stu-id="48e3b-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-136">*dwNormalOutSemantic* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-138">Especifica la semántica normal de salida, normalmente D3DDECLUSAGE \_ normal, que describe dónde se almacenará el vector normal en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="48e3b-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="48e3b-139">Si \_ el valor predeterminado de D3DX es, este vector normal no se almacenará.</span><span class="sxs-lookup"><span data-stu-id="48e3b-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-140">*dwNormalOutIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-142">Especifica el índice semántico en el que se va a almacenar el vector normal en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="48e3b-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-143">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-145">Combinación de una o varias marcas [**D3DXTANGENT**](./d3dxtangent.md) que especifican las opciones de cálculo de fotogramas tangentes.</span><span class="sxs-lookup"><span data-stu-id="48e3b-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="48e3b-146">Si **es null**, se especificarán las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="48e3b-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="48e3b-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="48e3b-147">Description</span></span>                                                                                              | <span data-ttu-id="48e3b-148">[**D3DXTANGENT**](./d3dxtangent.md) Valor de marca</span><span class="sxs-lookup"><span data-stu-id="48e3b-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="48e3b-149">Pondera la longitud del vector normal por el ángulo, en radianes, que se repite en los dos bordes que abandonan el vértice.</span><span class="sxs-lookup"><span data-stu-id="48e3b-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="48e3b-150">&. (D3DXTANGENT \_ PESO \_ por \_ área \| D3DXTANGENT \_ peso \_ igual)</span><span class="sxs-lookup"><span data-stu-id="48e3b-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="48e3b-151">Calcular coordenadas cartesianas ortogonales a partir de coordenadas de textura (u, v).</span><span class="sxs-lookup"><span data-stu-id="48e3b-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="48e3b-152">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="48e3b-152">See Remarks.</span></span>                   | <span data-ttu-id="48e3b-153">&. (D3DXTANGENT \_ ORTOGONAL \_ desde \_ U \| D3DXTANGENT \_ ortogonal \_ desde \_ V)</span><span class="sxs-lookup"><span data-stu-id="48e3b-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="48e3b-154">Las texturas no se ajustan en las direcciones u o v</span><span class="sxs-lookup"><span data-stu-id="48e3b-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="48e3b-155">&. (D3DXTANGENT \_ ENCAPSULAdo \_ UV)</span><span class="sxs-lookup"><span data-stu-id="48e3b-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="48e3b-156">Se normalizan las derivadas parciales con respecto a las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="48e3b-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="48e3b-157">&. (D3DXTANGENT \_ no \_ normalizar \_ parciales)</span><span class="sxs-lookup"><span data-stu-id="48e3b-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="48e3b-158">Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="48e3b-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="48e3b-159">&. (D3DXTANGENT \_ VIENTO \_ CW)</span><span class="sxs-lookup"><span data-stu-id="48e3b-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="48e3b-160">Use vectores normales por vértice ya presentes en la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="48e3b-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="48e3b-161">&. (D3DXTANGENT \_ CALCULAR \_ normales)</span><span class="sxs-lookup"><span data-stu-id="48e3b-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="48e3b-162">Si \_ \_ \_ no se establece D3DXTANGENT generar en contexto, la malla de entrada se clona.</span><span class="sxs-lookup"><span data-stu-id="48e3b-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="48e3b-163">Por lo tanto, la malla original debe tener espacio suficiente para almacenar el vector normal calculado y los datos derivados parciales.</span><span class="sxs-lookup"><span data-stu-id="48e3b-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-164">*pdwAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-165">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="48e3b-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48e3b-166">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="48e3b-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="48e3b-167">El número de bytes de esta matriz debe ser de al menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="48e3b-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-168">*fPartialEdgeThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-169">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-170">Especifica el coseno máximo del ángulo en el que dos derivados parciales se consideran incompatibles entre sí.</span><span class="sxs-lookup"><span data-stu-id="48e3b-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="48e3b-171">Si el producto de punto de la dirección de los dos derivados parciales de triángulos adyacentes es menor o igual que este umbral, los vértices compartidos entre estos triángulos se dividirán.</span><span class="sxs-lookup"><span data-stu-id="48e3b-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-172">*fSingularPointThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-173">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-174">Especifica la magnitud máxima de un derivado parcial en el que un vértice se considerará singular.</span><span class="sxs-lookup"><span data-stu-id="48e3b-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="48e3b-175">Dado que varios triángulos son incidentes en un punto que tiene fotogramas tangentes cercanos, pero que se cancelan entre sí (por ejemplo, en la parte superior de una esfera), la magnitud del derivado parcial disminuirá.</span><span class="sxs-lookup"><span data-stu-id="48e3b-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="48e3b-176">Si la magnitud es menor o igual que este umbral, el vértice se dividirá para cada triángulo que lo contenga.</span><span class="sxs-lookup"><span data-stu-id="48e3b-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-177">*fNormalEdgeThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-178">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e3b-179">Similar a fPartialEdgeThreshold, especifica el coseno máximo del ángulo entre dos normales que es un umbral más allá del cual se dividirán los vértices compartidos entre triángulos.</span><span class="sxs-lookup"><span data-stu-id="48e3b-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="48e3b-180">Si el producto de punto de las dos normales es inferior al umbral, se dividirán los vértices compartidos, formando un borde duro entre los triángulos vecinos.</span><span class="sxs-lookup"><span data-stu-id="48e3b-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="48e3b-181">Si el producto de punto es mayor que el umbral, se interpolarán sus normales triángulos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="48e3b-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-182">*ppMeshOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-183">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="48e3b-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="48e3b-184">Dirección de un puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida que recibe los datos de vector de la tangente calculada, binormalización y normal.</span><span class="sxs-lookup"><span data-stu-id="48e3b-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="48e3b-185">*ppVertexMapping* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48e3b-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e3b-186">Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="48e3b-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="48e3b-187">Dirección de un puntero a un objeto de búfer de [**ID3DXBuffer**](id3dxbuffer.md) de salida que recibe una asignación de los nuevos vértices calculados por este método para los vértices originales.</span><span class="sxs-lookup"><span data-stu-id="48e3b-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="48e3b-188">El búfer es una matriz de DWORDs, con el tamaño de la matriz definido como el número de vértices en ppMeshOut.</span><span class="sxs-lookup"><span data-stu-id="48e3b-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e3b-189">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48e3b-189">Return value</span></span>

<span data-ttu-id="48e3b-190">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48e3b-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48e3b-191">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48e3b-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="48e3b-192">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="48e3b-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e3b-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48e3b-193">Remarks</span></span>

<span data-ttu-id="48e3b-194">Una versión simplificada de esta función está disponible como [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span><span class="sxs-lookup"><span data-stu-id="48e3b-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="48e3b-195">El vector normal calculado en cada vértice siempre se normaliza para tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="48e3b-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="48e3b-196">La solución más sólida para calcular coordenadas cartesianos ortogonales consiste en no establecer marcas D3DXTANGENT \_ ortogonales \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V, de modo que las coordenadas ortogonales se calculan a partir de las coordenadas de textura que usted y V.</span><span class="sxs-lookup"><span data-stu-id="48e3b-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="48e3b-197">Sin embargo, en este caso, si u o v es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ortogonal \_ desde \_ v o D3DXTANGENT se \_ ortogonala \_ desde \_ u, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="48e3b-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e3b-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48e3b-198">Requirements</span></span>



| <span data-ttu-id="48e3b-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e3b-199">Requirement</span></span> | <span data-ttu-id="48e3b-200">Value</span><span class="sxs-lookup"><span data-stu-id="48e3b-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e3b-201">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48e3b-201">Header</span></span><br/>  | <dl> <span data-ttu-id="48e3b-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e3b-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="48e3b-203">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48e3b-203">Library</span></span><br/> | <dl> <span data-ttu-id="48e3b-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48e3b-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48e3b-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="48e3b-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e3b-206">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="48e3b-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="48e3b-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="48e3b-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
