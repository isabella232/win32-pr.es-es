---
description: Una estructura auxiliar que contiene información de tipo de miembro.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: D3DXSHADER_TYPEINFO estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362542"
---
# <a name="d3dxshader_typeinfo-structure"></a><span data-ttu-id="2954e-103">D3DXSHADER \_ TYPEINFO (estructura)</span><span class="sxs-lookup"><span data-stu-id="2954e-103">D3DXSHADER\_TYPEINFO structure</span></span>

<span data-ttu-id="2954e-104">Una estructura auxiliar que contiene información de tipo de miembro.</span><span class="sxs-lookup"><span data-stu-id="2954e-104">A helper structure containing member type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2954e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2954e-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="2954e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2954e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2954e-107">**Clase**</span><span class="sxs-lookup"><span data-stu-id="2954e-107">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-109">Tipo de objeto de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2954e-109">Shader object type.</span></span> <span data-ttu-id="2954e-110">Vea [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="2954e-110">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="2954e-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2954e-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-112">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-112">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-113">Tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2954e-113">Data type.</span></span> <span data-ttu-id="2954e-114">Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="2954e-114">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="2954e-115">**Filas**</span><span class="sxs-lookup"><span data-stu-id="2954e-115">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-116">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-116">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-117">Número de filas de la matriz (matrices).</span><span class="sxs-lookup"><span data-stu-id="2954e-117">Number of matrix rows (matrices).</span></span>

</dd> <dt>

<span data-ttu-id="2954e-118">**Columnas**</span><span class="sxs-lookup"><span data-stu-id="2954e-118">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-119">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-119">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-120">Número de columnas (vectores y matrices).</span><span class="sxs-lookup"><span data-stu-id="2954e-120">Number of columns (vectors and matrices).</span></span>

</dd> <dt>

<span data-ttu-id="2954e-121">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="2954e-121">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-122">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-122">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-123">Dimensión de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2954e-123">Array dimension.</span></span>

</dd> <dt>

<span data-ttu-id="2954e-124">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="2954e-124">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-125">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-125">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-126">Número de miembros de estructura.</span><span class="sxs-lookup"><span data-stu-id="2954e-126">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="2954e-127">**StructMemberInfo**</span><span class="sxs-lookup"><span data-stu-id="2954e-127">**StructMemberInfo**</span></span>
</dt> <dd>

<span data-ttu-id="2954e-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2954e-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2954e-129">Matriz de información de miembros de estructura, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] .</span><span class="sxs-lookup"><span data-stu-id="2954e-129">Array of structure member information, D3DXSHADER\_STRUCTMEMBERINFO\[*StructMembers*\].</span></span> <span data-ttu-id="2954e-130">Vea [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2954e-130">See [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2954e-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2954e-131">Remarks</span></span>

<span data-ttu-id="2954e-132">La información de tipo forma parte de [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2954e-132">The type information is part of [**D3DXSHADER\_STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2954e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2954e-133">Requirements</span></span>



| <span data-ttu-id="2954e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2954e-134">Requirement</span></span> | <span data-ttu-id="2954e-135">Value</span><span class="sxs-lookup"><span data-stu-id="2954e-135">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2954e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2954e-136">Header</span></span><br/> | <dl> <span data-ttu-id="2954e-137"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2954e-137"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2954e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2954e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2954e-139">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="2954e-139">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="2954e-140">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="2954e-140">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
