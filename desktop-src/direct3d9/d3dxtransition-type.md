---
description: Define el estilo de transición entre los valores de una animación de malla.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumeración D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003804"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="46715-103">\_Enumeración de tipo D3DXTRANSITION</span><span class="sxs-lookup"><span data-stu-id="46715-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="46715-104">Define el estilo de transición entre los valores de una animación de malla.</span><span class="sxs-lookup"><span data-stu-id="46715-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46715-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46715-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="46715-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="46715-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="46715-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**\_Lineal D3DXTRANSITION**</span><span class="sxs-lookup"><span data-stu-id="46715-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="46715-108">Transición lineal entre valores.</span><span class="sxs-lookup"><span data-stu-id="46715-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="46715-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**</span><span class="sxs-lookup"><span data-stu-id="46715-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="46715-110">Aceleración de la transición spline de fácil entrada entre valores.</span><span class="sxs-lookup"><span data-stu-id="46715-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="46715-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="46715-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="46715-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="46715-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="46715-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="46715-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="46715-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="46715-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46715-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46715-115">Remarks</span></span>

<span data-ttu-id="46715-116">El cálculo de la rampa de la entrada lenta a la salida se calcula de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="46715-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="46715-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="46715-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="46715-118">donde la rampa es una función Q (t) con las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="46715-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="46715-119">Q (t) es una spline cúbica.</span><span class="sxs-lookup"><span data-stu-id="46715-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="46715-120">Q (t) se interpola entre x e y como t oscila entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="46715-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="46715-121">Q (t) es horizontal cuando t = 0 y t = 1.</span><span class="sxs-lookup"><span data-stu-id="46715-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="46715-122">Matemáticamente, esto se traduce en:</span><span class="sxs-lookup"><span data-stu-id="46715-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="46715-123">Q (t) = at ³ + BT ² + CT + D (y, por lo tanto, Q ' (t) = 3At ² + 2Bt + C)</span><span class="sxs-lookup"><span data-stu-id="46715-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="46715-124">2A) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="46715-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="46715-125">2B) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="46715-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="46715-126">3A) Q ' (0) = 0</span><span class="sxs-lookup"><span data-stu-id="46715-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="46715-127">3B) Q ' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="46715-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="46715-128">Resolver para A, B, C, D:</span><span class="sxs-lookup"><span data-stu-id="46715-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="46715-129">D = x (desde 2A)</span><span class="sxs-lookup"><span data-stu-id="46715-129">D = x (from 2a)</span></span>  
<span data-ttu-id="46715-130">C = 0 (de 3A)</span><span class="sxs-lookup"><span data-stu-id="46715-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="46715-131">3A + 2B = 0 (de 3B)</span><span class="sxs-lookup"><span data-stu-id="46715-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="46715-132">A + B = y-x (de 2B y D = x)</span><span class="sxs-lookup"><span data-stu-id="46715-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="46715-133">Por lo tanto:</span><span class="sxs-lookup"><span data-stu-id="46715-133">Therefore:</span></span>

<dl> <span data-ttu-id="46715-134">A = 2 (x-y), B = 3 (y-x), C = 0, D = x</span><span class="sxs-lookup"><span data-stu-id="46715-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="46715-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46715-135">Requirements</span></span>



| <span data-ttu-id="46715-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="46715-136">Requirement</span></span> | <span data-ttu-id="46715-137">Value</span><span class="sxs-lookup"><span data-stu-id="46715-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46715-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46715-138">Header</span></span><br/> | <dl> <span data-ttu-id="46715-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="46715-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46715-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="46715-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46715-141">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="46715-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




