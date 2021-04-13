---
description: Obtiene la declaración de vértice.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo:: GetDeclaration (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362412"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="db4c0-103">ID3DXSkinInfo:: GetDeclaration (método)</span><span class="sxs-lookup"><span data-stu-id="db4c0-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="db4c0-104">Obtiene la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="db4c0-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db4c0-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="db4c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db4c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4c0-107">*Declaración* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="db4c0-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db4c0-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="db4c0-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="db4c0-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="db4c0-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="db4c0-110">El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="db4c0-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="db4c0-111">La matriz de elementos de vértice finaliza con la macro [**D3DDECL \_ End**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="db4c0-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db4c0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db4c0-112">Return value</span></span>

<span data-ttu-id="db4c0-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db4c0-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db4c0-114">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db4c0-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db4c0-115">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db4c0-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="db4c0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db4c0-116">Remarks</span></span>

<span data-ttu-id="db4c0-117">La matriz de elementos incluye la macro [**D3DDECL \_ End**](d3ddecl-end.md) , que finaliza la declaración.</span><span class="sxs-lookup"><span data-stu-id="db4c0-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4c0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db4c0-118">Requirements</span></span>



| <span data-ttu-id="db4c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="db4c0-119">Requirement</span></span> | <span data-ttu-id="db4c0-120">Value</span><span class="sxs-lookup"><span data-stu-id="db4c0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4c0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db4c0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="db4c0-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4c0-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="db4c0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db4c0-123">Library</span></span><br/> | <dl> <span data-ttu-id="db4c0-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db4c0-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db4c0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="db4c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4c0-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="db4c0-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="db4c0-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="db4c0-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
