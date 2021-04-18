---
description: Agrega una matriz a la pila.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: ID3DXMATRIXStack::P método uscripción (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 694bb8b02f340be14f38b7d2a44ec2038d175098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718539"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="b8d46-103">ID3DXMATRIXStack::P método uscripción (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b8d46-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="b8d46-104">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="b8d46-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d46-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8d46-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="b8d46-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8d46-106">Parameters</span></span>

<span data-ttu-id="b8d46-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8d46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8d46-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8d46-108">Return value</span></span>

<span data-ttu-id="b8d46-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8d46-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8d46-110">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8d46-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8d46-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b8d46-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d46-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8d46-112">Remarks</span></span>

<span data-ttu-id="b8d46-113">Este método incrementa el recuento de elementos de la pila en 1, duplicando la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="b8d46-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="b8d46-114">La pila aumentará dinámicamente a medida que se agreguen más elementos.</span><span class="sxs-lookup"><span data-stu-id="b8d46-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d46-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d46-115">Requirements</span></span>



| <span data-ttu-id="b8d46-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d46-116">Requirement</span></span> | <span data-ttu-id="b8d46-117">Value</span><span class="sxs-lookup"><span data-stu-id="b8d46-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d46-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8d46-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d46-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d46-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8d46-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8d46-120">Library</span></span><br/> | <dl> <span data-ttu-id="b8d46-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8d46-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d46-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8d46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d46-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b8d46-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b8d46-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b8d46-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




