---
description: 'Función D3DXMatrixRotationQuaternion (D3DX10Math.h): crea una matriz de rotación a partir de un cuaternión.'
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Función D3DXMatrixRotationQuaternion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103433"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="92b38-103">Función D3DXMatrixRotationQuaternion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="92b38-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="92b38-104">Crea una matriz de rotación a partir de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="92b38-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92b38-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="92b38-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92b38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b38-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92b38-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b38-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="92b38-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92b38-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="92b38-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="92b38-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="92b38-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b38-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="92b38-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="92b38-112">Puntero a la estructura D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="92b38-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b38-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92b38-113">Return value</span></span>

<span data-ttu-id="92b38-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="92b38-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="92b38-115">Puntero a una estructura D3DXMATRIX creada a partir del cuaternión de origen.</span><span class="sxs-lookup"><span data-stu-id="92b38-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b38-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92b38-116">Remarks</span></span>

<span data-ttu-id="92b38-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="92b38-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="92b38-118">De este modo, la función D3DXMatrixRotationQuaternion se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="92b38-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="92b38-119">Para obtener información sobre cómo calcular valores de cuaternión a partir de un vector de dirección (x, y, z) y un ángulo de rotación, vea [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="92b38-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92b38-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b38-120">Requirements</span></span>



| <span data-ttu-id="92b38-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b38-121">Requirement</span></span> | <span data-ttu-id="92b38-122">Value</span><span class="sxs-lookup"><span data-stu-id="92b38-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92b38-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92b38-123">Header</span></span><br/>  | <dl> <span data-ttu-id="92b38-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="92b38-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="92b38-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92b38-125">Library</span></span><br/> | <dl> <span data-ttu-id="92b38-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b38-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92b38-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="92b38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b38-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="92b38-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
