---
description: 'Función D3DXMatrixShadow (D3DX10Math.h): crea una matriz que aplana la geometría en un plano.'
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: Función D3DXMatrixShadow (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d3a5bff99552a4c5d65267c390c25a2892d3d32f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103353"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a><span data-ttu-id="f8035-103">Función D3DXMatrixShadow (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f8035-103">D3DXMatrixShadow function (D3DX10Math.h)</span></span>

<span data-ttu-id="f8035-104">Crea una matriz que aplana la geometría en un plano.</span><span class="sxs-lookup"><span data-stu-id="f8035-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8035-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8035-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="f8035-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8035-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f8035-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8035-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8035-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8035-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f8035-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8035-110">*pLight* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f8035-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8035-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8035-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8035-112">Puntero a [**un D3DXVECTOR4**](d3d10-d3dxvector4.md) que describe la posición de la luz.</span><span class="sxs-lookup"><span data-stu-id="f8035-112">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="f8035-113">*pPlane* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f8035-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8035-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8035-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="f8035-115">Puntero al [**D3DXPLANE de origen.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="f8035-115">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8035-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8035-116">Return value</span></span>

<span data-ttu-id="f8035-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8035-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8035-118">Puntero a una estructura D3DXMATRIX que aplana la geometría en un plano.</span><span class="sxs-lookup"><span data-stu-id="f8035-118">Pointer to a D3DXMATRIX structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8035-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8035-119">Remarks</span></span>

<span data-ttu-id="f8035-120">La **función D3DXMatrixShadow** aplana la geometría en un plano, como si la conversión de una sombra a partir de una luz.</span><span class="sxs-lookup"><span data-stu-id="f8035-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="f8035-121">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="f8035-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f8035-122">De esta manera, la **función D3DXMatrixShadow** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="f8035-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f8035-123">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="f8035-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="f8035-124">Si el componente w de la luz es 0, el rayo del origen a la luz representa una luz direccional.</span><span class="sxs-lookup"><span data-stu-id="f8035-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="f8035-125">Si es 1, la luz es una luz de punto.</span><span class="sxs-lookup"><span data-stu-id="f8035-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8035-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8035-126">Requirements</span></span>



| <span data-ttu-id="f8035-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8035-127">Requirement</span></span> | <span data-ttu-id="f8035-128">Value</span><span class="sxs-lookup"><span data-stu-id="f8035-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8035-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8035-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f8035-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8035-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8035-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8035-131">Library</span></span><br/> | <dl> <span data-ttu-id="f8035-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8035-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8035-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f8035-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8035-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f8035-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
