---
description: Desbloquee el búfer de atributo.
ms.assetid: 4077ad15-9753-4031-81e7-c04e4267a0c9
title: 'ID3DXPatchMesh:: UnlockAttributeBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 42ea5ffacae2a2de073f6c16a9d29a7f76633ef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670263"
---
# <a name="id3dxpatchmeshunlockattributebuffer-method"></a><span data-ttu-id="20654-103">ID3DXPatchMesh:: UnlockAttributeBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="20654-103">ID3DXPatchMesh::UnlockAttributeBuffer method</span></span>

<span data-ttu-id="20654-104">Desbloquee el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="20654-104">Unlock the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="20654-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20654-105">Syntax</span></span>


```C++
HRESULT UnlockAttributeBuffer();
```



## <a name="parameters"></a><span data-ttu-id="20654-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20654-106">Parameters</span></span>

<span data-ttu-id="20654-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="20654-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20654-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20654-108">Return value</span></span>

<span data-ttu-id="20654-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20654-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20654-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20654-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20654-111">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="20654-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="20654-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20654-112">Remarks</span></span>

<span data-ttu-id="20654-113">Normalmente, el búfer de atributo está bloqueado, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="20654-113">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="20654-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20654-114">Requirements</span></span>



| <span data-ttu-id="20654-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="20654-115">Requirement</span></span> | <span data-ttu-id="20654-116">Value</span><span class="sxs-lookup"><span data-stu-id="20654-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20654-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20654-117">Header</span></span><br/>  | <dl> <span data-ttu-id="20654-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="20654-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="20654-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20654-119">Library</span></span><br/> | <dl> <span data-ttu-id="20654-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20654-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20654-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="20654-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20654-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="20654-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




