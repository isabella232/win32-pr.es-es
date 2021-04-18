---
description: Calcula el producto de dos funciones representadas mediante SH (f y g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Función D3DXSHMultiply2 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717704"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="96358-103">Función D3DXSHMultiply2 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="96358-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="96358-104">Calcula el producto de dos funciones representadas mediante SH (f y g).</span><span class="sxs-lookup"><span data-stu-id="96358-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="96358-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96358-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="96358-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96358-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96358-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96358-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96358-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="96358-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96358-109">Puntero a la función YLM de los coeficientes de SH de salida se almacena en l \* l + m + l.</span><span class="sxs-lookup"><span data-stu-id="96358-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="96358-110">*PF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96358-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96358-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96358-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96358-112">Entrada SH coeffs para la primera función.</span><span class="sxs-lookup"><span data-stu-id="96358-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="96358-113">*PG* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96358-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96358-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96358-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96358-115">Segundo conjunto de entrada SH coeffs.</span><span class="sxs-lookup"><span data-stu-id="96358-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96358-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96358-116">Return value</span></span>

<span data-ttu-id="96358-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="96358-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96358-118">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="96358-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="96358-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96358-119">Remarks</span></span>

<span data-ttu-id="96358-120">El orden es un número entre 2 y 6, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="96358-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="96358-121">Por lo tanto, esta página documenta varias funciones: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="96358-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="96358-122">Calcula el producto de dos funciones representadas mediante SH (f y g), donde *pOut* \[ i \] = int (y \_ i (s) g (s) \* \* ), donde y \_ i es la función i + d, f (s) y g (s) son funciones SH (SUM \_ i (y \_ i) \* \_ ).</span><span class="sxs-lookup"><span data-stu-id="96358-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="96358-123">El orden O determina las longitudes de las matrices, donde siempre debe haber coeficientes O ^ 2.</span><span class="sxs-lookup"><span data-stu-id="96358-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="96358-124">En general, el producto de dos funciones SH de order O genera una función SH de orden 2 \* O-1, pero los resultados se truncan.</span><span class="sxs-lookup"><span data-stu-id="96358-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="96358-125">Esto significa que el producto se desactivará (f \* g = = g \* f), pero no se asocia (f \* (g \* h)! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="96358-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="96358-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96358-126">Requirements</span></span>



| <span data-ttu-id="96358-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="96358-127">Requirement</span></span> | <span data-ttu-id="96358-128">Value</span><span class="sxs-lookup"><span data-stu-id="96358-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96358-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96358-129">Header</span></span><br/> | <dl> <span data-ttu-id="96358-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="96358-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96358-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="96358-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96358-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="96358-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
