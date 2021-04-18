---
description: Determina el producto de la matriz actual y la matriz especificada.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack:: MultMatrix (método) (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717648"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="f532d-103">ID3DXMATRIXStack:: MultMatrix (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f532d-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="f532d-104">Determina el producto de la matriz actual y la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="f532d-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f532d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f532d-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="f532d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f532d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f532d-107">*pMat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f532d-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f532d-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f532d-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f532d-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que se va a multiplicar por la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="f532d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f532d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f532d-110">Return value</span></span>

<span data-ttu-id="f532d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f532d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f532d-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f532d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f532d-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f532d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f532d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f532d-114">Remarks</span></span>

<span data-ttu-id="f532d-115">Este método multiplica a la derecha la matriz especificada a la matriz actual (la transformación es sobre el origen mundial actual).</span><span class="sxs-lookup"><span data-stu-id="f532d-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="f532d-116">Este método no agrega un elemento a la pila, reemplaza la matriz actual con el producto de la matriz actual y la matriz determinada.</span><span class="sxs-lookup"><span data-stu-id="f532d-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f532d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f532d-117">Requirements</span></span>



| <span data-ttu-id="f532d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f532d-118">Requirement</span></span> | <span data-ttu-id="f532d-119">Value</span><span class="sxs-lookup"><span data-stu-id="f532d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f532d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f532d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f532d-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f532d-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f532d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f532d-122">Library</span></span><br/> | <dl> <span data-ttu-id="f532d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f532d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f532d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f532d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f532d-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="f532d-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f532d-126">**ID3DXMATRIXStack::MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="f532d-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




