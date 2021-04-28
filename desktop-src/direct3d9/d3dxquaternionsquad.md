---
description: 'Función D3DXQuaternionSquad (D3dx9math.h): interpola entre cuaterniones, mediante la interpolación de cuadrángulo esférico.'
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: Función D3DXQuaternionSquad (D3dx9math.h)
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
ms.openlocfilehash: c7bef8671b38ec2e8208a6de0ec7542cf28ffa44
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117993"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="30dc7-103">Función D3DXQuaternionSquad (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="30dc7-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="30dc7-104">Interpola entre cuaterniones mediante la interpolación de cuadrángulo esférica.</span><span class="sxs-lookup"><span data-stu-id="30dc7-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="30dc7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30dc7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="30dc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30dc7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="30dc7-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="30dc7-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="30dc7-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="30dc7-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-112">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="30dc7-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30dc7-113">*pA* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="30dc7-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-115">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="30dc7-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30dc7-116">*pB* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="30dc7-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-118">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="30dc7-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30dc7-119">*pC* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="30dc7-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-121">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="30dc7-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30dc7-122">*t* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="30dc7-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30dc7-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30dc7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30dc7-124">Parámetro que indica hasta qué punto se debe interpolar entre los cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="30dc7-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30dc7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30dc7-125">Return value</span></span>

<span data-ttu-id="30dc7-126">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="30dc7-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="30dc7-127">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la interpolación esférica de cuadrángulo.</span><span class="sxs-lookup"><span data-stu-id="30dc7-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="30dc7-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30dc7-128">Remarks</span></span>

<span data-ttu-id="30dc7-129">Esta función usa la siguiente secuencia de operaciones de interpolación lineal esférica:</span><span class="sxs-lookup"><span data-stu-id="30dc7-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="30dc7-130">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="30dc7-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="30dc7-131">De esta manera, la **función D3DXQuaternionSquad** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="30dc7-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="30dc7-132">Para obtener un ejemplo de interpolación entre cuaterniones, consulte el ejemplo de SkinnedMesh.</span><span class="sxs-lookup"><span data-stu-id="30dc7-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="30dc7-133">Puede obtener este ejemplo y obtener información sobre él en el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="30dc7-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="30dc7-134">Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="30dc7-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="30dc7-135">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="30dc7-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="30dc7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30dc7-136">Requirements</span></span>



| <span data-ttu-id="30dc7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="30dc7-137">Requirement</span></span> | <span data-ttu-id="30dc7-138">Value</span><span class="sxs-lookup"><span data-stu-id="30dc7-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30dc7-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30dc7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="30dc7-140"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="30dc7-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="30dc7-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30dc7-141">Library</span></span><br/> | <dl> <span data-ttu-id="30dc7-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="30dc7-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30dc7-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30dc7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dc7-144">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="30dc7-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="30dc7-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="30dc7-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="30dc7-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="30dc7-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="30dc7-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="30dc7-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
