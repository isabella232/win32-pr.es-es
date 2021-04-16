---
description: Ajusta el valor de contraste de un color.
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Función D3DXColorAdjustContrast (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6765f442b6a2550ba262073f61c876e3b3ae1fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678816"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="5ebd9-103">Función D3DXColorAdjustContrast (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="5ebd9-104">Ajusta el valor de contraste de un color.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebd9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ebd9-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="5ebd9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ebd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebd9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ebd9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebd9-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ebd9-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5ebd9-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd9-110">*PC* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5ebd9-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebd9-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ebd9-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5ebd9-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd9-113">*c* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="5ebd9-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebd9-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ebd9-115">Valor de contraste.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-115">Contrast value.</span></span> <span data-ttu-id="5ebd9-116">Este parámetro se interpola linealmente entre el 50% de gris y el color, el equipo.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="5ebd9-117">No hay límites en el valor de c.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-117">There are not limits on the value of c.</span></span> <span data-ttu-id="5ebd9-118">Si este parámetro es cero, el color devuelto es 50 por ciento de gris.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="5ebd9-119">Si este parámetro es 1, el color devuelto es el color original.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebd9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ebd9-120">Return value</span></span>

<span data-ttu-id="5ebd9-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ebd9-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5ebd9-122">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado del ajuste de contraste.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebd9-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ebd9-123">Remarks</span></span>

<span data-ttu-id="5ebd9-124">El canal alfa de entrada se copia, sin modificar, en el canal alfa de salida.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="5ebd9-125">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5ebd9-126">De esta manera, esta función se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5ebd9-127">Esta función interpola los componentes de color rojo, verde y azul de una estructura [**D3DXCOLOR**](d3dxcolor.md) entre el 50% de gris y un valor de contraste especificado, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="5ebd9-128">Si c es mayor que 0 y menor que 1, se reduce el contraste.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="5ebd9-129">Si c es mayor que 1, se aumenta el contraste.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebd9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebd9-130">Requirements</span></span>



| <span data-ttu-id="5ebd9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebd9-131">Requirement</span></span> | <span data-ttu-id="5ebd9-132">Value</span><span class="sxs-lookup"><span data-stu-id="5ebd9-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebd9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ebd9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5ebd9-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd9-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ebd9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ebd9-135">Library</span></span><br/> | <dl> <span data-ttu-id="5ebd9-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd9-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ebd9-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ebd9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebd9-138">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="5ebd9-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5ebd9-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
