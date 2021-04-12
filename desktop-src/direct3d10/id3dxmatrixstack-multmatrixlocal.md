---
description: Determina el producto de la matriz especificada y la matriz actual.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'ID3DXMATRIXStack:: MultMatrixLocal (método) (D3DX10. h)'
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
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280511"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="86bac-103">ID3DXMATRIXStack:: MultMatrixLocal (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="86bac-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="86bac-104">Determina el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="86bac-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="86bac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86bac-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="86bac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86bac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86bac-107">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86bac-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86bac-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="86bac-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="86bac-109">Puntero a la estructura D3DXMATRIX que se va a multiplicar por la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="86bac-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86bac-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86bac-110">Return value</span></span>

<span data-ttu-id="86bac-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86bac-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86bac-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86bac-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86bac-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="86bac-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="86bac-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86bac-114">Remarks</span></span>

<span data-ttu-id="86bac-115">Este método multiplica la matriz especificada a la matriz actual (la transformación es sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="86bac-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="86bac-116">Este método no agrega un elemento a la pila, reemplaza la matriz actual con el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="86bac-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="86bac-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86bac-117">Requirements</span></span>



| <span data-ttu-id="86bac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="86bac-118">Requirement</span></span> | <span data-ttu-id="86bac-119">Value</span><span class="sxs-lookup"><span data-stu-id="86bac-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86bac-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86bac-120">Header</span></span><br/>  | <dl> <span data-ttu-id="86bac-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="86bac-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="86bac-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86bac-122">Library</span></span><br/> | <dl> <span data-ttu-id="86bac-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86bac-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86bac-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="86bac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86bac-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="86bac-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="86bac-126">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="86bac-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
