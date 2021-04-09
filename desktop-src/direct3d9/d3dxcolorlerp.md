---
description: Utiliza la interpolación lineal para crear un valor de color.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Función D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914745"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="00460-103">D3DXColorLerp función)</span><span class="sxs-lookup"><span data-stu-id="00460-103">D3DXColorLerp function</span></span>

<span data-ttu-id="00460-104">Utiliza la interpolación lineal para crear un valor de color.</span><span class="sxs-lookup"><span data-stu-id="00460-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="00460-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00460-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="00460-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00460-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00460-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="00460-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00460-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="00460-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="00460-109">Puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="00460-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="00460-110">*pC1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00460-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00460-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="00460-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="00460-112">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="00460-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="00460-113">*pC2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00460-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00460-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="00460-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="00460-115">Puntero a una estructura de [**D3DXCOLOR**](d3dxcolor.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="00460-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="00460-116">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="00460-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00460-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00460-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00460-118">Parámetro que se interpola linealmente entre los colores, pC1 y pC2, tratando ambos como vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="00460-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="00460-119">No hay ningún límite en el valor de s.</span><span class="sxs-lookup"><span data-stu-id="00460-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00460-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00460-120">Return value</span></span>

<span data-ttu-id="00460-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="00460-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="00460-122">Esta función devuelve un puntero a una estructura [**D3DXCOLOR**](d3dxcolor.md) que es el resultado de la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="00460-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="00460-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00460-123">Remarks</span></span>

<span data-ttu-id="00460-124">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="00460-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="00460-125">De esta manera, la función **D3DXColorLerp** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="00460-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="00460-126">Esta función interpola los componentes rojo, verde, azul y alfa de una estructura [**D3DXCOLOR**](d3dxcolor.md) entre dos colores, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="00460-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="00460-127">Si va a interpolar linealmente entre los colores A y B, y s es 0, el color resultante es. Si es 1, el color resultante es el color B.</span><span class="sxs-lookup"><span data-stu-id="00460-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="00460-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00460-128">Requirements</span></span>



| <span data-ttu-id="00460-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="00460-129">Requirement</span></span> | <span data-ttu-id="00460-130">Value</span><span class="sxs-lookup"><span data-stu-id="00460-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00460-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00460-131">Header</span></span><br/>  | <dl> <span data-ttu-id="00460-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="00460-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="00460-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00460-133">Library</span></span><br/> | <dl> <span data-ttu-id="00460-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00460-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00460-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="00460-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00460-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="00460-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="00460-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="00460-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="00460-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="00460-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="00460-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="00460-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
