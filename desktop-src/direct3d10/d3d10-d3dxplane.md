---
description: 'Estructura D3DXPLANE (D3DX10Math.h): describe un plano.'
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estructura D3DXPLANE (D3DX10Math.h)
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
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103333"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="07cb9-103">Estructura D3DXPLANE (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="07cb9-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="07cb9-104">Describe un plano.</span><span class="sxs-lookup"><span data-stu-id="07cb9-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07cb9-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="07cb9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="07cb9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07cb9-107">**Un**</span><span class="sxs-lookup"><span data-stu-id="07cb9-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="07cb9-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07cb9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07cb9-109">Coeficiente del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="07cb9-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="07cb9-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07cb9-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07cb9-111">**b**</span><span class="sxs-lookup"><span data-stu-id="07cb9-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="07cb9-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07cb9-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07cb9-113">Coeficiente b del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="07cb9-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="07cb9-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07cb9-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07cb9-115">**c**</span><span class="sxs-lookup"><span data-stu-id="07cb9-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="07cb9-116">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07cb9-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07cb9-117">Coeficiente c del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="07cb9-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="07cb9-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07cb9-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07cb9-119">**d**</span><span class="sxs-lookup"><span data-stu-id="07cb9-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="07cb9-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07cb9-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07cb9-121">Coeficiente d del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="07cb9-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="07cb9-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07cb9-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07cb9-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07cb9-123">Remarks</span></span>

<span data-ttu-id="07cb9-124">Los miembros de la **estructura D3DXPLANE** toman la forma de la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="07cb9-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="07cb9-125">Encajan en la ecuación del plano general para que el eje + por + dw + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="07cb9-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cb9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07cb9-126">Requirements</span></span>



| <span data-ttu-id="07cb9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="07cb9-127">Requirement</span></span> | <span data-ttu-id="07cb9-128">Value</span><span class="sxs-lookup"><span data-stu-id="07cb9-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07cb9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07cb9-129">Header</span></span><br/> | <dl> <span data-ttu-id="07cb9-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="07cb9-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07cb9-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="07cb9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cb9-132">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="07cb9-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
