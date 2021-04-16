---
description: Crea una matriz que alisa la geometría en un plano.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Función D3DXMatrixShadow (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689886"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="bd3c6-103">Función D3DXMatrixShadow (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bd3c6-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="bd3c6-104">Crea una matriz que alisa la geometría en un plano.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd3c6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="bd3c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd3c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3c6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd3c6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3c6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd3c6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bd3c6-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bd3c6-110">*pLight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd3c6-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3c6-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd3c6-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bd3c6-112">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que describe la posición de la luz.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="bd3c6-113">*pPlane* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd3c6-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3c6-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd3c6-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bd3c6-115">Puntero a la estructura de [**D3DXPLANE**](d3dxplane.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3c6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3c6-116">Return value</span></span>

<span data-ttu-id="bd3c6-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd3c6-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bd3c6-118">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que alisa la geometría en un plano.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3c6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd3c6-119">Remarks</span></span>

<span data-ttu-id="bd3c6-120">La función **D3DXMatrixShadow** reduce la geometría en un plano, como si se convirtiendo una sombra de una luz.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="bd3c6-121">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="bd3c6-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bd3c6-122">De esta manera, la función **D3DXMatrixShadow** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bd3c6-123">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="bd3c6-124">Si el componente w-Light es 0, el rayo desde el origen a la luz representa una luz direccional.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="bd3c6-125">Si es 1, la luz es una luz puntual.</span><span class="sxs-lookup"><span data-stu-id="bd3c6-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd3c6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3c6-126">Requirements</span></span>



| <span data-ttu-id="bd3c6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd3c6-127">Requirement</span></span> | <span data-ttu-id="bd3c6-128">Value</span><span class="sxs-lookup"><span data-stu-id="bd3c6-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3c6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd3c6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bd3c6-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd3c6-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bd3c6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd3c6-131">Library</span></span><br/> | <dl> <span data-ttu-id="bd3c6-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd3c6-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd3c6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd3c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3c6-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bd3c6-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




