---
description: Describe los valores de color.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estructura D3DXCOLOR (D3dx9math. h)
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
ms.openlocfilehash: c7e5c1ac12341ccf6272714511959ee9a131ba4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678817"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="c785e-103">Estructura D3DXCOLOR (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c785e-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="c785e-104">Describe los valores de color.</span><span class="sxs-lookup"><span data-stu-id="c785e-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c785e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c785e-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="c785e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c785e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c785e-107">**r**</span><span class="sxs-lookup"><span data-stu-id="c785e-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="c785e-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c785e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c785e-109">Componente rojo del color.</span><span class="sxs-lookup"><span data-stu-id="c785e-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="c785e-110">**g**</span><span class="sxs-lookup"><span data-stu-id="c785e-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="c785e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c785e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c785e-112">Componente verde del color.</span><span class="sxs-lookup"><span data-stu-id="c785e-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="c785e-113">**b**</span><span class="sxs-lookup"><span data-stu-id="c785e-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="c785e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c785e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c785e-115">Componente azul del color.</span><span class="sxs-lookup"><span data-stu-id="c785e-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="c785e-116">**un**</span><span class="sxs-lookup"><span data-stu-id="c785e-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="c785e-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c785e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c785e-118">Componente alfa del color.</span><span class="sxs-lookup"><span data-stu-id="c785e-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c785e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c785e-119">Remarks</span></span>

<span data-ttu-id="c785e-120">Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXCOLOR**](d3dxcolor-extensions.md), que implementan constructores sobrecargados, así como operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="c785e-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="c785e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c785e-121">Requirements</span></span>



| <span data-ttu-id="c785e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c785e-122">Requirement</span></span> | <span data-ttu-id="c785e-123">Value</span><span class="sxs-lookup"><span data-stu-id="c785e-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c785e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c785e-124">Header</span></span><br/> | <dl> <span data-ttu-id="c785e-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c785e-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c785e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c785e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c785e-127">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="c785e-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
