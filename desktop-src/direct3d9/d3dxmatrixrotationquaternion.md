---
description: Crea una matriz de rotación a partir de un cuaternión.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Función D3DXMatrixRotationQuaternion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649437"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="fabea-103">Función D3DXMatrixRotationQuaternion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fabea-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="fabea-104">Crea una matriz de rotación a partir de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="fabea-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="fabea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fabea-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="fabea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fabea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fabea-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fabea-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fabea-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fabea-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fabea-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fabea-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fabea-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fabea-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fabea-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fabea-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fabea-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="fabea-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fabea-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fabea-113">Return value</span></span>

<span data-ttu-id="fabea-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fabea-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fabea-115">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) creada a partir del cuaternión de origen.</span><span class="sxs-lookup"><span data-stu-id="fabea-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="fabea-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fabea-116">Remarks</span></span>

<span data-ttu-id="fabea-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="fabea-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fabea-118">De esta manera, la función **D3DXMatrixRotationQuaternion** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="fabea-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fabea-119">Para obtener información sobre cómo calcular valores de cuaternión desde un vector de dirección (x, y, z) y un ángulo de rotación, vea [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="fabea-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fabea-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fabea-120">Requirements</span></span>



| <span data-ttu-id="fabea-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fabea-121">Requirement</span></span> | <span data-ttu-id="fabea-122">Value</span><span class="sxs-lookup"><span data-stu-id="fabea-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fabea-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fabea-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fabea-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fabea-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fabea-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fabea-125">Library</span></span><br/> | <dl> <span data-ttu-id="fabea-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fabea-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fabea-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fabea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabea-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fabea-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fabea-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="fabea-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="fabea-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="fabea-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="fabea-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="fabea-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="fabea-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="fabea-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="fabea-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="fabea-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




