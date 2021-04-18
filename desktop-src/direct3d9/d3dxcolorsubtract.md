---
description: Resta dos valores de color para crear un nuevo valor de color.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: Función D3DXColorSubtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718269"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="3b959-103">D3DXColorSubtract función)</span><span class="sxs-lookup"><span data-stu-id="3b959-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="3b959-104">Resta dos valores de color para crear un nuevo valor de color.</span><span class="sxs-lookup"><span data-stu-id="3b959-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b959-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b959-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="3b959-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b959-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b959-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3b959-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b959-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b959-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3b959-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3b959-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3b959-110">*pC1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b959-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b959-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b959-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3b959-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="3b959-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b959-113">*pC2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b959-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b959-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b959-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3b959-115">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="3b959-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b959-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b959-116">Return value</span></span>

<span data-ttu-id="3b959-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b959-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3b959-118">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es la diferencia entre dos valores de color.</span><span class="sxs-lookup"><span data-stu-id="3b959-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b959-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b959-119">Remarks</span></span>

<span data-ttu-id="3b959-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3b959-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3b959-121">De esta manera, la función **D3DXColorSubtract** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="3b959-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b959-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b959-122">Requirements</span></span>



| <span data-ttu-id="3b959-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b959-123">Requirement</span></span> | <span data-ttu-id="3b959-124">Value</span><span class="sxs-lookup"><span data-stu-id="3b959-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b959-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b959-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3b959-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b959-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3b959-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b959-127">Library</span></span><br/> | <dl> <span data-ttu-id="3b959-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b959-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3b959-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b959-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b959-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3b959-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3b959-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="3b959-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




