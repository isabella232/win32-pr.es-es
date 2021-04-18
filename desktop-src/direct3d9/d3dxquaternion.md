---
description: Describe un cuaternión.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estructura D3DXQUATERNION (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707831"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="07941-103">Estructura D3DXQUATERNION (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="07941-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="07941-104">Describe un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="07941-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="07941-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07941-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="07941-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="07941-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07941-107">**x**</span><span class="sxs-lookup"><span data-stu-id="07941-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="07941-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07941-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07941-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="07941-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="07941-110">**y**</span><span class="sxs-lookup"><span data-stu-id="07941-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="07941-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07941-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07941-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="07941-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="07941-113">**z**</span><span class="sxs-lookup"><span data-stu-id="07941-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="07941-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07941-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07941-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="07941-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="07941-116">**w**</span><span class="sxs-lookup"><span data-stu-id="07941-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="07941-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07941-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07941-118">Componente w-.</span><span class="sxs-lookup"><span data-stu-id="07941-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07941-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07941-119">Remarks</span></span>

<span data-ttu-id="07941-120">Los cuaterniones agregan un cuarto elemento a los \[ valores x, y, z \] que definen un vector, lo que da lugar a vectores 4D arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="07941-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="07941-121">Sin embargo, a continuación se muestra cómo cada elemento de un cuaternión de unidad se relaciona con una rotación de ángulo de eje (donde q representa un cuaternión de unidad (x, y, z, w), se normaliza el eje y Theta es la rotación del CCW deseada sobre el eje):</span><span class="sxs-lookup"><span data-stu-id="07941-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="07941-122">Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="07941-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="07941-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07941-123">Requirements</span></span>



| <span data-ttu-id="07941-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="07941-124">Requirement</span></span> | <span data-ttu-id="07941-125">Value</span><span class="sxs-lookup"><span data-stu-id="07941-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07941-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07941-126">Header</span></span><br/> | <dl> <span data-ttu-id="07941-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="07941-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07941-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="07941-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07941-129">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="07941-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="07941-130">Vectores, vértices y cuaterniones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07941-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
