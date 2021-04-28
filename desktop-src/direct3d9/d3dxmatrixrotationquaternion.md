---
description: 'Función D3DXMatrixRotationQuaternion (D3dx9math.h): crea una matriz de rotación a partir de un cuaternión.'
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Función D3DXMatrixRotationQuaternion (D3dx9math.h)
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
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118203"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="a5153-103">Función D3DXMatrixRotationQuaternion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a5153-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="a5153-104">Crea una matriz de rotación a partir de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="a5153-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5153-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5153-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a5153-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5153-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5153-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5153-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a5153-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a5153-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a5153-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a5153-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a5153-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5153-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5153-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a5153-112">Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="a5153-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5153-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5153-113">Return value</span></span>

<span data-ttu-id="a5153-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a5153-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a5153-115">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) creada a partir del cuaternión de origen.</span><span class="sxs-lookup"><span data-stu-id="a5153-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5153-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5153-116">Remarks</span></span>

<span data-ttu-id="a5153-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="a5153-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a5153-118">De esta manera, la **función D3DXMatrixRotationQuaternion** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="a5153-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a5153-119">Para obtener información sobre cómo calcular valores de cuaternión a partir de un vector de dirección (x, y, z ) y un ángulo de rotación, vea [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="a5153-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5153-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5153-120">Requirements</span></span>



| <span data-ttu-id="a5153-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5153-121">Requirement</span></span> | <span data-ttu-id="a5153-122">Value</span><span class="sxs-lookup"><span data-stu-id="a5153-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5153-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5153-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a5153-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a5153-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a5153-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5153-125">Library</span></span><br/> | <dl> <span data-ttu-id="a5153-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5153-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5153-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5153-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5153-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a5153-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a5153-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a5153-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a5153-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="a5153-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="a5153-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="a5153-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="a5153-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a5153-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="a5153-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="a5153-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




