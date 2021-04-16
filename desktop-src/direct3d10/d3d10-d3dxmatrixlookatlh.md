---
description: Crea una matriz de búsqueda a la izquierda.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: Función D3DXMatrixLookAtLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a5a7ffa8750fb08174f45b1069f103bfe08be1f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548078"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="47ba5-103">Función D3DXMatrixLookAtLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="47ba5-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="47ba5-104">Crea una matriz de búsqueda a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="47ba5-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ba5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47ba5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="47ba5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47ba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47ba5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="47ba5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47ba5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="47ba5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="47ba5-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="47ba5-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="47ba5-110">*pEye* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47ba5-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47ba5-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="47ba5-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="47ba5-112">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que define el punto de ojo.</span><span class="sxs-lookup"><span data-stu-id="47ba5-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="47ba5-113">Este valor se usa en la traducción.</span><span class="sxs-lookup"><span data-stu-id="47ba5-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="47ba5-114">*pAt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47ba5-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47ba5-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="47ba5-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="47ba5-116">Puntero a la estructura D3DXVECTOR3 que define el destino de la apariencia de la cámara.</span><span class="sxs-lookup"><span data-stu-id="47ba5-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="47ba5-117">*pUp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47ba5-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47ba5-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="47ba5-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="47ba5-119">Puntero a la estructura D3DXVECTOR3 que define el mundo actual, normalmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="47ba5-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47ba5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47ba5-120">Return value</span></span>

<span data-ttu-id="47ba5-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="47ba5-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="47ba5-122">Puntero a una estructura D3DXMATRIX que es una matriz de búsqueda a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="47ba5-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="47ba5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47ba5-123">Remarks</span></span>

<span data-ttu-id="47ba5-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="47ba5-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="47ba5-125">De esta manera, la función D3DXMatrixLookAtLH se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="47ba5-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="47ba5-126">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="47ba5-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="47ba5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47ba5-127">Requirements</span></span>



| <span data-ttu-id="47ba5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="47ba5-128">Requirement</span></span> | <span data-ttu-id="47ba5-129">Value</span><span class="sxs-lookup"><span data-stu-id="47ba5-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ba5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47ba5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="47ba5-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ba5-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="47ba5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47ba5-132">Library</span></span><br/> | <dl> <span data-ttu-id="47ba5-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47ba5-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47ba5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="47ba5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ba5-135">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="47ba5-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
