---
description: Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Método ID3DXMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003984"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="84442-103">ID3DXMesh:: Optimize (método)</span><span class="sxs-lookup"><span data-stu-id="84442-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="84442-104">Genera una nueva malla con caras y vértices reordenados para optimizar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="84442-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="84442-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84442-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="84442-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84442-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84442-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="84442-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84442-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84442-109">Especifica el tipo de optimización que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="84442-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="84442-110">Este parámetro se puede establecer en una combinación de una o varias marcas de [**D3DXMESHOPT**](./d3dxmeshopt.md) y [**D3DXMESH**](./d3dxmesh.md) (excepto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WRITEONLY y D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="84442-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="84442-111">*pAdjacencyIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84442-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-112">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="84442-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84442-113">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="84442-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="84442-114">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="84442-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="84442-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="84442-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="84442-116">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84442-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84442-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84442-118">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="84442-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="84442-119">Si el borde no tiene caras adyacentes, el valor es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="84442-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="84442-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84442-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84442-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84442-122">Matriz de DWORDs, una por cada tipo, que identifica la superficie de la malla original que corresponde a cada una de las caras de la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="84442-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="84442-123">Si el valor proporcionado para este argumento es **null**, no se devuelven los datos de reasignación de caras.</span><span class="sxs-lookup"><span data-stu-id="84442-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="84442-124">*ppVertexRemap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84442-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="84442-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="84442-126">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene un valor DWORD para cada vértice que especifica cómo se asignan los nuevos vértices a los vértices anteriores.</span><span class="sxs-lookup"><span data-stu-id="84442-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="84442-127">Esta reasignación es útil si necesita modificar los datos externos en función de la nueva asignación de vértices.</span><span class="sxs-lookup"><span data-stu-id="84442-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="84442-128">*ppOptMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84442-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84442-129">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="84442-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="84442-130">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla optimizada.</span><span class="sxs-lookup"><span data-stu-id="84442-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84442-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84442-131">Return value</span></span>

<span data-ttu-id="84442-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84442-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84442-133">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="84442-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84442-134">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="84442-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="84442-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84442-135">Remarks</span></span>

<span data-ttu-id="84442-136">Este método genera una nueva malla.</span><span class="sxs-lookup"><span data-stu-id="84442-136">This method generates a new mesh.</span></span> <span data-ttu-id="84442-137">Antes de ejecutar optimizar, una aplicación debe generar un búfer de adyacencia llamando a [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="84442-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="84442-138">El búfer de adyacencia contiene datos de adyacencias, como una lista de bordes y las caras adyacentes entre sí.</span><span class="sxs-lookup"><span data-stu-id="84442-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="84442-139">Este método es muy similar al método [**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) , salvo que puede realizar la optimización mientras genera el nuevo clon de la malla.</span><span class="sxs-lookup"><span data-stu-id="84442-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="84442-140">La malla de salida hereda todos los parámetros de creación de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="84442-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="84442-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84442-141">Requirements</span></span>



| <span data-ttu-id="84442-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="84442-142">Requirement</span></span> | <span data-ttu-id="84442-143">Value</span><span class="sxs-lookup"><span data-stu-id="84442-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84442-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84442-144">Header</span></span><br/>  | <dl> <span data-ttu-id="84442-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="84442-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="84442-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84442-146">Library</span></span><br/> | <dl> <span data-ttu-id="84442-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84442-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84442-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="84442-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84442-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="84442-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="84442-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="84442-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
