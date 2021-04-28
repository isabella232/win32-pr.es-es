---
description: 'Estructura D3DXPLANE (D3dx9math.h): describe un plano.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Estructura D3DXPLANE (D3dx9math.h)
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
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115723"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="da07a-103">Estructura D3DXPLANE (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="da07a-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="da07a-104">Describe un plano.</span><span class="sxs-lookup"><span data-stu-id="da07a-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="da07a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da07a-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="da07a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="da07a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="da07a-107">**Un**</span><span class="sxs-lookup"><span data-stu-id="da07a-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="da07a-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da07a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da07a-109">Coeficiente del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="da07a-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="da07a-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="da07a-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da07a-111">**b**</span><span class="sxs-lookup"><span data-stu-id="da07a-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="da07a-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da07a-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da07a-113">Coeficiente b del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="da07a-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="da07a-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="da07a-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da07a-115">**c**</span><span class="sxs-lookup"><span data-stu-id="da07a-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="da07a-116">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da07a-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da07a-117">Coeficiente c del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="da07a-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="da07a-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="da07a-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da07a-119">**d**</span><span class="sxs-lookup"><span data-stu-id="da07a-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="da07a-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da07a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da07a-121">Coeficiente d del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="da07a-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="da07a-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="da07a-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da07a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da07a-123">Remarks</span></span>

<span data-ttu-id="da07a-124">Los miembros de la **estructura D3DXPLANE** toman la forma de la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="da07a-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="da07a-125">Encajan en la ecuación de plano general para que **x**+ **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="da07a-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="da07a-126">Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXPLANE**](d3dxplane-extensions.md) que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="da07a-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="da07a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da07a-127">Requirements</span></span>



| <span data-ttu-id="da07a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="da07a-128">Requirement</span></span> | <span data-ttu-id="da07a-129">Value</span><span class="sxs-lookup"><span data-stu-id="da07a-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da07a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da07a-130">Header</span></span><br/> | <dl> <span data-ttu-id="da07a-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="da07a-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da07a-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da07a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da07a-133">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="da07a-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
