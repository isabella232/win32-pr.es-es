---
description: Obtiene la declaración de vértice.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh:: GetDeclaration (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362816"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="2d60a-103">ID3DXPatchMesh:: GetDeclaration (método)</span><span class="sxs-lookup"><span data-stu-id="2d60a-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="2d60a-104">Obtiene la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="2d60a-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d60a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d60a-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="2d60a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d60a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d60a-107">*pDeclaration* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d60a-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d60a-108">Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="2d60a-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="2d60a-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="2d60a-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="2d60a-110">La dimensión de esta matriz declaradora es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="2d60a-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="2d60a-111">La matriz de elementos de vértice finaliza con la macro [**D3DDECL \_ End**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="2d60a-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d60a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d60a-112">Return value</span></span>

<span data-ttu-id="2d60a-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d60a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d60a-114">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d60a-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d60a-115">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2d60a-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d60a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d60a-116">Remarks</span></span>

<span data-ttu-id="2d60a-117">La matriz de elementos incluye la macro [**D3DDECL \_ End**](d3ddecl-end.md) , que finaliza la declaración.</span><span class="sxs-lookup"><span data-stu-id="2d60a-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d60a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d60a-118">Requirements</span></span>



| <span data-ttu-id="2d60a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d60a-119">Requirement</span></span> | <span data-ttu-id="2d60a-120">Value</span><span class="sxs-lookup"><span data-stu-id="2d60a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d60a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d60a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2d60a-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d60a-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2d60a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d60a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2d60a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d60a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d60a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d60a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d60a-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="2d60a-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
