---
description: 'Estructura D3DXQUATERNION (D3dx9math.h): describe un cuaternión.'
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estructura D3DXQUATERNION (D3dx9math.h)
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115683"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="81add-103">Estructura D3DXQUATERNION (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="81add-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="81add-104">Describe un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="81add-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="81add-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81add-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="81add-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="81add-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81add-107">**x**</span><span class="sxs-lookup"><span data-stu-id="81add-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="81add-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81add-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81add-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="81add-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="81add-110">**y**</span><span class="sxs-lookup"><span data-stu-id="81add-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="81add-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81add-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81add-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="81add-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="81add-113">**z**</span><span class="sxs-lookup"><span data-stu-id="81add-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="81add-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81add-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81add-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="81add-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="81add-116">**w**</span><span class="sxs-lookup"><span data-stu-id="81add-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="81add-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81add-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="81add-118">W-component.</span><span class="sxs-lookup"><span data-stu-id="81add-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81add-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81add-119">Remarks</span></span>

<span data-ttu-id="81add-120">Los cuaterniones agregan un cuarto elemento a los valores x, y, z que definen un vector, lo que da lugar \[ \] a vectores 4D arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="81add-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="81add-121">Sin embargo, a continuación se muestra cómo cada elemento de un cuaternión de unidad se relaciona con una rotación de ángulo de eje (donde q representa un cuaternión de unidad (x, y, z, w), el eje se normaliza y theta es la rotación ccW deseada sobre el eje):</span><span class="sxs-lookup"><span data-stu-id="81add-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="81add-122">Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="81add-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="81add-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81add-123">Requirements</span></span>



| <span data-ttu-id="81add-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="81add-124">Requirement</span></span> | <span data-ttu-id="81add-125">Value</span><span class="sxs-lookup"><span data-stu-id="81add-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81add-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81add-126">Header</span></span><br/> | <dl> <span data-ttu-id="81add-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="81add-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81add-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81add-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81add-129">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="81add-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="81add-130">Vectores, vértices y cuaterniones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="81add-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
