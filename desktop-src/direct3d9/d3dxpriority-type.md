---
description: Define el tipo de prioridad al que se asigna una pista de animación.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Enumeración D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424376"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="23c93-103">\_Enumeración de tipo D3DXPRIORITY</span><span class="sxs-lookup"><span data-stu-id="23c93-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="23c93-104">Define el tipo de prioridad al que se asigna una pista de animación.</span><span class="sxs-lookup"><span data-stu-id="23c93-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c93-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23c93-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="23c93-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="23c93-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23c93-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ bajo**</span><span class="sxs-lookup"><span data-stu-id="23c93-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="23c93-108">La pista debe combinarse con todas las pistas de prioridad baja antes de que la mezcla de prioridad baja se mezcle con la mezcla de prioridad alta.</span><span class="sxs-lookup"><span data-stu-id="23c93-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="23c93-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ alto**</span><span class="sxs-lookup"><span data-stu-id="23c93-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="23c93-110">La pista debe combinarse con todas las pistas de prioridad alta antes de que la mezcla de prioridad alta se mezcle con la mezcla de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="23c93-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="23c93-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="23c93-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="23c93-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="23c93-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="23c93-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="23c93-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="23c93-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="23c93-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23c93-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23c93-115">Remarks</span></span>

<span data-ttu-id="23c93-116">Las pistas con la misma prioridad se mezclan juntas y los dos valores resultantes se combinan con el factor de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="23c93-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c93-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23c93-117">Requirements</span></span>



| <span data-ttu-id="23c93-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c93-118">Requirement</span></span> | <span data-ttu-id="23c93-119">Value</span><span class="sxs-lookup"><span data-stu-id="23c93-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23c93-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23c93-120">Header</span></span><br/> | <dl> <span data-ttu-id="23c93-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c93-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c93-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="23c93-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c93-123">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="23c93-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




