---
description: Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Función D3DXQuaternionSquad (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698220"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="c08aa-103">Función D3DXQuaternionSquad (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c08aa-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="c08aa-104">Interpola entre cuaterniones mediante la interpolación Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="c08aa-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c08aa-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c08aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c08aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08aa-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c08aa-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c08aa-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c08aa-110">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c08aa-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-112">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c08aa-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c08aa-113">*PA* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c08aa-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-115">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c08aa-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c08aa-116">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c08aa-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-118">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c08aa-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c08aa-119">*PC* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="c08aa-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-121">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c08aa-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c08aa-122">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c08aa-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08aa-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c08aa-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c08aa-124">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="c08aa-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08aa-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c08aa-125">Return value</span></span>

<span data-ttu-id="c08aa-126">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c08aa-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c08aa-127">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la interpolación Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="c08aa-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c08aa-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c08aa-128">Remarks</span></span>

<span data-ttu-id="c08aa-129">Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:</span><span class="sxs-lookup"><span data-stu-id="c08aa-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="c08aa-130">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="c08aa-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c08aa-131">De esta manera, la función **D3DXQuaternionSquad** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c08aa-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c08aa-132">Para obtener un ejemplo de la interpolación entre cuaterniones, vea el ejemplo SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="c08aa-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="c08aa-133">Puede obtener este ejemplo y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="c08aa-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="c08aa-134">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="c08aa-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="c08aa-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="c08aa-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08aa-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c08aa-136">Requirements</span></span>



| <span data-ttu-id="c08aa-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08aa-137">Requirement</span></span> | <span data-ttu-id="c08aa-138">Value</span><span class="sxs-lookup"><span data-stu-id="c08aa-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c08aa-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c08aa-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c08aa-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c08aa-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c08aa-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c08aa-141">Library</span></span><br/> | <dl> <span data-ttu-id="c08aa-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c08aa-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c08aa-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="c08aa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08aa-144">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c08aa-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c08aa-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="c08aa-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="c08aa-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="c08aa-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="c08aa-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="c08aa-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
