---
description: 'Estructura D3DXQUATERNION (D3DX10Math.h): describe un cuaternión.'
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Estructura D3DXQUATERNION (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: dac880607cf482b409c407b43992747af4aa39a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103253"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="dbe01-103">Estructura D3DXQUATERNION (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="dbe01-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="dbe01-104">Describe un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="dbe01-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe01-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbe01-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="dbe01-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dbe01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbe01-107">**x**</span><span class="sxs-lookup"><span data-stu-id="dbe01-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="dbe01-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe01-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbe01-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="dbe01-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="dbe01-110">**y**</span><span class="sxs-lookup"><span data-stu-id="dbe01-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="dbe01-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe01-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbe01-112">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="dbe01-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="dbe01-113">**z**</span><span class="sxs-lookup"><span data-stu-id="dbe01-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="dbe01-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe01-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbe01-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="dbe01-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="dbe01-116">**w**</span><span class="sxs-lookup"><span data-stu-id="dbe01-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="dbe01-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe01-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbe01-118">W-component.</span><span class="sxs-lookup"><span data-stu-id="dbe01-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbe01-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbe01-119">Remarks</span></span>

<span data-ttu-id="dbe01-120">Los cuaterniones agregan un cuarto elemento a los valores x, y, z que definen un vector, lo que da lugar \[ \] a vectores 4D arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="dbe01-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="dbe01-121">Sin embargo, a continuación se muestra cómo cada elemento de un cuaternión de unidad se relaciona con una rotación de ángulo de eje (donde q representa un cuaternión de unidad (x, y, z, w), el eje se normaliza y theta es la rotación ccW deseada sobre el eje):</span><span class="sxs-lookup"><span data-stu-id="dbe01-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="dbe01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbe01-122">Requirements</span></span>



| <span data-ttu-id="dbe01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe01-123">Requirement</span></span> | <span data-ttu-id="dbe01-124">Value</span><span class="sxs-lookup"><span data-stu-id="dbe01-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe01-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbe01-125">Header</span></span><br/> | <dl> <span data-ttu-id="dbe01-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe01-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe01-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dbe01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe01-128">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="dbe01-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
