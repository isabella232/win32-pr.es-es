---
description: 'Método ID3DXPatchMesh::GetDeclaration: obtiene la declaración de vértice.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: Método ID3DXPatchMesh::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093303"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="d2d10-103">Método ID3DXPatchMesh::GetDeclaration</span><span class="sxs-lookup"><span data-stu-id="d2d10-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="d2d10-104">Obtiene la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="d2d10-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2d10-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="d2d10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d10-107">*pDeclaration* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2d10-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d10-108">Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="d2d10-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="d2d10-109">Matriz [**de elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describen el formato de vértice de los vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="d2d10-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="d2d10-110">La dimensión de esta matriz declarator es [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="d2d10-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="d2d10-111">La matriz de elementos de vértice termina con la macro [**\_ END de D3DDECL.**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="d2d10-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d10-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2d10-112">Return value</span></span>

<span data-ttu-id="d2d10-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2d10-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2d10-114">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2d10-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2d10-115">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d2d10-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d10-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2d10-116">Remarks</span></span>

<span data-ttu-id="d2d10-117">La matriz de elementos incluye la macro [**\_ END de D3DDECL,**](d3ddecl-end.md) que finaliza la declaración.</span><span class="sxs-lookup"><span data-stu-id="d2d10-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2d10-118">Requirements</span></span>



| <span data-ttu-id="d2d10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d10-119">Requirement</span></span> | <span data-ttu-id="d2d10-120">Value</span><span class="sxs-lookup"><span data-stu-id="d2d10-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d10-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2d10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d2d10-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d10-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2d10-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2d10-123">Library</span></span><br/> | <dl> <span data-ttu-id="d2d10-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2d10-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2d10-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d2d10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d10-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d2d10-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
