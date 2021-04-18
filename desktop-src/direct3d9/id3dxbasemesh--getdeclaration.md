---
description: Recupera una declaración que describe los vértices de la malla.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'ID3DXBaseMesh:: GetDeclaration (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707724"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a><span data-ttu-id="4c50e-103">ID3DXBaseMesh:: GetDeclaration (método)</span><span class="sxs-lookup"><span data-stu-id="4c50e-103">ID3DXBaseMesh::GetDeclaration method</span></span>

<span data-ttu-id="4c50e-104">Recupera una declaración que describe los vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="4c50e-104">Retrieves a declaration describing the vertices in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c50e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c50e-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="4c50e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c50e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c50e-107">*Declaración* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c50e-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c50e-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="4c50e-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="4c50e-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="4c50e-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="4c50e-110">El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="4c50e-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="4c50e-111">La matriz de elementos de vértice finaliza con la macro [**D3DDECL \_ End**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="4c50e-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c50e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c50e-112">Return value</span></span>

<span data-ttu-id="4c50e-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c50e-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c50e-114">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c50e-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c50e-115">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4c50e-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c50e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c50e-116">Remarks</span></span>

<span data-ttu-id="4c50e-117">La matriz de elementos incluye la macro [**D3DDECL \_ End**](d3ddecl-end.md) , que finaliza la declaración.</span><span class="sxs-lookup"><span data-stu-id="4c50e-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c50e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c50e-118">Requirements</span></span>



| <span data-ttu-id="4c50e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c50e-119">Requirement</span></span> | <span data-ttu-id="4c50e-120">Value</span><span class="sxs-lookup"><span data-stu-id="4c50e-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c50e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4c50e-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c50e-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4c50e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c50e-123">Library</span></span><br/> | <dl> <span data-ttu-id="4c50e-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c50e-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c50e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c50e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c50e-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="4c50e-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
