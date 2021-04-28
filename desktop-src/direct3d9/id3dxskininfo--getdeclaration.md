---
description: 'Método ID3DXSkinInfo::GetDeclaration: obtiene la declaración de vértice.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: Método ID3DXSkinInfo::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093143"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="e00fe-103">Método ID3DXSkinInfo::GetDeclaration</span><span class="sxs-lookup"><span data-stu-id="e00fe-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="e00fe-104">Obtiene la declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="e00fe-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e00fe-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="e00fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e00fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00fe-107">*Declaración* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e00fe-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e00fe-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="e00fe-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="e00fe-109">Matriz [**de elementos D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describen el formato de vértice de los vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="e00fe-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="e00fe-110">El límite superior de esta matriz declarator es [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="e00fe-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="e00fe-111">La matriz de elementos de vértice termina con la macro [**\_ END de D3DDECL.**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="e00fe-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00fe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e00fe-112">Return value</span></span>

<span data-ttu-id="e00fe-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e00fe-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e00fe-114">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e00fe-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e00fe-115">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e00fe-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00fe-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e00fe-116">Remarks</span></span>

<span data-ttu-id="e00fe-117">La matriz de elementos incluye la macro [**\_ END de D3DDECL,**](d3ddecl-end.md) que finaliza la declaración.</span><span class="sxs-lookup"><span data-stu-id="e00fe-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00fe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00fe-118">Requirements</span></span>



| <span data-ttu-id="e00fe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00fe-119">Requirement</span></span> | <span data-ttu-id="e00fe-120">Value</span><span class="sxs-lookup"><span data-stu-id="e00fe-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e00fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e00fe-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e00fe-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="e00fe-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e00fe-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e00fe-123">Library</span></span><br/> | <dl> <span data-ttu-id="e00fe-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e00fe-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e00fe-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e00fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00fe-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="e00fe-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="e00fe-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="e00fe-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
