---
description: 'Función D3DXQuaternionExp (D3dx9math.h): calcula el valor exponencial.'
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Función D3DXQuaternionExp (D3dx9math.h)
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
ms.openlocfilehash: 30e48e21e2dc6af487f1fb076af3b3f2df57f9f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094103"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="83ff3-103">Función D3DXQuaternionExp (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="83ff3-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="83ff3-104">Calcula el valor exponencial.</span><span class="sxs-lookup"><span data-stu-id="83ff3-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ff3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83ff3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="83ff3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83ff3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ff3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83ff3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83ff3-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="83ff3-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="83ff3-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="83ff3-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="83ff3-110">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="83ff3-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83ff3-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="83ff3-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="83ff3-112">Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="83ff3-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ff3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83ff3-113">Return value</span></span>

<span data-ttu-id="83ff3-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="83ff3-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="83ff3-115">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es exponencial.</span><span class="sxs-lookup"><span data-stu-id="83ff3-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="83ff3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83ff3-116">Remarks</span></span>

<span data-ttu-id="83ff3-117">Este método convierte un cuaternión puro en un cuaternión de unidad.</span><span class="sxs-lookup"><span data-stu-id="83ff3-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="83ff3-118">**D3DXQuaternionExp** espera un cuaternión puro, donde w se omite en el cálculo (w == 0).</span><span class="sxs-lookup"><span data-stu-id="83ff3-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="83ff3-119">donde v es la parte vectorial de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="83ff3-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="83ff3-120">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="83ff3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="83ff3-121">De esta manera, la **función D3DXQuaternionExp** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="83ff3-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="83ff3-122">El [**método D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) también se puede usar para configurar los puntos de control de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="83ff3-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="83ff3-123">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="83ff3-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="83ff3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83ff3-124">Requirements</span></span>



| <span data-ttu-id="83ff3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83ff3-125">Requirement</span></span> | <span data-ttu-id="83ff3-126">Value</span><span class="sxs-lookup"><span data-stu-id="83ff3-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83ff3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83ff3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="83ff3-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="83ff3-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="83ff3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83ff3-129">Library</span></span><br/> | <dl> <span data-ttu-id="83ff3-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="83ff3-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83ff3-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83ff3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ff3-132">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="83ff3-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="83ff3-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="83ff3-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="83ff3-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="83ff3-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




