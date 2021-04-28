---
description: 'Función D3DXUVAtlasCreate: cree un atlas UV para una malla.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Función D3DXUVAtlasCreate (D3DX9Mesh.h)
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
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117833"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="a1d1d-103">Función D3DXUVAtlasCreate</span><span class="sxs-lookup"><span data-stu-id="a1d1d-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="a1d1d-104">Cree un atlas UV para una malla.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1d1d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a1d1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d1d-107">*pMesh* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a1d1d-109">Puntero a una malla de entrada (vea [**ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el atlas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="a1d1d-110">Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-111">*dwMaxChartNumber* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-113">Número máximo de gráficos en los que se particiona la malla.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="a1d1d-114">Vea comentarios sobre los modos de creación de particiones.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="a1d1d-115">Use 0 para decir a D3DX que el atlas debe parametrizarse en función de stretch.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-116">*fMaxStretch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-118">Cantidad de extensión permitida.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-118">The amount of stretching allowed.</span></span> <span data-ttu-id="a1d1d-119">0 significa que no se permite ningún stretching, 1 significa que se puede usar cualquier cantidad de stretching.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-120">*dwWidth* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-121">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-122">Ancho de textura.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-123">*dwHeight* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-124">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-125">Alto de textura.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-126">*fGutter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-128">Distancia mínima, en texturas, entre dos gráficos en el atlas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="a1d1d-129">El ancho del medianía siempre se escala; por lo tanto, si se usa un medianera de 2,5 en una textura de 512 x 512, la distancia mínima entre dos gráficos es de 2,5 / 512,0 texturas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-130">*dwTextureIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-132">Índice de coordenadas de textura de base cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-133">*pdwAdjacency* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-134">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1d1d-135">Puntero a una matriz de datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="a1d1d-136">con 3 DWORD por cara, lo que indica qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="a1d1d-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="a1d1d-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d1d-138">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1d1d-139">Matriz con 3 DWORDS por cara.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="a1d1d-140">Cada cara indica si un borde es false o no.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="a1d1d-141">Un borde no falso se indica mediante -1, un borde falso se indica mediante cualquier otro valor.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="a1d1d-142">Esto permite parametrizar una malla de cuádros donde no se cortarán los bordes del centro de cada quad.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-143">*pfIMTArray* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-144">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1d1d-145">Puntero a una matriz de tensores de métricas integrados que describe cómo extender un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="a1d1d-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-146">*pCallback* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-147">Tipo: **[LPD3DVATVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="a1d1d-148">Puntero a una función de devolución de llamada [(vea LPD3D MOUSEVATLASCB)](lpd3dxuvatlascb.md)que resulta útil para supervisar el progreso.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-149">*fCallbackFrequency* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-150">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-151">Especifique la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-152">*pUserContent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-153">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-154">Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-155">*dwOptions* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1d1d-157">Especifique la calidad de los gráficos generados.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="a1d1d-158">Vea [**D3DVATVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="a1d1d-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-159">*ppMeshOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-160">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a1d1d-161">Puntero a la malla creada con el atlas [**(vea ID3DXMesh).**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="a1d1d-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-162">*ppFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-163">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a1d1d-164">Puntero a una matriz de los datos finales de partición de caras.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="a1d1d-165">Cada elemento contiene un DWORD por cara (vea [**ID3DXBuffer).**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a1d1d-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-166">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-167">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a1d1d-168">Puntero a una matriz de vértices recortados.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="a1d1d-169">Cada elemento de matriz identifica el vértice original del que provenía cada vértice final (si el vértice se dividió durante el remapping).</span><span class="sxs-lookup"><span data-stu-id="a1d1d-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="a1d1d-170">Cada elemento de matriz contiene un DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-171">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-172">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1d1d-173">Puntero al valor de stretch máximo generado por el algoritmo atlas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="a1d1d-174">El intervalo está entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="a1d1d-175">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1d1d-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1d1d-176">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1d1d-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1d1d-177">Puntero al número de gráficos creados por el algoritmo atlas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="a1d1d-178">Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un atlas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d1d-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1d1d-179">Return value</span></span>

<span data-ttu-id="a1d1d-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1d1d-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1d1d-181">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d1d-182">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1d1d-182">Remarks</span></span>

<span data-ttu-id="a1d1d-183">D3DXUVAtlasCreate puede particionar la geometría de malla de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="a1d1d-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="a1d1d-184">En función del número de gráficos</span><span class="sxs-lookup"><span data-stu-id="a1d1d-184">Based on the number of charts</span></span>
-   <span data-ttu-id="a1d1d-185">En función del límite máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="a1d1d-186">Si el stretch máximo permitido es 0, es probable que cada triángulo esté en su propio gráfico.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d1d-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1d1d-187">Requirements</span></span>



| <span data-ttu-id="a1d1d-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1d1d-188">Requirement</span></span> | <span data-ttu-id="a1d1d-189">Value</span><span class="sxs-lookup"><span data-stu-id="a1d1d-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d1d-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1d1d-190">Header</span></span><br/>  | <dl> <span data-ttu-id="a1d1d-191"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="a1d1d-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a1d1d-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1d1d-192">Library</span></span><br/> | <dl> <span data-ttu-id="a1d1d-193"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1d1d-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1d1d-194">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a1d1d-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d1d-195">Funciones UVAtlas</span><span class="sxs-lookup"><span data-stu-id="a1d1d-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="a1d1d-196">[Herramienta de Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="a1d1d-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
