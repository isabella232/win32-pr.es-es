---
description: Realiza una interpolación lineal entre dos vectores 3D.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: Función D3DXVec3Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718526"
---
# <a name="d3dxvec3lerp-function"></a><span data-ttu-id="87e6c-103">D3DXVec3Lerp función)</span><span class="sxs-lookup"><span data-stu-id="87e6c-103">D3DXVec3Lerp function</span></span>

<span data-ttu-id="87e6c-104">Realiza una interpolación lineal entre dos vectores 3D.</span><span class="sxs-lookup"><span data-stu-id="87e6c-104">Performs a linear interpolation between two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e6c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87e6c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="87e6c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87e6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e6c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87e6c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e6c-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="87e6c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87e6c-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="87e6c-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87e6c-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87e6c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e6c-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87e6c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87e6c-112">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="87e6c-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87e6c-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="87e6c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e6c-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87e6c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87e6c-115">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="87e6c-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="87e6c-116">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="87e6c-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e6c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87e6c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87e6c-118">Parámetro que se interpola linealmente entre los vectores.</span><span class="sxs-lookup"><span data-stu-id="87e6c-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e6c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87e6c-119">Return value</span></span>

<span data-ttu-id="87e6c-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="87e6c-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="87e6c-121">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="87e6c-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e6c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87e6c-122">Remarks</span></span>

<span data-ttu-id="87e6c-123">Esta función realiza la interpolación lineal basada en la siguiente fórmula: v1 + s (V2-V1).</span><span class="sxs-lookup"><span data-stu-id="87e6c-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="87e6c-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="87e6c-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="87e6c-125">De esta manera, la función **D3DXVec3Lerp** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="87e6c-125">In this way, the **D3DXVec3Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e6c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e6c-126">Requirements</span></span>



| <span data-ttu-id="87e6c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e6c-127">Requirement</span></span> | <span data-ttu-id="87e6c-128">Value</span><span class="sxs-lookup"><span data-stu-id="87e6c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e6c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87e6c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="87e6c-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e6c-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="87e6c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87e6c-131">Library</span></span><br/> | <dl> <span data-ttu-id="87e6c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87e6c-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87e6c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="87e6c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e6c-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="87e6c-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
