---
description: Recupera la matriz actual en la parte superior de la pila.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack:: GetTop (método) (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717651"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="e3937-103">ID3DXMATRIXStack:: GetTop (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e3937-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="e3937-104">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="e3937-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3937-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3937-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="e3937-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3937-106">Parameters</span></span>

<span data-ttu-id="e3937-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e3937-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3937-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3937-108">Return value</span></span>

<span data-ttu-id="e3937-109">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3937-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3937-110">Este método devuelve un puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que representa la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e3937-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3937-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3937-111">Remarks</span></span>

<span data-ttu-id="e3937-112">No se garantiza que el puntero [**D3DXMATRIX**](d3dxmatrix.md) devuelto por este método sea válido después de las operaciones de pila posteriores.</span><span class="sxs-lookup"><span data-stu-id="e3937-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="e3937-113">Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e3937-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3937-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3937-114">Requirements</span></span>



| <span data-ttu-id="e3937-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3937-115">Requirement</span></span> | <span data-ttu-id="e3937-116">Value</span><span class="sxs-lookup"><span data-stu-id="e3937-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3937-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3937-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3937-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3937-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3937-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3937-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3937-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3937-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3937-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3937-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3937-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e3937-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e3937-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="e3937-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="e3937-124">**ID3DXMATRIXStack::P uscripción**</span><span class="sxs-lookup"><span data-stu-id="e3937-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




