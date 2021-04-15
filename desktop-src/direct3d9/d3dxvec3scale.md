---
description: Escala un vector 3D.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: Función D3DXVec3Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708098"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="01f5d-103">D3DXVec3Scale función)</span><span class="sxs-lookup"><span data-stu-id="01f5d-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="01f5d-104">Escala un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="01f5d-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01f5d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="01f5d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01f5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f5d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01f5d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01f5d-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="01f5d-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="01f5d-109">Puntero a la estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="01f5d-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="01f5d-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01f5d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f5d-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="01f5d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="01f5d-112">Puntero a la estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="01f5d-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="01f5d-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="01f5d-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f5d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01f5d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01f5d-115">Valor de escalado.</span><span class="sxs-lookup"><span data-stu-id="01f5d-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f5d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f5d-116">Return value</span></span>

<span data-ttu-id="01f5d-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="01f5d-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="01f5d-118">Puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que es el vector escalado.</span><span class="sxs-lookup"><span data-stu-id="01f5d-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="01f5d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01f5d-119">Remarks</span></span>

<span data-ttu-id="01f5d-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="01f5d-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="01f5d-121">De esta manera, la función **D3DXVec3Scale** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="01f5d-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f5d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f5d-122">Requirements</span></span>



| <span data-ttu-id="01f5d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f5d-123">Requirement</span></span> | <span data-ttu-id="01f5d-124">Value</span><span class="sxs-lookup"><span data-stu-id="01f5d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f5d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01f5d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="01f5d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="01f5d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="01f5d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01f5d-127">Library</span></span><br/> | <dl> <span data-ttu-id="01f5d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01f5d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01f5d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f5d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f5d-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="01f5d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="01f5d-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="01f5d-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="01f5d-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="01f5d-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
