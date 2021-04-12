---
description: Calcular el término Fresnel.
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Función D3DXFresnelTerm (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6c6dd19dd6b7b70c5eeb08051f9799756b0782
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362568"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="c8a52-103">Función D3DXFresnelTerm (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c8a52-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="c8a52-104">Calcular el término Fresnel.</span><span class="sxs-lookup"><span data-stu-id="c8a52-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8a52-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c8a52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8a52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a52-107">*CosTheta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8a52-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a52-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8a52-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8a52-109">El valor debe estar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="c8a52-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="c8a52-110">*RefractionIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8a52-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a52-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8a52-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8a52-112">Índice de refracción de un material.</span><span class="sxs-lookup"><span data-stu-id="c8a52-112">The refraction index of a material.</span></span> <span data-ttu-id="c8a52-113">El valor debe ser mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="c8a52-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a52-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8a52-114">Return value</span></span>

<span data-ttu-id="c8a52-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8a52-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8a52-116">Esta función devuelve el término Fresnel para una luz no polarizada.</span><span class="sxs-lookup"><span data-stu-id="c8a52-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="c8a52-117">CosTheta es el coseno del ángulo del incidente.</span><span class="sxs-lookup"><span data-stu-id="c8a52-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a52-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8a52-118">Remarks</span></span>

<span data-ttu-id="c8a52-119">Para encontrar el término Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="c8a52-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="c8a52-120">Si un es el ángulo de incidencia y B es el ángulo de la refracción, entonces</span><span class="sxs-lookup"><span data-stu-id="c8a52-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="c8a52-121">A continuación, la expansión con las identidades trigonométricas y la simplificación, obtiene:</span><span class="sxs-lookup"><span data-stu-id="c8a52-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="c8a52-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a52-122">Requirements</span></span>



| <span data-ttu-id="c8a52-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a52-123">Requirement</span></span> | <span data-ttu-id="c8a52-124">Value</span><span class="sxs-lookup"><span data-stu-id="c8a52-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a52-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8a52-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c8a52-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8a52-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8a52-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8a52-127">Library</span></span><br/> | <dl> <span data-ttu-id="c8a52-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8a52-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8a52-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8a52-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a52-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c8a52-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
