---
description: Quita la matriz actual de la parte superior de la pila.
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: 'ID3DXMATRIXStack: método OP:P (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083710"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="5753b-103">ID3DXMATRIXStack: método OP:P (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5753b-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="5753b-104">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="5753b-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5753b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5753b-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="5753b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5753b-106">Parameters</span></span>

<span data-ttu-id="5753b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5753b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5753b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5753b-108">Return value</span></span>

<span data-ttu-id="5753b-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5753b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5753b-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5753b-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5753b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5753b-111">Remarks</span></span>

<span data-ttu-id="5753b-112">Tenga en cuenta que este método reduce el número de elementos de la pila en 1, quitando de forma eficaz la matriz actual de la parte superior de la pila y promocionando una matriz a la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="5753b-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="5753b-113">Si el recuento actual de elementos de la pila es 0, este método devuelve sin realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="5753b-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="5753b-114">Si el recuento actual de elementos de la pila es 1, este método vacía la pila.</span><span class="sxs-lookup"><span data-stu-id="5753b-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="5753b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5753b-115">Requirements</span></span>



| <span data-ttu-id="5753b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5753b-116">Requirement</span></span> | <span data-ttu-id="5753b-117">Value</span><span class="sxs-lookup"><span data-stu-id="5753b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5753b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5753b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5753b-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5753b-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5753b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5753b-120">Library</span></span><br/> | <dl> <span data-ttu-id="5753b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5753b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5753b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5753b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5753b-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5753b-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5753b-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="5753b-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="5753b-125">**ID3DXMATRIXStack::P uscripción**</span><span class="sxs-lookup"><span data-stu-id="5753b-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




