---
description: Obtiene el búfer de vértices de malla.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'ID3DXPatchMesh:: GetVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718555"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="490b3-103">ID3DXPatchMesh:: GetVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="490b3-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="490b3-104">Obtiene el búfer de vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="490b3-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="490b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="490b3-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="490b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="490b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="490b3-107">*ppVB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="490b3-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="490b3-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="490b3-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="490b3-109">Puntero al búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="490b3-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="490b3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="490b3-110">Return value</span></span>

<span data-ttu-id="490b3-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="490b3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="490b3-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="490b3-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="490b3-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="490b3-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="490b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="490b3-114">Remarks</span></span>

<span data-ttu-id="490b3-115">Este método presupone la teselación uniforme.</span><span class="sxs-lookup"><span data-stu-id="490b3-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="490b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="490b3-116">Requirements</span></span>



| <span data-ttu-id="490b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="490b3-117">Requirement</span></span> | <span data-ttu-id="490b3-118">Value</span><span class="sxs-lookup"><span data-stu-id="490b3-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="490b3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="490b3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="490b3-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="490b3-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="490b3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="490b3-121">Library</span></span><br/> | <dl> <span data-ttu-id="490b3-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="490b3-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="490b3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="490b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="490b3-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="490b3-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
