---
description: Calcula las normales de unidad para cada vértice de una malla. Proporcionado para admitir aplicaciones heredadas. Use D3DXComputeTangentFrameEx para obtener mejores resultados.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Función D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003868"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="79107-105">D3DXComputeNormals función)</span><span class="sxs-lookup"><span data-stu-id="79107-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="79107-106">Calcula las normales de unidad para cada vértice de una malla.</span><span class="sxs-lookup"><span data-stu-id="79107-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="79107-107">Proporcionado para admitir aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="79107-107">Provided to support legacy applications.</span></span> <span data-ttu-id="79107-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obtener mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="79107-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="79107-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79107-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="79107-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79107-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79107-111">*pmesh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="79107-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="79107-112">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="79107-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="79107-113">Puntero a una interfaz [**ID3DXBaseMesh**](id3dxbasemesh.md) que representa el objeto de malla normalizado.</span><span class="sxs-lookup"><span data-stu-id="79107-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="79107-114">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79107-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79107-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="79107-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79107-116">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla progresiva creada.</span><span class="sxs-lookup"><span data-stu-id="79107-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="79107-117">Este parámetro es opcional y debe establecerse en **null** si no se usa.</span><span class="sxs-lookup"><span data-stu-id="79107-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79107-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79107-118">Return value</span></span>

<span data-ttu-id="79107-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79107-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79107-120">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79107-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="79107-121">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="79107-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="79107-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79107-122">Remarks</span></span>

<span data-ttu-id="79107-123">La malla de entrada debe tener la marca [D3DFVF \_ normal](d3dfvf.md) especificada en su formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="79107-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="79107-124">La normalización de un vértice se genera al calcular el promedio de las normales de todas las caras que comparten dicho vértice.</span><span class="sxs-lookup"><span data-stu-id="79107-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="79107-125">Si se proporciona adyacencia, se omiten los vértices replicados y se "suavizan".</span><span class="sxs-lookup"><span data-stu-id="79107-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="79107-126">Si no se proporciona la adyacencia, los vértices replicados tendrán un promedio de normalización de solo los rostros a los que se hace referencia explícitamente.</span><span class="sxs-lookup"><span data-stu-id="79107-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="79107-127">Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="79107-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="79107-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79107-128">Requirements</span></span>



| <span data-ttu-id="79107-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="79107-129">Requirement</span></span> | <span data-ttu-id="79107-130">Value</span><span class="sxs-lookup"><span data-stu-id="79107-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79107-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79107-131">Header</span></span><br/>  | <dl> <span data-ttu-id="79107-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="79107-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="79107-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79107-133">Library</span></span><br/> | <dl> <span data-ttu-id="79107-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79107-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79107-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="79107-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79107-136">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="79107-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
