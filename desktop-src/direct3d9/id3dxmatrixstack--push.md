---
description: 'Método ID3DXMATRIXStack::P ush (D3dx9math.h): agrega una matriz a la pila.'
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: Método ID3DXMATRIXStack::P ush (D3dx9math.h)
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
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093512"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="537b3-103">Método ID3DXMATRIXStack::P ush (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="537b3-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="537b3-104">Agrega una matriz a la pila.</span><span class="sxs-lookup"><span data-stu-id="537b3-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="537b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="537b3-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="537b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="537b3-106">Parameters</span></span>

<span data-ttu-id="537b3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="537b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="537b3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="537b3-108">Return value</span></span>

<span data-ttu-id="537b3-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="537b3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="537b3-110">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="537b3-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="537b3-111">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="537b3-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="537b3-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="537b3-112">Remarks</span></span>

<span data-ttu-id="537b3-113">Este método incrementa el recuento de elementos en la pila en 1, duplicando la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="537b3-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="537b3-114">La pila crecerá dinámicamente a medida que se agregan más elementos.</span><span class="sxs-lookup"><span data-stu-id="537b3-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="537b3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="537b3-115">Requirements</span></span>



| <span data-ttu-id="537b3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="537b3-116">Requirement</span></span> | <span data-ttu-id="537b3-117">Value</span><span class="sxs-lookup"><span data-stu-id="537b3-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="537b3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="537b3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="537b3-119"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="537b3-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="537b3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="537b3-120">Library</span></span><br/> | <dl> <span data-ttu-id="537b3-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="537b3-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="537b3-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="537b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537b3-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="537b3-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="537b3-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="537b3-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="537b3-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="537b3-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




