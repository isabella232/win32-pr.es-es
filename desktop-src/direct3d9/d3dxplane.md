---
description: Describe un plano.
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estructura D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717557"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="2ddd8-103">Estructura D3DXPLANE (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2ddd8-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="2ddd8-104">Describe un plano.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ddd8-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="2ddd8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ddd8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ddd8-107">**un**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="2ddd8-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ddd8-109">Un coeficiente del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="2ddd8-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2ddd8-111">**b**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="2ddd8-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ddd8-113">El coeficiente b del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="2ddd8-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2ddd8-115">**c**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="2ddd8-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ddd8-117">Coeficiente c del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="2ddd8-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2ddd8-119">**d**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="2ddd8-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ddd8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2ddd8-121">Coeficiente d del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="2ddd8-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ddd8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ddd8-123">Remarks</span></span>

<span data-ttu-id="2ddd8-124">Los miembros de la estructura **D3DXPLANE** adoptan la forma de la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="2ddd8-125">Se ajustan a la ecuación de plano general **para que x**+ **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="2ddd8-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="2ddd8-126">Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXPLANE**](d3dxplane-extensions.md) que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="2ddd8-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddd8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddd8-127">Requirements</span></span>



| <span data-ttu-id="2ddd8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddd8-128">Requirement</span></span> | <span data-ttu-id="2ddd8-129">Value</span><span class="sxs-lookup"><span data-stu-id="2ddd8-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddd8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ddd8-130">Header</span></span><br/> | <dl> <span data-ttu-id="2ddd8-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddd8-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddd8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ddd8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddd8-133">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="2ddd8-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
