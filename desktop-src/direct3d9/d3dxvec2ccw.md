---
description: Devuelve el componente z tomando el producto cruzado de dos vectores 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Función D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707861"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="8b3bc-103">D3DXVec2CCW función)</span><span class="sxs-lookup"><span data-stu-id="8b3bc-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="8b3bc-104">Devuelve el componente z tomando el producto cruzado de dos vectores 2D.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b3bc-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="8b3bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b3bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b3bc-107">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b3bc-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3bc-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b3bc-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8b3bc-109">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b3bc-110">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b3bc-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b3bc-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b3bc-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8b3bc-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b3bc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b3bc-113">Return value</span></span>

<span data-ttu-id="8b3bc-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b3bc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b3bc-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b3bc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b3bc-116">Remarks</span></span>

<span data-ttu-id="8b3bc-117">Esta función determina el componente z determinando el producto cruzado basado en la siguiente fórmula: ((x1, Y1, 0) Cross (x2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="8b3bc-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="8b3bc-118">O tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="8b3bc-119">Si el valor del componente z es positivo, el vector V2 es en sentido contrario a las agujas del reloj desde el vector v1.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="8b3bc-120">Esta información es útil para la selección de la cara posterior.</span><span class="sxs-lookup"><span data-stu-id="8b3bc-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3bc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b3bc-121">Requirements</span></span>



| <span data-ttu-id="8b3bc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b3bc-122">Requirement</span></span> | <span data-ttu-id="8b3bc-123">Value</span><span class="sxs-lookup"><span data-stu-id="8b3bc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3bc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b3bc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8b3bc-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b3bc-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8b3bc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b3bc-126">Library</span></span><br/> | <dl> <span data-ttu-id="8b3bc-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b3bc-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b3bc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b3bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3bc-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="8b3bc-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8b3bc-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="8b3bc-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
