---
description: Cree un Atlas UV para una malla.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Función D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717699"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="9ed47-103">D3DXUVAtlasCreate función)</span><span class="sxs-lookup"><span data-stu-id="9ed47-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="9ed47-104">Cree un Atlas UV para una malla.</span><span class="sxs-lookup"><span data-stu-id="9ed47-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ed47-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="9ed47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ed47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed47-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9ed47-109">Puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ed47-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="9ed47-110">Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="9ed47-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-111">*dwMaxChartNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-113">Número máximo de gráficos en los que se va a particionar la malla.</span><span class="sxs-lookup"><span data-stu-id="9ed47-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="9ed47-114">Vea comentarios sobre los modos de creación de particiones.</span><span class="sxs-lookup"><span data-stu-id="9ed47-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="9ed47-115">Use 0 para indicar a D3DX que el Atlas debe parametrizarse en función de Stretch.</span><span class="sxs-lookup"><span data-stu-id="9ed47-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-116">*fMaxStretch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-118">La cantidad de ajuste permitido.</span><span class="sxs-lookup"><span data-stu-id="9ed47-118">The amount of stretching allowed.</span></span> <span data-ttu-id="9ed47-119">0 significa que no se permite la expansión; 1 significa que se puede usar cualquier cantidad de ajuste.</span><span class="sxs-lookup"><span data-stu-id="9ed47-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-120">*dwWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-122">Ancho de la textura.</span><span class="sxs-lookup"><span data-stu-id="9ed47-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-123">*dwHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-125">Alto de textura.</span><span class="sxs-lookup"><span data-stu-id="9ed47-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-126">*fGutter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-128">Distancia mínima, en textura, entre dos gráficos en el Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ed47-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="9ed47-129">El margen se escala siempre por el ancho; por lo tanto, si se usa un medianil de 2,5 en una textura 512 x 512, la distancia mínima entre dos gráficos es 2,5/512,0 textura.</span><span class="sxs-lookup"><span data-stu-id="9ed47-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-130">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-132">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9ed47-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-133">*pdwAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-134">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ed47-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ed47-135">Puntero a una matriz de datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="9ed47-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="9ed47-136">con 3 DWORDs por caras, que indican qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="9ed47-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="9ed47-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed47-138">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ed47-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ed47-139">Una matriz con 3 DWORDs por caras.</span><span class="sxs-lookup"><span data-stu-id="9ed47-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="9ed47-140">Cada una de las caras indica si un borde es falso o no.</span><span class="sxs-lookup"><span data-stu-id="9ed47-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="9ed47-141">Un borde que no sea falso se indica mediante-1, un borde falso se indica con cualquier otro valor.</span><span class="sxs-lookup"><span data-stu-id="9ed47-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="9ed47-142">Esto permite la parametrización de una malla de cuádruples, donde los bordes inferiores a la mitad de cada cuádruple no se cortarán.</span><span class="sxs-lookup"><span data-stu-id="9ed47-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-143">*pfIMTArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-144">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ed47-145">Puntero a una matriz de decenas de métricas integrados que describe cómo expandir un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="9ed47-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-146">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-147">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="9ed47-148">Un puntero a una función de devolución de llamada (vea [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que es útil para supervisar el progreso.</span><span class="sxs-lookup"><span data-stu-id="9ed47-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-149">*fCallbackFrequency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-150">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-151">Especificar la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="9ed47-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-152">*pUserContent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-153">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-154">Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9ed47-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-155">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ed47-157">Especifique la calidad de los gráficos generados.</span><span class="sxs-lookup"><span data-stu-id="9ed47-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="9ed47-158">Vea [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="9ed47-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-159">*ppMeshOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-160">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9ed47-161">Puntero a la malla creada con el Atlas (vea [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="9ed47-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-162">*ppFacePartitioning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-163">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9ed47-164">Puntero a una matriz de los datos finales de partición de caras.</span><span class="sxs-lookup"><span data-stu-id="9ed47-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="9ed47-165">Cada elemento contiene un valor DWORD por cada tipo de letra (vea [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="9ed47-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-166">*ppVertexRemapArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-167">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9ed47-168">Puntero a una matriz de vértices reasignados.</span><span class="sxs-lookup"><span data-stu-id="9ed47-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="9ed47-169">Cada elemento de la matriz identifica el vértice original del que proceden los vértices finales (si el vértice se dividió durante la reasignación).</span><span class="sxs-lookup"><span data-stu-id="9ed47-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="9ed47-170">Cada elemento de la matriz contiene un valor DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="9ed47-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-171">*pfMaxStretchOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-172">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ed47-173">Puntero al valor de stretch máximo generado por el algoritmo de Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ed47-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="9ed47-174">El intervalo está comprendido entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="9ed47-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="9ed47-175">*pdwNumChartsOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ed47-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed47-176">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9ed47-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9ed47-177">Puntero al número de gráficos creados por el algoritmo de Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ed47-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="9ed47-178">Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un Atlas.</span><span class="sxs-lookup"><span data-stu-id="9ed47-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed47-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ed47-179">Return value</span></span>

<span data-ttu-id="9ed47-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ed47-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ed47-181">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9ed47-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed47-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ed47-182">Remarks</span></span>

<span data-ttu-id="9ed47-183">D3DXUVAtlasCreate puede crear particiones de la geometría de malla de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="9ed47-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="9ed47-184">Basado en el número de gráficos</span><span class="sxs-lookup"><span data-stu-id="9ed47-184">Based on the number of charts</span></span>
-   <span data-ttu-id="9ed47-185">Basado en el ajuste máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="9ed47-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="9ed47-186">Si el ajuste máximo permitido es 0, es probable que cada triángulo esté en su propio gráfico.</span><span class="sxs-lookup"><span data-stu-id="9ed47-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed47-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed47-187">Requirements</span></span>



| <span data-ttu-id="9ed47-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed47-188">Requirement</span></span> | <span data-ttu-id="9ed47-189">Value</span><span class="sxs-lookup"><span data-stu-id="9ed47-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed47-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ed47-190">Header</span></span><br/>  | <dl> <span data-ttu-id="9ed47-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed47-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9ed47-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ed47-192">Library</span></span><br/> | <dl> <span data-ttu-id="9ed47-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ed47-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ed47-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ed47-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed47-195">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="9ed47-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="9ed47-196">[Herramienta de Command-Line de Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9ed47-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
