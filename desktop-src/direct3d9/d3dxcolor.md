---
description: 'Estructura D3DXCOLOR (D3dx9math.h): describe los valores de color.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estructura D3DXCOLOR (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115933"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="e612b-103">Estructura D3DXCOLOR (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e612b-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="e612b-104">Describe los valores de color.</span><span class="sxs-lookup"><span data-stu-id="e612b-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e612b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e612b-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="e612b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e612b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e612b-107">**r**</span><span class="sxs-lookup"><span data-stu-id="e612b-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="e612b-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e612b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e612b-109">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="e612b-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="e612b-110">**g**</span><span class="sxs-lookup"><span data-stu-id="e612b-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="e612b-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e612b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e612b-112">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="e612b-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="e612b-113">**b**</span><span class="sxs-lookup"><span data-stu-id="e612b-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="e612b-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e612b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e612b-115">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="e612b-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="e612b-116">**Un**</span><span class="sxs-lookup"><span data-stu-id="e612b-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="e612b-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e612b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e612b-118">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="e612b-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e612b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e612b-119">Remarks</span></span>

<span data-ttu-id="e612b-120">Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXCOLOR**](d3dxcolor-extensions.md), que implementan constructores sobrecargados, así como operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="e612b-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="e612b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e612b-121">Requirements</span></span>



| <span data-ttu-id="e612b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e612b-122">Requirement</span></span> | <span data-ttu-id="e612b-123">Value</span><span class="sxs-lookup"><span data-stu-id="e612b-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e612b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e612b-124">Header</span></span><br/> | <dl> <span data-ttu-id="e612b-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e612b-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e612b-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e612b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e612b-127">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="e612b-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
