---
description: Generar una lista de bordes de malla y las revisiones que comparten cada borde.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'ID3DXPatchMesh:: GenerateAdjacency (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424335"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="c92c1-103">ID3DXPatchMesh:: GenerateAdjacency (método)</span><span class="sxs-lookup"><span data-stu-id="c92c1-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="c92c1-104">Generar una lista de bordes de malla y las revisiones que comparten cada borde.</span><span class="sxs-lookup"><span data-stu-id="c92c1-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c92c1-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="c92c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c92c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c92c1-107">*fTolerance* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c92c1-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92c1-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c92c1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c92c1-109">Especifica que los vértices que difieren en su posición menor que la tolerancia se deben tratar como coincidentes.</span><span class="sxs-lookup"><span data-stu-id="c92c1-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c92c1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c92c1-110">Return value</span></span>

<span data-ttu-id="c92c1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c92c1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c92c1-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c92c1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c92c1-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c92c1-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c92c1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c92c1-114">Remarks</span></span>

<span data-ttu-id="c92c1-115">Una vez que una aplicación genera información de adyacencias para una malla, los datos de la malla pueden optimizarse para mejorar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="c92c1-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="c92c1-116">Este método determina qué revisiones son adyacentes (dentro de la tolerancia proporcionada).</span><span class="sxs-lookup"><span data-stu-id="c92c1-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="c92c1-117">Esta información se usa internamente para optimizar la teselación.</span><span class="sxs-lookup"><span data-stu-id="c92c1-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92c1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c92c1-118">Requirements</span></span>



| <span data-ttu-id="c92c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c92c1-119">Requirement</span></span> | <span data-ttu-id="c92c1-120">Value</span><span class="sxs-lookup"><span data-stu-id="c92c1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c92c1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c92c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c92c1-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c92c1-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c92c1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c92c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="c92c1-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c92c1-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c92c1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c92c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92c1-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="c92c1-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="c92c1-127">**ID3DXPatchMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="c92c1-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
