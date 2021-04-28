---
description: 'Método ID3DXMATRIXStack::GetTop (D3DX10.h): recupera la matriz actual en la parte superior de la pila.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: Método ID3DXMATRIXStack::GetTop (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108043"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="ae7e9-103">Método ID3DXMATRIXStack::GetTop (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="ae7e9-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="ae7e9-104">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="ae7e9-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae7e9-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="ae7e9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae7e9-106">Parameters</span></span>

<span data-ttu-id="ae7e9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ae7e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae7e9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae7e9-108">Return value</span></span>

<span data-ttu-id="ae7e9-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae7e9-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ae7e9-110">Este método devuelve un puntero a una estructura D3DXMATRIX que representa la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ae7e9-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae7e9-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae7e9-111">Remarks</span></span>

<span data-ttu-id="ae7e9-112">No se garantiza que el puntero D3DXMATRIX devuelto por este método sea válido después de las operaciones de pila posteriores.</span><span class="sxs-lookup"><span data-stu-id="ae7e9-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="ae7e9-113">Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ae7e9-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7e9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7e9-114">Requirements</span></span>



| <span data-ttu-id="ae7e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7e9-115">Requirement</span></span> | <span data-ttu-id="ae7e9-116">Value</span><span class="sxs-lookup"><span data-stu-id="ae7e9-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7e9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae7e9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae7e9-118"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e9-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae7e9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae7e9-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae7e9-120"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae7e9-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae7e9-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae7e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7e9-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ae7e9-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ae7e9-123">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="ae7e9-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
