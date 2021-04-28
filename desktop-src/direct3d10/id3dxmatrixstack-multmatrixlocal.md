---
description: 'Método ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h): determina el producto de la matriz dada y la matriz actual.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: Método ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107953"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="ba5d8-103">Método ID3DXMATRIXStack::MultMatrixLocal (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="ba5d8-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="ba5d8-104">Determina el producto de la matriz dada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ba5d8-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba5d8-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ba5d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba5d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5d8-107">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ba5d8-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5d8-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba5d8-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ba5d8-109">Puntero a la estructura D3DXMATRIX que se va a multiplicar por la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ba5d8-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5d8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba5d8-110">Return value</span></span>

<span data-ttu-id="ba5d8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba5d8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba5d8-112">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba5d8-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba5d8-113">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ba5d8-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5d8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba5d8-114">Remarks</span></span>

<span data-ttu-id="ba5d8-115">Este método multiplica a la izquierda la matriz dada a la matriz actual (la transformación trata sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="ba5d8-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="ba5d8-116">Este método no agrega un elemento a la pila, reemplaza la matriz actual por el producto de la matriz dada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="ba5d8-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5d8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba5d8-117">Requirements</span></span>



| <span data-ttu-id="ba5d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5d8-118">Requirement</span></span> | <span data-ttu-id="ba5d8-119">Value</span><span class="sxs-lookup"><span data-stu-id="ba5d8-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5d8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba5d8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ba5d8-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ba5d8-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba5d8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba5d8-122">Library</span></span><br/> | <dl> <span data-ttu-id="ba5d8-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba5d8-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba5d8-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ba5d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5d8-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ba5d8-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ba5d8-126">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="ba5d8-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
