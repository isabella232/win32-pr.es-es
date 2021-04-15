---
description: Cree un Atlas UV para una malla.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Función D3DXUVAtlasPartition (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707862"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="0629d-103">D3DXUVAtlasPartition función)</span><span class="sxs-lookup"><span data-stu-id="0629d-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="0629d-104">Cree un Atlas UV para una malla.</span><span class="sxs-lookup"><span data-stu-id="0629d-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0629d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0629d-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="0629d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0629d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0629d-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0629d-109">Puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el Atlas.</span><span class="sxs-lookup"><span data-stu-id="0629d-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="0629d-110">Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="0629d-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-111">*dwMaxChartNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-113">Número máximo de gráficos en los que se va a particionar la malla.</span><span class="sxs-lookup"><span data-stu-id="0629d-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="0629d-114">Vea comentarios sobre los modos de creación de particiones.</span><span class="sxs-lookup"><span data-stu-id="0629d-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="0629d-115">Use 0 para indicar a D3DX que el Atlas debe parametrizarse en función de Stretch.</span><span class="sxs-lookup"><span data-stu-id="0629d-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-116">*fMaxStretch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-118">La cantidad de ajuste permitido.</span><span class="sxs-lookup"><span data-stu-id="0629d-118">The amount of stretching allowed.</span></span> <span data-ttu-id="0629d-119">0 significa que no se permite la expansión; 1 significa que se puede usar cualquier cantidad de ajuste.</span><span class="sxs-lookup"><span data-stu-id="0629d-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-120">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-122">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0629d-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-123">*pdwAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-124">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0629d-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0629d-125">Puntero a una matriz de datos de adyacencia con 3 DWORDs por caras, que indica qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="0629d-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0629d-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="0629d-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="0629d-127">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0629d-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0629d-128">Una matriz con 3 DWORDs por caras.</span><span class="sxs-lookup"><span data-stu-id="0629d-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="0629d-129">Cada una de las caras indica si un borde es falso o no.</span><span class="sxs-lookup"><span data-stu-id="0629d-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="0629d-130">Un borde que no sea falso se indica mediante-1, un borde falso se indica con cualquier otro valor.</span><span class="sxs-lookup"><span data-stu-id="0629d-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="0629d-131">Esto permite la parametrización de una malla de cuádruples, donde los bordes inferiores a la mitad de cada cuádruple no se cortarán.</span><span class="sxs-lookup"><span data-stu-id="0629d-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-132">*pfIMTArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0629d-134">Puntero a una matriz de decenas de métricas integrados que describe cómo expandir un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="0629d-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0629d-135">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="0629d-137">Un puntero a una función de devolución de llamada (vea [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que es útil para supervisar el progreso.</span><span class="sxs-lookup"><span data-stu-id="0629d-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-138">*fCallbackFrequency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-139">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-140">Especificar la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="0629d-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-141">*pUserContent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-142">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-143">Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0629d-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-144">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0629d-146">Especifique la calidad de los gráficos generados mediante la combinación de una o varias marcas de [**D3DXUVATLAS**](./d3dxuvatlas.md) .</span><span class="sxs-lookup"><span data-stu-id="0629d-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-147">*ppMeshOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0629d-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-148">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0629d-149">Puntero a la malla creada con el Atlas (vea [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="0629d-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0629d-150">*pFacePartitioning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0629d-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="0629d-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="0629d-152">Puntero a una matriz de los datos finales de partición de caras.</span><span class="sxs-lookup"><span data-stu-id="0629d-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="0629d-153">Cada elemento contiene un valor DWORD por cada tipo de letra (vea [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="0629d-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0629d-154">*ppVertexRemapArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0629d-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-155">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0629d-156">Puntero a una matriz de vértices reasignados.</span><span class="sxs-lookup"><span data-stu-id="0629d-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="0629d-157">Cada elemento de la matriz identifica el vértice original del que proceden los vértices finales (si el vértice se dividió durante la reasignación).</span><span class="sxs-lookup"><span data-stu-id="0629d-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="0629d-158">Cada elemento de la matriz contiene un valor DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="0629d-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="0629d-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="0629d-160">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0629d-161">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0629d-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0629d-162">Este búfer contendrá una matriz de tres DWORD por cada tipo que especifique los tres vecinos para cada una de las caras de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="0629d-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="0629d-163">Este parámetro no debe ser **null**, ya que la siguiente llamada a D3DXUVAtlasPack () lo requiere.</span><span class="sxs-lookup"><span data-stu-id="0629d-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-164">*pfMaxStretchOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0629d-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-165">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0629d-166">Puntero al valor de stretch máximo generado por el algoritmo de Atlas.</span><span class="sxs-lookup"><span data-stu-id="0629d-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="0629d-167">El intervalo está comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="0629d-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="0629d-168">*pdwNumChartsOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0629d-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0629d-169">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0629d-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0629d-170">Puntero al número de gráficos creados por el algoritmo de Atlas.</span><span class="sxs-lookup"><span data-stu-id="0629d-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="0629d-171">Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un Atlas.</span><span class="sxs-lookup"><span data-stu-id="0629d-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0629d-172">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0629d-172">Return value</span></span>

<span data-ttu-id="0629d-173">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0629d-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0629d-174">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0629d-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0629d-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0629d-175">Remarks</span></span>

<span data-ttu-id="0629d-176">D3DXUVAtlasPartition es similar a [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), salvo que D3DXUVAtlasPartition no realiza el paso de empaquetado final.</span><span class="sxs-lookup"><span data-stu-id="0629d-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="0629d-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0629d-177">Requirements</span></span>



| <span data-ttu-id="0629d-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="0629d-178">Requirement</span></span> | <span data-ttu-id="0629d-179">Value</span><span class="sxs-lookup"><span data-stu-id="0629d-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0629d-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0629d-180">Header</span></span><br/>  | <dl> <span data-ttu-id="0629d-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0629d-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0629d-182">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0629d-182">Library</span></span><br/> | <dl> <span data-ttu-id="0629d-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0629d-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0629d-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="0629d-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0629d-185">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="0629d-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="0629d-186">[Herramienta de Command-Line de Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0629d-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
