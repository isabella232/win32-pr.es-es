---
description: Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo. Este método reordena la malla existente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh:: OptimizeInplace (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821426"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="a9fa8-104">ID3DXMesh:: OptimizeInplace (método)</span><span class="sxs-lookup"><span data-stu-id="a9fa8-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="a9fa8-105">Genera una malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="a9fa8-106">Este método reordena la malla existente.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fa8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9fa8-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="a9fa8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9fa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fa8-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a9fa8-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fa8-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9fa8-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9fa8-111">Combinación de una o varias marcas [**D3DXMESHOPT**](./d3dxmeshopt.md) , especificando el tipo de optimización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa8-112">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9fa8-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fa8-113">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9fa8-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9fa8-114">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="a9fa8-115">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa8-116">*pAdjacencyOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9fa8-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fa8-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fa8-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9fa8-118">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="a9fa8-119">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="a9fa8-120">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa8-121">*pFaceRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9fa8-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fa8-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fa8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9fa8-123">Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="a9fa8-124">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="a9fa8-125">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9fa8-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9fa8-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9fa8-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a9fa8-127">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="a9fa8-128">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="a9fa8-129">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fa8-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9fa8-130">Return value</span></span>

<span data-ttu-id="a9fa8-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9fa8-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9fa8-132">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9fa8-133">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9fa8-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9fa8-134">Remarks</span></span>

<span data-ttu-id="a9fa8-135">Antes de ejecutar **ID3DXMesh:: OptimizeInplace**, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="a9fa8-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="a9fa8-136">El búfer de adyacencia contiene datos de adyacencias, como una lista de bordes y las caras adyacentes entre sí.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="a9fa8-137">Este método producirá un error si la malla comparte su búfer de vértice con otra malla, a menos que el \_ IGNOREVERTS de D3DXMESHOPT se establezca en marcas.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9fa8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9fa8-138">Requirements</span></span>



| <span data-ttu-id="a9fa8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9fa8-139">Requirement</span></span> | <span data-ttu-id="a9fa8-140">Value</span><span class="sxs-lookup"><span data-stu-id="a9fa8-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fa8-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9fa8-141">Header</span></span><br/>  | <dl> <span data-ttu-id="a9fa8-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fa8-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a9fa8-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9fa8-143">Library</span></span><br/> | <dl> <span data-ttu-id="a9fa8-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9fa8-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9fa8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9fa8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fa8-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="a9fa8-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="a9fa8-147">**ID3DXMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="a9fa8-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
