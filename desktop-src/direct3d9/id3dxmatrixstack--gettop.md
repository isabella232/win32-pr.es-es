---
description: 'Método ID3DXMATRIXStack::GetTop (D3dx9math.h): recupera la matriz actual en la parte superior de la pila.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: Método ID3DXMATRIXStack::GetTop (D3dx9math.h)
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
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093583"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="ab3cb-103">Método ID3DXMATRIXStack::GetTop (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ab3cb-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="ab3cb-104">Recupera la matriz actual en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab3cb-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="ab3cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab3cb-106">Parameters</span></span>

<span data-ttu-id="ab3cb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab3cb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab3cb-108">Return value</span></span>

<span data-ttu-id="ab3cb-109">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab3cb-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab3cb-110">Este método devuelve un puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que representa la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab3cb-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab3cb-111">Remarks</span></span>

<span data-ttu-id="ab3cb-112">No se garantiza que el puntero [**D3DXMATRIX**](d3dxmatrix.md) devuelto por este método sea válido después de las operaciones de pila posteriores.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="ab3cb-113">Tenga en cuenta que este método no quita la matriz actual de la parte superior de la pila; en su lugar, simplemente devuelve la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ab3cb-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab3cb-114">Requirements</span></span>



| <span data-ttu-id="ab3cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab3cb-115">Requirement</span></span> | <span data-ttu-id="ab3cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="ab3cb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3cb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab3cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab3cb-118"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab3cb-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab3cb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab3cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab3cb-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab3cb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab3cb-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab3cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3cb-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ab3cb-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ab3cb-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="ab3cb-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="ab3cb-124">**ID3DXMATRIXStack::P ush**</span><span class="sxs-lookup"><span data-stu-id="ab3cb-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




