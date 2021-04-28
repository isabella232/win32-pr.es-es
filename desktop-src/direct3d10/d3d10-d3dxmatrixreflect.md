---
description: 'Función D3DXMatrixReflect (D3DX10Math.h): crea una matriz que refleja el sistema de coordenadas sobre un plano.'
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: Función D3DXMatrixReflect (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103420"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="c68c6-103">Función D3DXMatrixReflect (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c68c6-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="c68c6-104">Crea una matriz que refleja el sistema de coordenadas sobre un plano.</span><span class="sxs-lookup"><span data-stu-id="c68c6-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c68c6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="c68c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c68c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68c6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c68c6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c68c6-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c68c6-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c68c6-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c68c6-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c68c6-110">*pPlane* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c68c6-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c68c6-111">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c68c6-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c68c6-112">Puntero al [**D3DXPLANE de origen.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="c68c6-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68c6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c68c6-113">Return value</span></span>

<span data-ttu-id="c68c6-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c68c6-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c68c6-115">Puntero a una estructura D3DXMATRIX que refleja el sistema de coordenadas sobre el plano de origen.</span><span class="sxs-lookup"><span data-stu-id="c68c6-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68c6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c68c6-116">Remarks</span></span>

<span data-ttu-id="c68c6-117">Esta función normaliza la ecuación del plano antes de crear la matriz reflejada.</span><span class="sxs-lookup"><span data-stu-id="c68c6-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="c68c6-118">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="c68c6-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c68c6-119">De este modo, la función D3DXMatrixReflect se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c68c6-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c68c6-120">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="c68c6-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="c68c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c68c6-121">Requirements</span></span>



| <span data-ttu-id="c68c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68c6-122">Requirement</span></span> | <span data-ttu-id="c68c6-123">Value</span><span class="sxs-lookup"><span data-stu-id="c68c6-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c68c6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c68c6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c68c6-125"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c68c6-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c68c6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c68c6-126">Library</span></span><br/> | <dl> <span data-ttu-id="c68c6-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c68c6-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c68c6-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c68c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68c6-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c68c6-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
