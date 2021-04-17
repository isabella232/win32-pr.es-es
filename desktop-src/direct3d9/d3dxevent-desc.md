---
description: Describe un evento de animación.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC estructura (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698251"
---
# <a name="d3dxevent_desc-structure"></a><span data-ttu-id="425b0-103">D3DXEVENT \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="425b0-103">D3DXEVENT\_DESC structure</span></span>

<span data-ttu-id="425b0-104">Describe un evento de animación.</span><span class="sxs-lookup"><span data-stu-id="425b0-104">Describes an animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="425b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="425b0-105">Syntax</span></span>


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a><span data-ttu-id="425b0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="425b0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="425b0-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="425b0-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-108">Tipo: **[ **D3DXEVENT \_ Type**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-108">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-109">Tipo de evento, tal y como se define en [**D3DXEVENT \_ Type**](./d3dxevent-type.md).</span><span class="sxs-lookup"><span data-stu-id="425b0-109">Event type, as defined in [**D3DXEVENT\_TYPE**](./d3dxevent-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="425b0-110">**Dar**</span><span class="sxs-lookup"><span data-stu-id="425b0-110">**Track**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-112">Identificador de la pista de eventos.</span><span class="sxs-lookup"><span data-stu-id="425b0-112">Event track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-113">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="425b0-113">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-115">Hora de inicio del evento en tiempo global.</span><span class="sxs-lookup"><span data-stu-id="425b0-115">Start time of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-116">**Duration**</span><span class="sxs-lookup"><span data-stu-id="425b0-116">**Duration**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-117">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-117">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-118">Duración del evento en tiempo global.</span><span class="sxs-lookup"><span data-stu-id="425b0-118">Duration of the event in global time.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-119">**Transición**</span><span class="sxs-lookup"><span data-stu-id="425b0-119">**Transition**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-120">Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-120">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-121">Estilo de transición del evento, tal y como se define en [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="425b0-121">Transition style of the event, as defined in [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="425b0-122">**Peso**</span><span class="sxs-lookup"><span data-stu-id="425b0-122">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-124">Ponderación del seguimiento del evento.</span><span class="sxs-lookup"><span data-stu-id="425b0-124">Track weight for the event.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-125">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="425b0-125">**Speed**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-127">Velocidad de seguimiento para el evento.</span><span class="sxs-lookup"><span data-stu-id="425b0-127">Track speed for the event.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-128">**Position**</span><span class="sxs-lookup"><span data-stu-id="425b0-128">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-129">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-129">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-130">Seguimiento de la posición del evento.</span><span class="sxs-lookup"><span data-stu-id="425b0-130">Track position for the event.</span></span>

</dd> <dt>

<span data-ttu-id="425b0-131">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="425b0-131">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="425b0-132">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="425b0-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="425b0-133">Habilitar marca.</span><span class="sxs-lookup"><span data-stu-id="425b0-133">Enable flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="425b0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="425b0-134">Requirements</span></span>



| <span data-ttu-id="425b0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="425b0-135">Requirement</span></span> | <span data-ttu-id="425b0-136">Value</span><span class="sxs-lookup"><span data-stu-id="425b0-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="425b0-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="425b0-137">Header</span></span><br/> | <dl> <span data-ttu-id="425b0-138"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="425b0-138"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="425b0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="425b0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425b0-140">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="425b0-140">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
