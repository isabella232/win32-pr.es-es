---
description: Divide una malla en mallas menores que el tamaño especificado.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Función D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717734"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="28008-103">D3DXSplitMesh función)</span><span class="sxs-lookup"><span data-stu-id="28008-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="28008-104">Divide una malla en mallas menores que el tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="28008-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="28008-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28008-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="28008-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28008-107">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28008-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="28008-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="28008-109">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="28008-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="28008-110">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28008-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="28008-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="28008-112">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla que se van a simplificar.</span><span class="sxs-lookup"><span data-stu-id="28008-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="28008-113">*MaxSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28008-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28008-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28008-115">Número máximo de vértices en la malla resultante.</span><span class="sxs-lookup"><span data-stu-id="28008-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="28008-116">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="28008-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28008-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28008-118">Marcas de opciones para las nuevas mallas.</span><span class="sxs-lookup"><span data-stu-id="28008-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="28008-119">*pMeshesOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28008-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="28008-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="28008-121">Número de mallas devueltas.</span><span class="sxs-lookup"><span data-stu-id="28008-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="28008-122">*ppMeshArrayOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28008-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28008-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28008-124">Búfer que contiene una matriz de interfaces [**ID3DXMesh**](id3dxmesh.md) para las nuevas mallas.</span><span class="sxs-lookup"><span data-stu-id="28008-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="28008-125">Para una división de la malla de origen en n mallas, *ppMeshArrayOut* es una matriz de n punteros **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="28008-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="28008-126">*ppAdjacencyArrayOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28008-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28008-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28008-128">Búfer que contiene una matriz de matrices de adyacencias (DWORDs) para las nuevas mallas.</span><span class="sxs-lookup"><span data-stu-id="28008-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="28008-129">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="28008-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="28008-130">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="28008-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="28008-131">*ppFaceRemapArrayOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28008-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28008-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28008-133">Búfer que contiene una matriz de matrices de reasignación de caras (DWORDs) para las nuevas mallas.</span><span class="sxs-lookup"><span data-stu-id="28008-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="28008-134">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="28008-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="28008-135">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="28008-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="28008-136">*ppVertRemapArrayOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28008-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28008-137">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="28008-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="28008-138">Búfer que contiene una matriz de matrices de reasignación de vértices para las nuevas mallas.</span><span class="sxs-lookup"><span data-stu-id="28008-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="28008-139">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="28008-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="28008-140">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="28008-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28008-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28008-141">Return value</span></span>

<span data-ttu-id="28008-142">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28008-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="28008-143">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="28008-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="28008-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28008-144">Remarks</span></span>

<span data-ttu-id="28008-145">Un uso común de esta función es dividir una malla con índices de 32 bits (más de 65535 vértices) en más de una malla, cada una de las cuales tiene índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="28008-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="28008-146">Las matrices de tipo adyacencia, reasignación de vértices y asignación de caras son matrices son DWORDs donde cada matriz contiene n punteros DWORD, seguidos de los datos DWORD a los que hacen referencia los punteros.</span><span class="sxs-lookup"><span data-stu-id="28008-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="28008-147">Por ejemplo, para obtener la información de reasignación de caras de la esfera 3 de la malla 2, se podría usar el código siguiente, suponiendo que los datos de reasignación de caras se devolvieron en una variable denominada *ppFaceRemapArrayOut*.</span><span class="sxs-lookup"><span data-stu-id="28008-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="28008-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28008-148">Requirements</span></span>



| <span data-ttu-id="28008-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="28008-149">Requirement</span></span> | <span data-ttu-id="28008-150">Value</span><span class="sxs-lookup"><span data-stu-id="28008-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28008-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28008-151">Header</span></span><br/>  | <dl> <span data-ttu-id="28008-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="28008-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="28008-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28008-153">Library</span></span><br/> | <dl> <span data-ttu-id="28008-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28008-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28008-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="28008-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28008-156">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="28008-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
