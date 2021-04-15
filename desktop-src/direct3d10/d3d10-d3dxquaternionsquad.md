---
description: Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Función D3DXQuaternionSquad (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548022"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="ee32a-103">Función D3DXQuaternionSquad (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ee32a-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="ee32a-104">Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="ee32a-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee32a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee32a-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="ee32a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee32a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee32a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee32a-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ee32a-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ee32a-110">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee32a-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-112">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="ee32a-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee32a-113">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-114">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee32a-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-115">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="ee32a-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee32a-116">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee32a-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-118">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="ee32a-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee32a-119">*PC* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee32a-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-121">Puntero a una estructura de D3DXQUATERNION de origen.</span><span class="sxs-lookup"><span data-stu-id="ee32a-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="ee32a-122">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ee32a-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee32a-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee32a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee32a-124">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="ee32a-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee32a-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee32a-125">Return value</span></span>

<span data-ttu-id="ee32a-126">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee32a-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ee32a-127">Puntero a una estructura D3DXQUATERNION que es el resultado de la interpolación Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="ee32a-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee32a-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee32a-128">Remarks</span></span>

<span data-ttu-id="ee32a-129">Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:</span><span class="sxs-lookup"><span data-stu-id="ee32a-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="ee32a-130">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="ee32a-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ee32a-131">De esta manera, la función D3DXQuaternionSquad se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="ee32a-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ee32a-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="ee32a-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee32a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee32a-133">Requirements</span></span>



| <span data-ttu-id="ee32a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee32a-134">Requirement</span></span> | <span data-ttu-id="ee32a-135">Value</span><span class="sxs-lookup"><span data-stu-id="ee32a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee32a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee32a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ee32a-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee32a-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ee32a-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee32a-138">Library</span></span><br/> | <dl> <span data-ttu-id="ee32a-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee32a-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee32a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee32a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee32a-141">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="ee32a-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
