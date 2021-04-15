---
description: Calcula el valor exponencial.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Función D3DXQuaternionExp (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9cb5765e01c4fbbc6ab3785363425262ee491ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707828"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="e8b00-103">Función D3DXQuaternionExp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e8b00-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="e8b00-104">Calcula el valor exponencial.</span><span class="sxs-lookup"><span data-stu-id="e8b00-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8b00-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="e8b00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8b00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b00-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e8b00-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b00-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8b00-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8b00-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e8b00-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e8b00-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8b00-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b00-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8b00-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8b00-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e8b00-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b00-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8b00-113">Return value</span></span>

<span data-ttu-id="e8b00-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8b00-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8b00-115">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es exponencial.</span><span class="sxs-lookup"><span data-stu-id="e8b00-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b00-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8b00-116">Remarks</span></span>

<span data-ttu-id="e8b00-117">Este método convierte un cuaternión puro en un cuaternión de unidad.</span><span class="sxs-lookup"><span data-stu-id="e8b00-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="e8b00-118">**D3DXQuaternionExp** espera un cuaternión puro, donde w se omite en el cálculo (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="e8b00-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="e8b00-119">donde v es la parte del vector de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e8b00-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="e8b00-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="e8b00-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e8b00-121">De esta manera, la función **D3DXQuaternionExp** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e8b00-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e8b00-122">El método [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) también se puede utilizar para configurar los puntos de control de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="e8b00-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="e8b00-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="e8b00-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b00-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8b00-124">Requirements</span></span>



| <span data-ttu-id="e8b00-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b00-125">Requirement</span></span> | <span data-ttu-id="e8b00-126">Value</span><span class="sxs-lookup"><span data-stu-id="e8b00-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b00-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8b00-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e8b00-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b00-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e8b00-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8b00-129">Library</span></span><br/> | <dl> <span data-ttu-id="e8b00-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8b00-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8b00-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8b00-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b00-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e8b00-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e8b00-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="e8b00-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="e8b00-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="e8b00-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




