---
description: Desbloquee el búfer de índice.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'ID3DXPatchMesh:: UnlockIndexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698317"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="77b8a-103">ID3DXPatchMesh:: UnlockIndexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="77b8a-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="77b8a-104">Desbloquee el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="77b8a-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77b8a-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="77b8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77b8a-106">Parameters</span></span>

<span data-ttu-id="77b8a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="77b8a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77b8a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77b8a-108">Return value</span></span>

<span data-ttu-id="77b8a-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77b8a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77b8a-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77b8a-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="77b8a-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="77b8a-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="77b8a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77b8a-112">Remarks</span></span>

<span data-ttu-id="77b8a-113">Normalmente, el búfer de índice está bloqueado, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="77b8a-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="77b8a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77b8a-114">Requirements</span></span>



| <span data-ttu-id="77b8a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b8a-115">Requirement</span></span> | <span data-ttu-id="77b8a-116">Value</span><span class="sxs-lookup"><span data-stu-id="77b8a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77b8a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77b8a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="77b8a-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b8a-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="77b8a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77b8a-119">Library</span></span><br/> | <dl> <span data-ttu-id="77b8a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77b8a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77b8a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="77b8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b8a-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="77b8a-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




