---
description: Interpola entre dos cuaterniones mediante la interpolación lineal esférica.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: Función D3DXQuaternionSlerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717711"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="c964d-103">Función D3DXQuaternionSlerp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c964d-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="c964d-104">Interpola entre dos cuaterniones mediante la interpolación lineal esférica.</span><span class="sxs-lookup"><span data-stu-id="c964d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c964d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c964d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="c964d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c964d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c964d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c964d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c964d-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c964d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c964d-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c964d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c964d-110">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c964d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c964d-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c964d-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c964d-112">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c964d-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c964d-113">*pQ2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c964d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c964d-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c964d-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c964d-115">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c964d-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c964d-116">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c964d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c964d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c964d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c964d-118">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="c964d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c964d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c964d-119">Return value</span></span>

<span data-ttu-id="c964d-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c964d-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c964d-121">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la interpolación.</span><span class="sxs-lookup"><span data-stu-id="c964d-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c964d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c964d-122">Remarks</span></span>

<span data-ttu-id="c964d-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="c964d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c964d-124">De esta manera, la función **D3DXQuaternionSlerp** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c964d-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c964d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="c964d-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c964d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c964d-126">Requirements</span></span>



| <span data-ttu-id="c964d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c964d-127">Requirement</span></span> | <span data-ttu-id="c964d-128">Value</span><span class="sxs-lookup"><span data-stu-id="c964d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c964d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c964d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c964d-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c964d-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c964d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c964d-131">Library</span></span><br/> | <dl> <span data-ttu-id="c964d-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c964d-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c964d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c964d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c964d-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c964d-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
