---
description: Escala un vector 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Función D3DXVec4Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707913"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="7e476-103">D3DXVec4Scale función)</span><span class="sxs-lookup"><span data-stu-id="7e476-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="7e476-104">Escala un vector 4D.</span><span class="sxs-lookup"><span data-stu-id="7e476-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e476-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e476-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="7e476-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e476-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e476-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7e476-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e476-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e476-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="7e476-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7e476-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e476-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e476-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e476-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e476-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="7e476-112">Puntero a la estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="7e476-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e476-113">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7e476-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e476-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e476-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e476-115">Valor de escalado.</span><span class="sxs-lookup"><span data-stu-id="7e476-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e476-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e476-116">Return value</span></span>

<span data-ttu-id="7e476-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e476-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="7e476-118">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el vector escalado.</span><span class="sxs-lookup"><span data-stu-id="7e476-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e476-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e476-119">Remarks</span></span>

<span data-ttu-id="7e476-120">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="7e476-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7e476-121">De esta manera, la función **D3DXVec4Scale** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="7e476-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e476-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e476-122">Requirements</span></span>



| <span data-ttu-id="7e476-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e476-123">Requirement</span></span> | <span data-ttu-id="7e476-124">Value</span><span class="sxs-lookup"><span data-stu-id="7e476-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e476-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e476-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7e476-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e476-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7e476-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e476-127">Library</span></span><br/> | <dl> <span data-ttu-id="7e476-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e476-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e476-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e476-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e476-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="7e476-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7e476-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="7e476-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="7e476-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="7e476-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
