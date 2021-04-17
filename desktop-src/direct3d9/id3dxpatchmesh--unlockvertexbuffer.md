---
description: Desbloquee el búfer de vértices.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'ID3DXPatchMesh:: UnlockVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698435"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="7c0a6-103">ID3DXPatchMesh:: UnlockVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="7c0a6-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="7c0a6-104">Desbloquee el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c0a6-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="7c0a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c0a6-106">Parameters</span></span>

<span data-ttu-id="7c0a6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c0a6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c0a6-108">Return value</span></span>

<span data-ttu-id="7c0a6-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c0a6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c0a6-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c0a6-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0a6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c0a6-112">Remarks</span></span>

<span data-ttu-id="7c0a6-113">Normalmente, el búfer de vértices se bloquea, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="7c0a6-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0a6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0a6-114">Requirements</span></span>



| <span data-ttu-id="7c0a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0a6-115">Requirement</span></span> | <span data-ttu-id="7c0a6-116">Value</span><span class="sxs-lookup"><span data-stu-id="7c0a6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0a6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c0a6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c0a6-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0a6-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7c0a6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c0a6-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c0a6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c0a6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c0a6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c0a6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0a6-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="7c0a6-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




