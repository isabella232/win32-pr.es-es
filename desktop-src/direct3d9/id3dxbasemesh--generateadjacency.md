---
description: 'Método ID3DXBaseMesh::GenerateAdjacency: genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: Método ID3DXBaseMesh::GenerateAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 783ed7ad61337e606793b9b467e4b17fddd7ecd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115463"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="80eaa-103">Método ID3DXBaseMesh::GenerateAdjacency</span><span class="sxs-lookup"><span data-stu-id="80eaa-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="80eaa-104">Genere una lista de bordes de malla, así como una lista de caras que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="80eaa-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="80eaa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80eaa-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="80eaa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80eaa-107">*Epsilon* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80eaa-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80eaa-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80eaa-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80eaa-109">Especifica que los vértices que difieren en la posición en menos de epsilon deben tratarse como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="80eaa-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="80eaa-110">*pAdjacency* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="80eaa-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80eaa-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80eaa-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80eaa-112">Puntero a una matriz de tres DWORD por cara que se va a rellenar con los índices de caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="80eaa-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="80eaa-113">El número de bytes de esta matriz debe ser al menos \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span><span class="sxs-lookup"><span data-stu-id="80eaa-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80eaa-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80eaa-114">Return value</span></span>

<span data-ttu-id="80eaa-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80eaa-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80eaa-116">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80eaa-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80eaa-117">Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="80eaa-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="80eaa-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80eaa-118">Remarks</span></span>

<span data-ttu-id="80eaa-119">Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar para mejorar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="80eaa-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="80eaa-120">El orden de las entradas del búfer de adyacencia viene determinado por el orden de los índices de vértice en el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="80eaa-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="80eaa-121">El triángulo adyacente 0 siempre se corresponde con el borde entre los índices de las esquinas 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="80eaa-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="80eaa-122">El triángulo adyacente 1 siempre corresponde al borde entre los índices de las esquinas 1 y 2, mientras que el triángulo adyacente 2 corresponde al borde entre los índices de las esquinas 2 y 0.</span><span class="sxs-lookup"><span data-stu-id="80eaa-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="80eaa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80eaa-123">Requirements</span></span>



| <span data-ttu-id="80eaa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="80eaa-124">Requirement</span></span> | <span data-ttu-id="80eaa-125">Value</span><span class="sxs-lookup"><span data-stu-id="80eaa-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80eaa-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80eaa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="80eaa-127"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="80eaa-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80eaa-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80eaa-128">Library</span></span><br/> | <dl> <span data-ttu-id="80eaa-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="80eaa-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80eaa-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="80eaa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80eaa-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="80eaa-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="80eaa-132">**ID3DXMesh::Optimize**</span><span class="sxs-lookup"><span data-stu-id="80eaa-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="80eaa-133">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="80eaa-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
