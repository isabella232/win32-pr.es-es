---
description: Define constantes que describen los modos de sombreado admitidos.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumeración D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362507"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="ed8b4-103">Enumeración D3DSHADEMODE</span><span class="sxs-lookup"><span data-stu-id="ed8b4-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="ed8b4-104">Define constantes que describen los modos de sombreado admitidos.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed8b4-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="ed8b4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ed8b4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed8b4-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ plano**</span><span class="sxs-lookup"><span data-stu-id="ed8b4-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="ed8b4-108">Modo de sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-108">Flat shading mode.</span></span> <span data-ttu-id="ed8b4-109">El color y el componente especular del primer vértice del triángulo se usan para determinar el color y el componente especular de la superficie.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="ed8b4-110">Estos colores permanecen constantes a lo largo del triángulo; es decir, no se interpolan.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="ed8b4-111">El alfa especular está interpolado.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="ed8b4-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed8b4-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**</span><span class="sxs-lookup"><span data-stu-id="ed8b4-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="ed8b4-114">Modo de sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-114">Gouraud shading mode.</span></span> <span data-ttu-id="ed8b4-115">Los componentes de color y especular de la superficie se determinan mediante una interpolación lineal entre los tres vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ed8b4-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**</span><span class="sxs-lookup"><span data-stu-id="ed8b4-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="ed8b4-117">No se admite.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed8b4-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ed8b4-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ed8b4-119">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ed8b4-120">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ed8b4-121">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed8b4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed8b4-122">Remarks</span></span>

<span data-ttu-id="ed8b4-123">El primer vértice de un triángulo para el modo de sombreado plano se define de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="ed8b4-124">En el caso de una lista de triángulos, el primer vértice del triángulo i es i \* 3.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="ed8b4-125">En el caso de una franja de triángulo, el primer vértice del triángulo i es el vértice i.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="ed8b4-126">En el caso de un ventilador de triángulo, el primer vértice del triángulo i es el vértice i + 1.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="ed8b4-127">Los miembros de este tipo enumerado definen el valores para el estado de representación de D3DRS \_ SHADEMODE.</span><span class="sxs-lookup"><span data-stu-id="ed8b4-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8b4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8b4-128">Requirements</span></span>



| <span data-ttu-id="ed8b4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8b4-129">Requirement</span></span> | <span data-ttu-id="ed8b4-130">Value</span><span class="sxs-lookup"><span data-stu-id="ed8b4-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8b4-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed8b4-131">Header</span></span><br/> | <dl> <span data-ttu-id="ed8b4-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed8b4-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8b4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed8b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8b4-134">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ed8b4-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ed8b4-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="ed8b4-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
