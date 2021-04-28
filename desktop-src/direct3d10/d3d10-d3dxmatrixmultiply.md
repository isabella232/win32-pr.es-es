---
description: 'Función D3DXMatrixMultiply (D3DX10Math.h): determina el producto de dos matrices.'
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: Función D3DXMatrixMultiply (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 89e103d441648643be0176ca34f72f6175c11213
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113133"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="c2de2-103">Función D3DXMatrixMultiply (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c2de2-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="c2de2-104">Determina el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="c2de2-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2de2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2de2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="c2de2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2de2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c2de2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2de2-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2de2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2de2-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c2de2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c2de2-110">*pM1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c2de2-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2de2-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2de2-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2de2-112">Puntero a una estructura D3DXMATRIX de origen (lado izquierdo).</span><span class="sxs-lookup"><span data-stu-id="c2de2-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="c2de2-113">*pM2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c2de2-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2de2-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2de2-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2de2-115">Puntero a una estructura D3DXMATRIX de origen (lado derecho).</span><span class="sxs-lookup"><span data-stu-id="c2de2-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2de2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2de2-116">Return value</span></span>

<span data-ttu-id="c2de2-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2de2-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2de2-118">Puntero a una estructura D3DXMATRIX que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="c2de2-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2de2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2de2-119">Remarks</span></span>

<span data-ttu-id="c2de2-120">El resultado representa la transformación M1 seguida de la transformación M2 (Out = M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="c2de2-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="c2de2-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="c2de2-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c2de2-122">De esta manera, la función D3DXMatrixMultiply se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c2de2-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2de2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2de2-123">Requirements</span></span>



| <span data-ttu-id="c2de2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2de2-124">Requirement</span></span> | <span data-ttu-id="c2de2-125">Value</span><span class="sxs-lookup"><span data-stu-id="c2de2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2de2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2de2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c2de2-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c2de2-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2de2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2de2-128">Library</span></span><br/> | <dl> <span data-ttu-id="c2de2-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2de2-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2de2-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2de2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2de2-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c2de2-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
