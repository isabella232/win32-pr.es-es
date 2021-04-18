---
description: Describe una pista de animación y especifica el peso, la velocidad y la posición de fusión de la pista en un momento dado.
ms.assetid: f1469b6f-861f-4b7d-a187-933092a5d257
title: D3DXTRACK_DESC estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRACK_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12f1604cf954bcdd6a2a898fec5410804112e498
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717727"
---
# <a name="d3dxtrack_desc-structure"></a><span data-ttu-id="3fe1b-103">D3DXTRACK \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="3fe1b-103">D3DXTRACK\_DESC structure</span></span>

<span data-ttu-id="3fe1b-104">Describe una pista de animación y especifica el peso, la velocidad y la posición de fusión de la pista en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-104">Describes an animation track and specifies blending weight, speed, and position for the track at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe1b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fe1b-105">Syntax</span></span>


```C++
typedef struct D3DXTRACK_DESC {
  D3DXPRIORITY_TYPE Priority;
  FLOAT             Weight;
  FLOAT             Speed;
  DOUBLE            Position;
  BOOL              Enable;
} D3DXTRACK_DESC, *LPD3DXTRACK_DESC;
```



## <a name="members"></a><span data-ttu-id="3fe1b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fe1b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3fe1b-107">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-107">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="3fe1b-108">Tipo: **[ **D3DXPRIORITY \_ Type**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-108">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3fe1b-109">Tipo de prioridad, tal y como se define en [**D3DXPRIORITY \_ Type**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="3fe1b-109">Priority type, as defined in [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="3fe1b-110">**Peso**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-110">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="3fe1b-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3fe1b-112">Valor de peso.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-112">Weight value.</span></span> <span data-ttu-id="3fe1b-113">El peso determina la proporción de esta pista para mezclar con otras pistas.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-113">The weight determines the proportion of this track to blend with other tracks.</span></span>

</dd> <dt>

<span data-ttu-id="3fe1b-114">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-114">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="3fe1b-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3fe1b-116">Valor de velocidad.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-116">Speed value.</span></span> <span data-ttu-id="3fe1b-117">Se utiliza de forma similar a un multiplicador para escalar el período de la pista.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-117">This is used similarly to a multiplier to scale the period of the track.</span></span>

</dd> <dt>

<span data-ttu-id="3fe1b-118">**Position**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-118">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="3fe1b-119">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-119">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3fe1b-120">Posición de hora de la pista, en el intervalo de tiempo local de su conjunto de animaciones actual.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-120">Time position of the track, in the local timeframe of its current animation set.</span></span>

</dd> <dt>

<span data-ttu-id="3fe1b-121">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-121">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="3fe1b-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3fe1b-123">Seguimiento habilitar/deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-123">Track enable/disable.</span></span> <span data-ttu-id="3fe1b-124">Para habilitarlo, establézcalo en **true**.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-124">To enable, set to **TRUE**.</span></span> <span data-ttu-id="3fe1b-125">Para deshabilitar, establezca en **false**.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-125">To disable, set to **FALSE**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fe1b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fe1b-126">Remarks</span></span>

<span data-ttu-id="3fe1b-127">Las pistas con la misma prioridad se mezclan juntas y los dos valores resultantes se combinan con el factor de mezcla de prioridad.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-127">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span> <span data-ttu-id="3fe1b-128">Una pista debe tener una animación establecida (almacenada por separado) asociada.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-128">A track must have an animation set (stored separately) associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe1b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fe1b-129">Requirements</span></span>



| <span data-ttu-id="3fe1b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe1b-130">Requirement</span></span> | <span data-ttu-id="3fe1b-131">Value</span><span class="sxs-lookup"><span data-stu-id="3fe1b-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe1b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fe1b-132">Header</span></span><br/> | <dl> <span data-ttu-id="3fe1b-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe1b-133"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fe1b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fe1b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe1b-135">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="3fe1b-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
