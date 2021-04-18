---
description: Agrega una matriz a la pila.
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: ID3DXMATRIXStack::P método uscripción (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1678ad9481a7c76fdb0e92a0c3b2de66d638de71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717646"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="48391-103">ID3DXMATRIXStack::P método uscripción (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="48391-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="48391-104">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="48391-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="48391-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48391-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="48391-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48391-106">Parameters</span></span>

<span data-ttu-id="48391-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="48391-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48391-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48391-108">Return value</span></span>

<span data-ttu-id="48391-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48391-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48391-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48391-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48391-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="48391-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="48391-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48391-112">Remarks</span></span>

<span data-ttu-id="48391-113">Este método incrementa el recuento de elementos de la pila en 1, duplicando la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="48391-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="48391-114">La pila aumentará dinámicamente a medida que se agreguen más elementos.</span><span class="sxs-lookup"><span data-stu-id="48391-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="48391-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48391-115">Requirements</span></span>



| <span data-ttu-id="48391-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="48391-116">Requirement</span></span> | <span data-ttu-id="48391-117">Value</span><span class="sxs-lookup"><span data-stu-id="48391-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48391-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48391-118">Header</span></span><br/>  | <dl> <span data-ttu-id="48391-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="48391-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="48391-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48391-120">Library</span></span><br/> | <dl> <span data-ttu-id="48391-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48391-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48391-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="48391-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48391-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="48391-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="48391-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="48391-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="48391-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="48391-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




