---
description: Crea una matriz que gira en torno a un eje arbitrario.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Función D3DXMatrixRotationAxis (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083786"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="d926f-103">Función D3DXMatrixRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d926f-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="d926f-104">Crea una matriz que gira en torno a un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d926f-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d926f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d926f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="d926f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d926f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d926f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d926f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d926f-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d926f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d926f-109">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d926f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d926f-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d926f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d926f-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d926f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d926f-112">Puntero al eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d926f-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="d926f-113">Vea [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="d926f-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="d926f-114">*Ángulo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d926f-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d926f-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d926f-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d926f-116">Ángulo de rotación en radianes.</span><span class="sxs-lookup"><span data-stu-id="d926f-116">Angle of rotation in radians.</span></span> <span data-ttu-id="d926f-117">Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="d926f-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d926f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d926f-118">Return value</span></span>

<span data-ttu-id="d926f-119">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d926f-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d926f-120">Puntero a una estructura D3DXMATRIX girada alrededor del eje especificado.</span><span class="sxs-lookup"><span data-stu-id="d926f-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="d926f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d926f-121">Remarks</span></span>

<span data-ttu-id="d926f-122">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d926f-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d926f-123">De esta manera, la función D3DXMatrixRotationAxis se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="d926f-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d926f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d926f-124">Requirements</span></span>



| <span data-ttu-id="d926f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d926f-125">Requirement</span></span> | <span data-ttu-id="d926f-126">Value</span><span class="sxs-lookup"><span data-stu-id="d926f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d926f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d926f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d926f-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d926f-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d926f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d926f-129">Library</span></span><br/> | <dl> <span data-ttu-id="d926f-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d926f-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d926f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d926f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d926f-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d926f-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
