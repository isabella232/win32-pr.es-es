---
description: Calcular el término Fresnel.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Función D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548094"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="94b69-103">Función D3DXFresnelTerm (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="94b69-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="94b69-104">Calcular el término Fresnel.</span><span class="sxs-lookup"><span data-stu-id="94b69-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94b69-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="94b69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94b69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94b69-107">*CosTheta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94b69-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b69-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94b69-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94b69-109">El valor debe estar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="94b69-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="94b69-110">*RefractionIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94b69-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94b69-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94b69-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94b69-112">Índice de refracción de un material.</span><span class="sxs-lookup"><span data-stu-id="94b69-112">The refraction index of a material.</span></span> <span data-ttu-id="94b69-113">El valor debe ser mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="94b69-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94b69-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94b69-114">Return value</span></span>

<span data-ttu-id="94b69-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94b69-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94b69-116">Esta función devuelve el término Fresnel para una luz no polarizada.</span><span class="sxs-lookup"><span data-stu-id="94b69-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="94b69-117">CosTheta es el coseno del ángulo del incidente.</span><span class="sxs-lookup"><span data-stu-id="94b69-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b69-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94b69-118">Remarks</span></span>

<span data-ttu-id="94b69-119">Para encontrar el término Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="94b69-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="94b69-120">Si un es el ángulo de incidencia y B es el ángulo de la refracción, entonces</span><span class="sxs-lookup"><span data-stu-id="94b69-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="94b69-121">A continuación, la expansión con las identidades trigonométricas y la simplificación, obtiene:</span><span class="sxs-lookup"><span data-stu-id="94b69-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="94b69-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b69-122">Requirements</span></span>



| <span data-ttu-id="94b69-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b69-123">Requirement</span></span> | <span data-ttu-id="94b69-124">Value</span><span class="sxs-lookup"><span data-stu-id="94b69-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b69-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94b69-125">Header</span></span><br/>  | <dl> <span data-ttu-id="94b69-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b69-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="94b69-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94b69-127">Library</span></span><br/> | <dl> <span data-ttu-id="94b69-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94b69-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94b69-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="94b69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b69-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="94b69-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
