---
description: 'Función D3DXMatrixLookAtRH (D3dx9math.h): crea una matriz de mirada derecha.'
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Función D3DXMatrixLookAtRH (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b3a738de31edf373deb65ea9991e1e1502f47c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335609"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="bb9e0-103">Función D3DXMatrixLookAtRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bb9e0-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="bb9e0-104">Crea una matriz de mirada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb9e0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="bb9e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb9e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb9e0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb9e0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb9e0-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb9e0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb9e0-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb9e0-110">*pEye* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bb9e0-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb9e0-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb9e0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb9e0-112">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que define el punto de los ojos.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="bb9e0-113">Este valor se usa en la traducción.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="bb9e0-114">*pAt* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bb9e0-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb9e0-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb9e0-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb9e0-116">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que define el destino de mirada de la cámara.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="bb9e0-117">*pUp* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="bb9e0-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb9e0-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb9e0-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bb9e0-119">Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que define el valor de arriba del mundo actual, normalmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="bb9e0-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb9e0-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb9e0-120">Return value</span></span>

<span data-ttu-id="bb9e0-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb9e0-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb9e0-122">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es una matriz de mirada derecha.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb9e0-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb9e0-123">Remarks</span></span>

<span data-ttu-id="bb9e0-124">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="bb9e0-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bb9e0-125">De esta manera, la **función D3DXMatrixLookAtRH** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bb9e0-126">Esta función usa la fórmula siguiente para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="bb9e0-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="bb9e0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb9e0-127">Requirements</span></span>



| <span data-ttu-id="bb9e0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb9e0-128">Requirement</span></span> | <span data-ttu-id="bb9e0-129">Value</span><span class="sxs-lookup"><span data-stu-id="bb9e0-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9e0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb9e0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bb9e0-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bb9e0-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb9e0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb9e0-132">Library</span></span><br/> | <dl> <span data-ttu-id="bb9e0-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb9e0-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb9e0-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb9e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9e0-135">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bb9e0-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bb9e0-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="bb9e0-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




