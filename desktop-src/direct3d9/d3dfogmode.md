---
description: Define constantes que describen el modo de niebla.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumeración D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362647"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="bc198-103">Enumeración D3DFOGMODE</span><span class="sxs-lookup"><span data-stu-id="bc198-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="bc198-104">Define constantes que describen el modo de niebla.</span><span class="sxs-lookup"><span data-stu-id="bc198-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc198-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc198-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="bc198-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc198-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc198-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="bc198-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="bc198-108">Ningún efecto de niebla.</span><span class="sxs-lookup"><span data-stu-id="bc198-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="bc198-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**</span><span class="sxs-lookup"><span data-stu-id="bc198-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="bc198-110">El efecto de niebla se intensifica exponencialmente, de acuerdo con la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="bc198-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![fórmula de intensidad del efecto niebla](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="bc198-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**</span><span class="sxs-lookup"><span data-stu-id="bc198-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="bc198-113">El efecto de niebla intensifica exponencialmente con el cuadrado de la distancia, de acuerdo con la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="bc198-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![fórmula de intensidad del efecto niebla basada en el cuadrado de la distancia](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="bc198-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**\_Lineal D3DFOG**</span><span class="sxs-lookup"><span data-stu-id="bc198-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="bc198-116">El efecto de niebla intensifica linealmente entre los puntos inicial y final, de acuerdo con la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="bc198-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![fórmula de intensidad del efecto niebla basada en los puntos inicial y final](images/fogliner.png)

<span data-ttu-id="bc198-118">Este es el único modo de niebla compatible actualmente.</span><span class="sxs-lookup"><span data-stu-id="bc198-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="bc198-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bc198-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bc198-120">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="bc198-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bc198-121">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bc198-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bc198-122">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc198-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc198-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc198-123">Remarks</span></span>

<span data-ttu-id="bc198-124">Los valores de este tipo enumerado se usan en los \_ Estados de representación D3DRS FOGTABLEMODE y D3DRS \_ FOGVERTEXMODE.</span><span class="sxs-lookup"><span data-stu-id="bc198-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="bc198-125">La niebla se puede considerar una medida de visibilidad: cuanto menor sea el valor de niebla producido por una ecuación de niebla, menos visible será un objeto.</span><span class="sxs-lookup"><span data-stu-id="bc198-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc198-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc198-126">Requirements</span></span>



| <span data-ttu-id="bc198-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc198-127">Requirement</span></span> | <span data-ttu-id="bc198-128">Value</span><span class="sxs-lookup"><span data-stu-id="bc198-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc198-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc198-129">Header</span></span><br/> | <dl> <span data-ttu-id="bc198-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc198-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc198-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc198-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc198-132">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc198-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="bc198-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="bc198-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
