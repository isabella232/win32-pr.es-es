---
description: 'Función D3DXUVAtlasPartition: cree un atlas UV para una malla.'
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Función D3DXUVAtlasPartition (D3DX9Mesh.h)
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
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117803"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="d93e1-103">Función D3DXUVAtlasPartition</span><span class="sxs-lookup"><span data-stu-id="d93e1-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="d93e1-104">Cree un atlas UV para una malla.</span><span class="sxs-lookup"><span data-stu-id="d93e1-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d93e1-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d93e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d93e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93e1-107">*pMesh* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="d93e1-109">Puntero a una malla de entrada (vea [**ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el atlas.</span><span class="sxs-lookup"><span data-stu-id="d93e1-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="d93e1-110">Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="d93e1-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-111">*dwMaxChartNumber* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-113">Número máximo de gráficos en los que se particiona la malla.</span><span class="sxs-lookup"><span data-stu-id="d93e1-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="d93e1-114">Vea los comentarios sobre los modos de creación de particiones.</span><span class="sxs-lookup"><span data-stu-id="d93e1-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="d93e1-115">Use 0 para decir a D3DX que el atlas debe parametrizarse en función de stretch.</span><span class="sxs-lookup"><span data-stu-id="d93e1-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-116">*fMaxStretch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-118">Cantidad de extensión permitida.</span><span class="sxs-lookup"><span data-stu-id="d93e1-118">The amount of stretching allowed.</span></span> <span data-ttu-id="d93e1-119">0 significa que no se permite ninguna extensión, 1 significa que se puede usar cualquier cantidad de extensión.</span><span class="sxs-lookup"><span data-stu-id="d93e1-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-120">*dwTextureIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-122">Índice de coordenadas de textura de base cero que identifica qué conjunto de coordenadas de textura usar.</span><span class="sxs-lookup"><span data-stu-id="d93e1-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-123">*pdwAdjacency* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-124">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d93e1-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d93e1-125">Puntero a una matriz de datos de adyacencia con 3 DWORD por cara, que indica qué triángulos son adyacentes entre sí (vea [**ID3DXBaseMesh::GenerateAdjacency).**](id3dxbasemesh--generateadjacency.md)</span><span class="sxs-lookup"><span data-stu-id="d93e1-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="d93e1-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="d93e1-127">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d93e1-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d93e1-128">Matriz con 3 DWORDS por cara.</span><span class="sxs-lookup"><span data-stu-id="d93e1-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="d93e1-129">Cada cara indica si un borde es false o no.</span><span class="sxs-lookup"><span data-stu-id="d93e1-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="d93e1-130">Un borde no falso se indica mediante -1, un borde falso se indica mediante cualquier otro valor.</span><span class="sxs-lookup"><span data-stu-id="d93e1-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="d93e1-131">Esto permite parametrizar una malla de quads en la que no se cortarán los bordes del centro de cada quad.</span><span class="sxs-lookup"><span data-stu-id="d93e1-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-132">*pfIMTArray* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d93e1-134">Puntero a una matriz de tensores de métricas integrados que describe cómo extender un triángulo (vea [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="d93e1-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-135">*pCallback* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-136">Tipo: **[LPD3DVATVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="d93e1-137">Puntero a una función de devolución de llamada [(vea LPD3D MOUSEVATLASCB)](lpd3dxuvatlascb.md)que resulta útil para supervisar el progreso.</span><span class="sxs-lookup"><span data-stu-id="d93e1-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-138">*fCallbackFrequency* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-139">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-140">Especifique la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="d93e1-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-141">*pUserContent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-142">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-143">Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d93e1-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-144">*dwOptions* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d93e1-146">Especifique la calidad de los gráficos generados mediante la combinación de una o varias [**marcas D3D PRECISELAS.**](./d3dxuvatlas.md)</span><span class="sxs-lookup"><span data-stu-id="d93e1-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-147">*ppMeshOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-148">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d93e1-149">Puntero a la malla creada con el atlas (vea [**ID3DXMesh).**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="d93e1-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-150">*pFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="d93e1-152">Puntero a una matriz de los datos finales de partición de caras.</span><span class="sxs-lookup"><span data-stu-id="d93e1-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="d93e1-153">Cada elemento contiene un DWORD por cara (vea [**ID3DXBuffer).**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d93e1-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-154">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-155">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d93e1-156">Puntero a una matriz de vértices recortados.</span><span class="sxs-lookup"><span data-stu-id="d93e1-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="d93e1-157">Cada elemento de matriz identifica el vértice original del que provenía cada vértice final (si el vértice se dividió durante la remapping).</span><span class="sxs-lookup"><span data-stu-id="d93e1-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="d93e1-158">Cada elemento de matriz contiene un DWORD por vértice.</span><span class="sxs-lookup"><span data-stu-id="d93e1-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="d93e1-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="d93e1-160">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d93e1-161">Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d93e1-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="d93e1-162">Este búfer contendrá una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara en la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="d93e1-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="d93e1-163">Este parámetro no debe ser **NULL,** porque la llamada posterior a D3DXUVAtlasPack() lo requiere.</span><span class="sxs-lookup"><span data-stu-id="d93e1-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-164">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-165">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d93e1-166">Puntero al valor de stretch máximo generado por el algoritmo atlas.</span><span class="sxs-lookup"><span data-stu-id="d93e1-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="d93e1-167">El intervalo está entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="d93e1-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-168">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d93e1-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d93e1-169">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d93e1-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d93e1-170">Puntero al número de gráficos creados por el algoritmo atlas.</span><span class="sxs-lookup"><span data-stu-id="d93e1-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="d93e1-171">Si dwMaxChartNumber es demasiado bajo, este parámetro devolverá el número mínimo de gráficos necesarios para crear un atlas.</span><span class="sxs-lookup"><span data-stu-id="d93e1-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93e1-172">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d93e1-172">Return value</span></span>

<span data-ttu-id="d93e1-173">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d93e1-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d93e1-174">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d93e1-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d93e1-175">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d93e1-175">Remarks</span></span>

<span data-ttu-id="d93e1-176">D3DXUVAtlasPartition es similar a [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)salvo que D3DXUVAtlasPartition no realiza el paso de empaquetado final.</span><span class="sxs-lookup"><span data-stu-id="d93e1-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="d93e1-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d93e1-177">Requirements</span></span>



| <span data-ttu-id="d93e1-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="d93e1-178">Requirement</span></span> | <span data-ttu-id="d93e1-179">Value</span><span class="sxs-lookup"><span data-stu-id="d93e1-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d93e1-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d93e1-180">Header</span></span><br/>  | <dl> <span data-ttu-id="d93e1-181"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="d93e1-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d93e1-182">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d93e1-182">Library</span></span><br/> | <dl> <span data-ttu-id="d93e1-183"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d93e1-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d93e1-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d93e1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e1-185">Funciones UVAtlas</span><span class="sxs-lookup"><span data-stu-id="d93e1-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="d93e1-186">[Herramienta de Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d93e1-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
