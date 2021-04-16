---
description: Agrega dos valores de color juntos para crear un nuevo valor de color.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Función D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678827"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="e1250-103">D3DXColorAdd función)</span><span class="sxs-lookup"><span data-stu-id="e1250-103">D3DXColorAdd function</span></span>

<span data-ttu-id="e1250-104">Agrega dos valores de color juntos para crear un nuevo valor de color.</span><span class="sxs-lookup"><span data-stu-id="e1250-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1250-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1250-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="e1250-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1250-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e1250-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1250-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1250-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e1250-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e1250-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e1250-110">*pC1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1250-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1250-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1250-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e1250-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e1250-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e1250-113">*pC2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1250-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1250-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1250-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e1250-115">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="e1250-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1250-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1250-116">Return value</span></span>

<span data-ttu-id="e1250-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1250-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="e1250-118">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es la suma de dos valores de color.</span><span class="sxs-lookup"><span data-stu-id="e1250-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1250-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1250-119">Remarks</span></span>

<span data-ttu-id="e1250-120">El valor devuelto para esta función es el mismo valor devuelto en pOut.</span><span class="sxs-lookup"><span data-stu-id="e1250-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="e1250-121">De esta manera, la función **D3DXColorAdd** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="e1250-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1250-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1250-122">Requirements</span></span>



| <span data-ttu-id="e1250-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1250-123">Requirement</span></span> | <span data-ttu-id="e1250-124">Value</span><span class="sxs-lookup"><span data-stu-id="e1250-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1250-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1250-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e1250-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1250-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1250-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1250-127">Library</span></span><br/> | <dl> <span data-ttu-id="e1250-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1250-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1250-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1250-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1250-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e1250-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e1250-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="e1250-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="e1250-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="e1250-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




