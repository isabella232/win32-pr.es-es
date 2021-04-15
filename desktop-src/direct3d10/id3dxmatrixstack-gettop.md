---
description: Recupera la matriz actual en la parte superior de la pila.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack:: GetTop (método) (D3DX10. h)'
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708105"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="69cc5-103">ID3DXMATRIXStack:: GetTop (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="69cc5-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="69cc5-104">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="69cc5-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="69cc5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69cc5-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="69cc5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69cc5-106">Parameters</span></span>

<span data-ttu-id="69cc5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="69cc5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69cc5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69cc5-108">Return value</span></span>

<span data-ttu-id="69cc5-109">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="69cc5-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="69cc5-110">Este método devuelve un puntero a una estructura D3DXMATRIX que representa la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="69cc5-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="69cc5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69cc5-111">Remarks</span></span>

<span data-ttu-id="69cc5-112">No se garantiza que el puntero D3DXMATRIX devuelto por este método sea válido después de las operaciones de pila posteriores.</span><span class="sxs-lookup"><span data-stu-id="69cc5-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="69cc5-113">Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="69cc5-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="69cc5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69cc5-114">Requirements</span></span>



| <span data-ttu-id="69cc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="69cc5-115">Requirement</span></span> | <span data-ttu-id="69cc5-116">Value</span><span class="sxs-lookup"><span data-stu-id="69cc5-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69cc5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69cc5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="69cc5-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69cc5-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69cc5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69cc5-119">Library</span></span><br/> | <dl> <span data-ttu-id="69cc5-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69cc5-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69cc5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="69cc5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69cc5-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="69cc5-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="69cc5-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="69cc5-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
