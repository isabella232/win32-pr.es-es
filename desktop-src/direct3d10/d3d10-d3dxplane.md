---
description: Describe un plano.
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: Estructura D3DXPLANE (D3DX10Math. h)
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
ms.openlocfilehash: 9949aec16e90a53e01e536255c20f442052bb98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362730"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="78a24-103">Estructura D3DXPLANE (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="78a24-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="78a24-104">Describe un plano.</span><span class="sxs-lookup"><span data-stu-id="78a24-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78a24-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="78a24-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="78a24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78a24-107">**un**</span><span class="sxs-lookup"><span data-stu-id="78a24-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="78a24-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78a24-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78a24-109">Un coeficiente del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="78a24-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="78a24-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="78a24-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78a24-111">**b**</span><span class="sxs-lookup"><span data-stu-id="78a24-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="78a24-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78a24-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78a24-113">El coeficiente b del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="78a24-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="78a24-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="78a24-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78a24-115">**c**</span><span class="sxs-lookup"><span data-stu-id="78a24-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="78a24-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78a24-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78a24-117">Coeficiente c del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="78a24-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="78a24-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="78a24-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="78a24-119">**d**</span><span class="sxs-lookup"><span data-stu-id="78a24-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="78a24-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78a24-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="78a24-121">Coeficiente d del plano de recorte en la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="78a24-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="78a24-122">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="78a24-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78a24-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78a24-123">Remarks</span></span>

<span data-ttu-id="78a24-124">Los miembros de la estructura **D3DXPLANE** adoptan la forma de la ecuación de plano general.</span><span class="sxs-lookup"><span data-stu-id="78a24-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="78a24-125">Se ajustan a la ecuación de plano general para que AX + por + cz + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="78a24-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a24-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a24-126">Requirements</span></span>



| <span data-ttu-id="78a24-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a24-127">Requirement</span></span> | <span data-ttu-id="78a24-128">Value</span><span class="sxs-lookup"><span data-stu-id="78a24-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78a24-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78a24-129">Header</span></span><br/> | <dl> <span data-ttu-id="78a24-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="78a24-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a24-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="78a24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a24-132">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="78a24-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
