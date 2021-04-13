---
description: Describe el tipo de eventos que se pueden codificar mediante el controlador de animación.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Enumeración D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362575"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="239cc-103">\_Enumeración de tipo D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="239cc-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="239cc-104">Describe el tipo de eventos que se pueden codificar mediante el controlador de animación.</span><span class="sxs-lookup"><span data-stu-id="239cc-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="239cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="239cc-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="239cc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="239cc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="239cc-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ TRACKSPEED**</span><span class="sxs-lookup"><span data-stu-id="239cc-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-108">Velocidad de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="239cc-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="239cc-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ TRACKWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="239cc-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-110">Seguimiento de peso.</span><span class="sxs-lookup"><span data-stu-id="239cc-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="239cc-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="239cc-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-112">Seguimiento de la posición.</span><span class="sxs-lookup"><span data-stu-id="239cc-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="239cc-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ TRACKENABLE**</span><span class="sxs-lookup"><span data-stu-id="239cc-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-114">Habilitar marca.</span><span class="sxs-lookup"><span data-stu-id="239cc-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="239cc-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ PRIORITYBLEND**</span><span class="sxs-lookup"><span data-stu-id="239cc-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-116">Valor de Blend de prioridad.</span><span class="sxs-lookup"><span data-stu-id="239cc-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="239cc-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="239cc-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="239cc-118">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="239cc-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="239cc-119">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="239cc-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="239cc-120">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="239cc-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="239cc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="239cc-121">Requirements</span></span>



| <span data-ttu-id="239cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="239cc-122">Requirement</span></span> | <span data-ttu-id="239cc-123">Value</span><span class="sxs-lookup"><span data-stu-id="239cc-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="239cc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="239cc-124">Header</span></span><br/> | <dl> <span data-ttu-id="239cc-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="239cc-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239cc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="239cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239cc-127">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="239cc-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




