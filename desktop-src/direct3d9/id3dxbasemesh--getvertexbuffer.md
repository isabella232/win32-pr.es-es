---
description: Recupera el búfer de vértices asociado a la malla.
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'ID3DXBaseMesh:: GetVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2098d97c1b7a685e9bd68cb3a6ac4feb6b949d2a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698176"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="60308-103">ID3DXBaseMesh:: GetVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="60308-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="60308-104">Recupera el búfer de vértices asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="60308-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="60308-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60308-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="60308-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60308-107">*ppVB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="60308-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="60308-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="60308-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="60308-109">Dirección de un puntero a una interfaz [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) que representa el objeto de búfer de vértice asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="60308-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60308-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60308-110">Return value</span></span>

<span data-ttu-id="60308-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60308-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60308-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60308-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60308-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="60308-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="60308-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60308-114">Requirements</span></span>



| <span data-ttu-id="60308-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="60308-115">Requirement</span></span> | <span data-ttu-id="60308-116">Value</span><span class="sxs-lookup"><span data-stu-id="60308-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60308-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60308-117">Header</span></span><br/>  | <dl> <span data-ttu-id="60308-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="60308-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="60308-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60308-119">Library</span></span><br/> | <dl> <span data-ttu-id="60308-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60308-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60308-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="60308-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60308-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="60308-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
