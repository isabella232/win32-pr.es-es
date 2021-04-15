---
description: Define constantes que describen el modo de relleno.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Enumeración D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708127"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="14851-103">Enumeración D3DFILLMODE</span><span class="sxs-lookup"><span data-stu-id="14851-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="14851-104">Define constantes que describen el modo de relleno.</span><span class="sxs-lookup"><span data-stu-id="14851-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="14851-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14851-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="14851-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="14851-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="14851-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**\_Punto D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="14851-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="14851-108">Puntos de relleno.</span><span class="sxs-lookup"><span data-stu-id="14851-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="14851-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL \_ alambre**</span><span class="sxs-lookup"><span data-stu-id="14851-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="14851-110">Tramas de alambres.</span><span class="sxs-lookup"><span data-stu-id="14851-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="14851-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ Solid**</span><span class="sxs-lookup"><span data-stu-id="14851-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="14851-112">Sólidos de relleno.</span><span class="sxs-lookup"><span data-stu-id="14851-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="14851-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="14851-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="14851-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="14851-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="14851-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="14851-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="14851-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="14851-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14851-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14851-117">Remarks</span></span>

<span data-ttu-id="14851-118">El estado de representación de D3DRS FILLMODE usa los valores de este tipo enumerado \_ .</span><span class="sxs-lookup"><span data-stu-id="14851-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="14851-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14851-119">Requirements</span></span>



| <span data-ttu-id="14851-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14851-120">Requirement</span></span> | <span data-ttu-id="14851-121">Value</span><span class="sxs-lookup"><span data-stu-id="14851-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14851-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14851-122">Header</span></span><br/> | <dl> <span data-ttu-id="14851-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="14851-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14851-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="14851-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14851-125">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="14851-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="14851-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="14851-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
