---
description: Determina el producto de la matriz especificada y la matriz actual.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'ID3DXMATRIXStack:: MultMatrixLocal (método) (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717647"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="83500-103">ID3DXMATRIXStack:: MultMatrixLocal (método) (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="83500-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="83500-104">Determina el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="83500-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="83500-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83500-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="83500-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83500-107">*pMat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83500-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83500-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="83500-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="83500-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que se va a multiplicar por la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="83500-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83500-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83500-110">Return value</span></span>

<span data-ttu-id="83500-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83500-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83500-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83500-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83500-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="83500-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="83500-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83500-114">Remarks</span></span>

<span data-ttu-id="83500-115">Este método multiplica la matriz especificada a la matriz actual (la transformación es sobre el origen local del objeto).</span><span class="sxs-lookup"><span data-stu-id="83500-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="83500-116">Este método no agrega un elemento a la pila, reemplaza la matriz actual con el producto de la matriz especificada y la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="83500-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="83500-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83500-117">Requirements</span></span>



| <span data-ttu-id="83500-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83500-118">Requirement</span></span> | <span data-ttu-id="83500-119">Value</span><span class="sxs-lookup"><span data-stu-id="83500-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83500-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83500-120">Header</span></span><br/>  | <dl> <span data-ttu-id="83500-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="83500-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="83500-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83500-122">Library</span></span><br/> | <dl> <span data-ttu-id="83500-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83500-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83500-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="83500-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83500-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="83500-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="83500-126">**ID3DXMATRIXStack::MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="83500-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




