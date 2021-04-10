---
description: Calcula el producto de dos funciones de armónicos esféricos (f y g). Ambas funciones son del orden N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Función D3DXSHMultiply4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280427"
---
# <a name="d3dxshmultiply4-function"></a><span data-ttu-id="b4a4b-104">D3DXSHMultiply4 función)</span><span class="sxs-lookup"><span data-stu-id="b4a4b-104">D3DXSHMultiply4 function</span></span>

<span data-ttu-id="b4a4b-105">Calcula el producto de dos funciones de armónicos esféricos (*f* y *g*).</span><span class="sxs-lookup"><span data-stu-id="b4a4b-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="b4a4b-106">Ambas funciones son del orden N = 4.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-106">Both functions are of order N = 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a4b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4a4b-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="b4a4b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4a4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a4b-109">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4a4b-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a4b-110">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4a4b-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4a4b-111">Puntero a los coeficientes SH de salida: función base *Y* LM se almacena en l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-111">Pointer to the output SH coefficients — basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="b4a4b-112">El orden *N* determina la longitud de la matriz, donde siempre debe haber un coeficiente de *N*².</span><span class="sxs-lookup"><span data-stu-id="b4a4b-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="b4a4b-113">*PF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4a4b-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a4b-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4a4b-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4a4b-115">Los coeficientes SH de entrada para la primera función.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="b4a4b-116">*PG* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b4a4b-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a4b-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4a4b-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4a4b-118">Segundo conjunto de coeficientes SH de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a4b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4a4b-119">Return value</span></span>

<span data-ttu-id="b4a4b-120">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4a4b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4a4b-121">Puntero a los coeficientes de salida SH.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a4b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4a4b-122">Remarks</span></span>

<span data-ttu-id="b4a4b-123">El producto de dos funciones SH de orden N = 4 genera una función SH de orden 2 × *N* -1 = 7, pero los resultados se truncan.</span><span class="sxs-lookup"><span data-stu-id="b4a4b-123">The product of two SH functions of order N = 4 generates an SH function of order 2 × *N* - 1 = 7, but the results are truncated.</span></span> <span data-ttu-id="b4a4b-124">Esto significa que el producto se desactivará ( *f* × *g*  =  *g* × *f* ), pero no se asocia ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="b4a4b-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="b4a4b-125">Esta función usa la siguiente ecuación:</span><span class="sxs-lookup"><span data-stu-id="b4a4b-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="b4a4b-126">donde y \_ son las funciones de base de l l, donde f (s) y g (s) usan la siguiente función SH:</span><span class="sxs-lookup"><span data-stu-id="b4a4b-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="b4a4b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a4b-127">Requirements</span></span>



| <span data-ttu-id="b4a4b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a4b-128">Requirement</span></span> | <span data-ttu-id="b4a4b-129">Value</span><span class="sxs-lookup"><span data-stu-id="b4a4b-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a4b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4a4b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b4a4b-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a4b-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b4a4b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4a4b-132">Library</span></span><br/> | <dl> <span data-ttu-id="b4a4b-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4a4b-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b4a4b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4a4b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a4b-135">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b4a4b-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
