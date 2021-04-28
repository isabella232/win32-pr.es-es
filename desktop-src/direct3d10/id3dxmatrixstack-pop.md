---
description: 'Método ID3DXMATRIXStack::P op (D3DX10.h): quita la matriz actual de la parte superior de la pila.'
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: Método ID3DXMATRIXStack::P op (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107933"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="ec24d-103">Método ID3DXMATRIXStack::P op (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="ec24d-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="ec24d-104">Quita la matriz actual de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="ec24d-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec24d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec24d-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="ec24d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec24d-106">Parameters</span></span>

<span data-ttu-id="ec24d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec24d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec24d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec24d-108">Return value</span></span>

<span data-ttu-id="ec24d-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec24d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec24d-110">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec24d-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec24d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec24d-111">Remarks</span></span>

<span data-ttu-id="ec24d-112">Tenga en cuenta que este método reduce el número de elementos de la pila en 1, quitando eficazmente la matriz actual de la parte superior de la pila y promocionando una matriz en la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="ec24d-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="ec24d-113">Si el recuento actual de elementos de la pila es 0, este método devuelve sin realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="ec24d-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="ec24d-114">Si el recuento actual de elementos de la pila es 1, este método vacía la pila.</span><span class="sxs-lookup"><span data-stu-id="ec24d-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec24d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec24d-115">Requirements</span></span>



| <span data-ttu-id="ec24d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec24d-116">Requirement</span></span> | <span data-ttu-id="ec24d-117">Value</span><span class="sxs-lookup"><span data-stu-id="ec24d-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec24d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec24d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ec24d-119"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec24d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec24d-120">Library</span></span><br/> | <dl> <span data-ttu-id="ec24d-121"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec24d-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec24d-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec24d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec24d-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ec24d-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ec24d-124">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="ec24d-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




