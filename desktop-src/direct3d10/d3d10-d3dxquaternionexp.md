---
description: Calcula el valor exponencial.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Función D3DXQuaternionExp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821255"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="868fd-103">Función D3DXQuaternionExp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="868fd-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="868fd-104">Calcula el valor exponencial.</span><span class="sxs-lookup"><span data-stu-id="868fd-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="868fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="868fd-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="868fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="868fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868fd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="868fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="868fd-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="868fd-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="868fd-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="868fd-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="868fd-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="868fd-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868fd-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="868fd-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="868fd-112">Puntero a la estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="868fd-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868fd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="868fd-113">Return value</span></span>

<span data-ttu-id="868fd-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="868fd-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="868fd-115">Puntero a una estructura D3DXQUATERNION que es exponencial.</span><span class="sxs-lookup"><span data-stu-id="868fd-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="868fd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="868fd-116">Remarks</span></span>

<span data-ttu-id="868fd-117">Este método convierte un cuaternión puro en un cuaternión de unidad.</span><span class="sxs-lookup"><span data-stu-id="868fd-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="868fd-118">D3DXQuaternionExp espera un cuaternión puro, donde w se omite en el cálculo (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="868fd-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="868fd-119">donde v es la parte del vector de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="868fd-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="868fd-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="868fd-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="868fd-121">De esta manera, la función D3DXQuaternionExp se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="868fd-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="868fd-122">El método [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) también se puede utilizar para configurar los puntos de control de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="868fd-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="868fd-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="868fd-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="868fd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="868fd-124">Requirements</span></span>



| <span data-ttu-id="868fd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="868fd-125">Requirement</span></span> | <span data-ttu-id="868fd-126">Value</span><span class="sxs-lookup"><span data-stu-id="868fd-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="868fd-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="868fd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="868fd-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="868fd-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="868fd-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="868fd-129">Library</span></span><br/> | <dl> <span data-ttu-id="868fd-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="868fd-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="868fd-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="868fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868fd-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="868fd-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
