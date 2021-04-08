---
description: Optimiza la malla de revisión para una teselación eficaz.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Método ID3DXPatchMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003980"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="e547d-103">ID3DXPatchMesh:: Optimize (método)</span><span class="sxs-lookup"><span data-stu-id="e547d-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="e547d-104">Optimiza la malla de revisión para una teselación eficaz.</span><span class="sxs-lookup"><span data-stu-id="e547d-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e547d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e547d-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e547d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e547d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e547d-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e547d-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e547d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e547d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e547d-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="e547d-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e547d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e547d-110">Return value</span></span>

<span data-ttu-id="e547d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e547d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e547d-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e547d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e547d-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.</span><span class="sxs-lookup"><span data-stu-id="e547d-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="e547d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e547d-114">Remarks</span></span>

<span data-ttu-id="e547d-115">Después de que una aplicación genera información de adyacencias para una malla, los datos de la malla se pueden optimizar (reordenar) para mejorar el rendimiento del dibujo.</span><span class="sxs-lookup"><span data-stu-id="e547d-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="e547d-116">Este método determina qué revisiones son adyacentes (dentro de la tolerancia proporcionada).</span><span class="sxs-lookup"><span data-stu-id="e547d-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="e547d-117">La información de adyacencias también se utiliza para optimizar la teselación.</span><span class="sxs-lookup"><span data-stu-id="e547d-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="e547d-118">Generar información de proximidad una vez y dividirlas repetidamente llamando a [**ID3DXPatchMesh:: dividirlas**](id3dxpatchmesh--tessellate.md).</span><span class="sxs-lookup"><span data-stu-id="e547d-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="e547d-119">La optimización realizada es independiente del nivel de teselación real utilizado.</span><span class="sxs-lookup"><span data-stu-id="e547d-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="e547d-120">Sin embargo, si se cambian los vértices de la malla, debe volver a generar la información de adyacencias.</span><span class="sxs-lookup"><span data-stu-id="e547d-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e547d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e547d-121">Requirements</span></span>



| <span data-ttu-id="e547d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e547d-122">Requirement</span></span> | <span data-ttu-id="e547d-123">Value</span><span class="sxs-lookup"><span data-stu-id="e547d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e547d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e547d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e547d-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e547d-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e547d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e547d-126">Library</span></span><br/> | <dl> <span data-ttu-id="e547d-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e547d-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e547d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e547d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e547d-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="e547d-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="e547d-130">**ID3DXPatchMesh::GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="e547d-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
