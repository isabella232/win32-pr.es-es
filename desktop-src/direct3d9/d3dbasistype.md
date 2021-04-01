---
description: Define el tipo base de una superficie de revisión de orden superior.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumeración D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157152"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="b55d0-103">Enumeración D3DBASISTYPE</span><span class="sxs-lookup"><span data-stu-id="b55d0-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="b55d0-104">Define el tipo base de una superficie de revisión de orden superior.</span><span class="sxs-lookup"><span data-stu-id="b55d0-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b55d0-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="b55d0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b55d0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b55d0-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bézier**</span><span class="sxs-lookup"><span data-stu-id="b55d0-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="b55d0-108">Los vértices de entrada se tratan como una serie de revisiones de Bézier.</span><span class="sxs-lookup"><span data-stu-id="b55d0-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="b55d0-109">El número de vértices especificado debe ser divisible por 4.</span><span class="sxs-lookup"><span data-stu-id="b55d0-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="b55d0-110">No se representarán las partes de la malla que superen este criterio.</span><span class="sxs-lookup"><span data-stu-id="b55d0-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="b55d0-111">Se supone una continuidad completa entre las subrevisiones en el interior de la superficie representada por cada llamada.</span><span class="sxs-lookup"><span data-stu-id="b55d0-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="b55d0-112">Solo se garantiza que los vértices de las esquinas de cada subrevisión se encuentran en la superficie resultante.</span><span class="sxs-lookup"><span data-stu-id="b55d0-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="b55d0-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**</span><span class="sxs-lookup"><span data-stu-id="b55d0-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="b55d0-114">Los vértices de entrada se tratan como puntos de control de una superficie de spline B.</span><span class="sxs-lookup"><span data-stu-id="b55d0-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="b55d0-115">El número de aberturas representadas es dos veces menor que el número de aberturas en esa dirección.</span><span class="sxs-lookup"><span data-stu-id="b55d0-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="b55d0-116">En general, la superficie generada no contiene los vértices de control especificados.</span><span class="sxs-lookup"><span data-stu-id="b55d0-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="b55d0-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="b55d0-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="b55d0-118">Una base de interpolación define la superficie para que la superficie pase por todos los vértices de entrada especificados.</span><span class="sxs-lookup"><span data-stu-id="b55d0-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="b55d0-119">En DirectX 8, esto era D3DBASIS \_ Interpolate.</span><span class="sxs-lookup"><span data-stu-id="b55d0-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="b55d0-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b55d0-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b55d0-121">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b55d0-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b55d0-122">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b55d0-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b55d0-123">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b55d0-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b55d0-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b55d0-124">Remarks</span></span>

<span data-ttu-id="b55d0-125">Los miembros de **D3DBASISTYPE** especifican la formulación que se va a usar en la evaluación de la primitiva de la superficie de revisión de orden superior durante la teselación.</span><span class="sxs-lookup"><span data-stu-id="b55d0-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b55d0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b55d0-126">Requirements</span></span>



| <span data-ttu-id="b55d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b55d0-127">Requirement</span></span> | <span data-ttu-id="b55d0-128">Value</span><span class="sxs-lookup"><span data-stu-id="b55d0-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b55d0-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b55d0-129">Header</span></span><br/> | <dl> <span data-ttu-id="b55d0-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55d0-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55d0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b55d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55d0-132">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b55d0-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b55d0-133">**Información de D3DRECTPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="b55d0-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="b55d0-134">**Información de D3DTRIPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="b55d0-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




