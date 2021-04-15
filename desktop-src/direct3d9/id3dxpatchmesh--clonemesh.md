---
description: Crea una nueva malla de revisión con la declaración de vértice especificada.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh:: CloneMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362464"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="3c0e5-103">ID3DXPatchMesh:: CloneMesh (método)</span><span class="sxs-lookup"><span data-stu-id="3c0e5-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="3c0e5-104">Crea una nueva malla de revisión con la declaración de vértice especificada.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c0e5-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="3c0e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c0e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0e5-107">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c0e5-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0e5-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c0e5-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c0e5-109">Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3c0e5-110">*pDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c0e5-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0e5-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3c0e5-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="3c0e5-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que especifican el formato de vértice de los vértices de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3c0e5-113">*pmesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3c0e5-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3c0e5-114">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c0e5-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="3c0e5-115">Dirección de un puntero a una interfaz [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa la malla clonada.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0e5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c0e5-116">Return value</span></span>

<span data-ttu-id="3c0e5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c0e5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c0e5-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c0e5-119">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0e5-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c0e5-120">Remarks</span></span>

<span data-ttu-id="3c0e5-121">**CloneMesh** convierte el búfer de vértices en la nueva declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="3c0e5-122">Las entradas en la declaración de vértices que son nuevas en la malla original se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="3c0e5-123">Si la malla actual tiene adyacencias, la nueva malla también tendrá adyacencias.</span><span class="sxs-lookup"><span data-stu-id="3c0e5-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0e5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c0e5-124">Requirements</span></span>



| <span data-ttu-id="3c0e5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c0e5-125">Requirement</span></span> | <span data-ttu-id="3c0e5-126">Value</span><span class="sxs-lookup"><span data-stu-id="3c0e5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0e5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c0e5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3c0e5-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c0e5-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3c0e5-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c0e5-129">Library</span></span><br/> | <dl> <span data-ttu-id="3c0e5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c0e5-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3c0e5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c0e5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0e5-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="3c0e5-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
