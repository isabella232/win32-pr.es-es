---
description: Crea una matriz de búsqueda a la izquierda.
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: Función D3DXMatrixLookAtLH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fa7acdf467761bd3b3cfbc023662e9b3368b98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708009"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="6ac0c-103">Función D3DXMatrixLookAtLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6ac0c-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="6ac0c-104">Crea una matriz de búsqueda a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac0c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ac0c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="6ac0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ac0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac0c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6ac0c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac0c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ac0c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ac0c-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ac0c-110">*pEye* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac0c-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac0c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac0c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac0c-112">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que define el punto de ojo.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="6ac0c-113">Este valor se usa en la traducción.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="6ac0c-114">*pAt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac0c-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac0c-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac0c-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac0c-116">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que define el destino de la apariencia de la cámara.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="6ac0c-117">*pUp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ac0c-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac0c-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ac0c-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ac0c-119">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que define el mundo actual, normalmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="6ac0c-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac0c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ac0c-120">Return value</span></span>

<span data-ttu-id="6ac0c-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ac0c-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ac0c-122">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz de búsqueda a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac0c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ac0c-123">Remarks</span></span>

<span data-ttu-id="6ac0c-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="6ac0c-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6ac0c-125">De esta manera, la función **D3DXMatrixLookAtLH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6ac0c-126">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="6ac0c-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="6ac0c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ac0c-127">Requirements</span></span>



| <span data-ttu-id="6ac0c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac0c-128">Requirement</span></span> | <span data-ttu-id="6ac0c-129">Value</span><span class="sxs-lookup"><span data-stu-id="6ac0c-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac0c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ac0c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6ac0c-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac0c-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ac0c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ac0c-132">Library</span></span><br/> | <dl> <span data-ttu-id="6ac0c-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ac0c-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ac0c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ac0c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac0c-135">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="6ac0c-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6ac0c-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="6ac0c-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




