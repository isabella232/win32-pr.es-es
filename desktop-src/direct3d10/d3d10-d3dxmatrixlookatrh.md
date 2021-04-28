---
description: 'Función D3DXMatrixLookAtRH (D3DX10Math.h): crea una matriz de mirada derecha.'
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Función D3DXMatrixLookAtRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0380207124e4a446b6303dbb377d116b8ae058ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103453"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="e8f45-103">Función D3DXMatrixLookAtRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="e8f45-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="e8f45-104">Crea una matriz de mirada derecha.</span><span class="sxs-lookup"><span data-stu-id="e8f45-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8f45-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="e8f45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8f45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8f45-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e8f45-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f45-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8f45-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e8f45-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e8f45-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e8f45-110">*pEye* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e8f45-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f45-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8f45-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e8f45-112">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que define el punto de los ojos.</span><span class="sxs-lookup"><span data-stu-id="e8f45-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="e8f45-113">Este valor se usa en la traducción.</span><span class="sxs-lookup"><span data-stu-id="e8f45-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="e8f45-114">*pAt* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e8f45-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f45-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8f45-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e8f45-116">Puntero a la estructura D3DXVECTOR3 que define el destino de mirada de la cámara.</span><span class="sxs-lookup"><span data-stu-id="e8f45-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="e8f45-117">*pUp* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e8f45-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8f45-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8f45-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e8f45-119">Puntero a la estructura D3DXVECTOR3 que define el valor de up del mundo actual, normalmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="e8f45-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8f45-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8f45-120">Return value</span></span>

<span data-ttu-id="e8f45-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8f45-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e8f45-122">Puntero a una estructura D3DXMATRIX que es una matriz de mirada derecha.</span><span class="sxs-lookup"><span data-stu-id="e8f45-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8f45-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8f45-123">Remarks</span></span>

<span data-ttu-id="e8f45-124">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="e8f45-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e8f45-125">De esta manera, la función D3DXMatrixLookAtRH se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e8f45-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e8f45-126">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="e8f45-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="e8f45-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8f45-127">Requirements</span></span>



| <span data-ttu-id="e8f45-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8f45-128">Requirement</span></span> | <span data-ttu-id="e8f45-129">Value</span><span class="sxs-lookup"><span data-stu-id="e8f45-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f45-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8f45-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e8f45-131"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e8f45-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e8f45-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8f45-132">Library</span></span><br/> | <dl> <span data-ttu-id="e8f45-133"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8f45-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8f45-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8f45-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f45-135">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e8f45-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
