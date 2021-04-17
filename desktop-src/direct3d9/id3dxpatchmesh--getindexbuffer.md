---
description: Obtiene el búfer de índice de malla.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'ID3DXPatchMesh:: GetIndexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718455"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="f76d5-103">ID3DXPatchMesh:: GetIndexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="f76d5-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="f76d5-104">Obtiene el búfer de índice de malla.</span><span class="sxs-lookup"><span data-stu-id="f76d5-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f76d5-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="f76d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f76d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76d5-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f76d5-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f76d5-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="f76d5-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="f76d5-109">Puntero al búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="f76d5-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76d5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f76d5-110">Return value</span></span>

<span data-ttu-id="f76d5-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f76d5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f76d5-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f76d5-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f76d5-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f76d5-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f76d5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f76d5-114">Remarks</span></span>

<span data-ttu-id="f76d5-115">El búfer de índice contiene el orden de los vértices en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="f76d5-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="f76d5-116">El búfer de índice se usa para tener acceso al búfer de vértices cuando se representa la malla.</span><span class="sxs-lookup"><span data-stu-id="f76d5-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="f76d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f76d5-117">Requirements</span></span>



| <span data-ttu-id="f76d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76d5-118">Requirement</span></span> | <span data-ttu-id="f76d5-119">Value</span><span class="sxs-lookup"><span data-stu-id="f76d5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f76d5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f76d5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f76d5-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f76d5-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f76d5-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f76d5-122">Library</span></span><br/> | <dl> <span data-ttu-id="f76d5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f76d5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f76d5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f76d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76d5-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f76d5-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
