---
description: Describe un parámetro utilizado para un objeto de efecto.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280243"
---
# <a name="d3dxparameter_desc-structure"></a><span data-ttu-id="20c89-103">D3DXPARAMETER \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="20c89-103">D3DXPARAMETER\_DESC structure</span></span>

<span data-ttu-id="20c89-104">Describe un parámetro utilizado para un objeto de efecto.</span><span class="sxs-lookup"><span data-stu-id="20c89-104">Describes a parameter used for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20c89-105">Syntax</span></span>


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a><span data-ttu-id="20c89-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="20c89-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="20c89-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="20c89-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-109">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="20c89-109">Name of the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-110">**Semántica**</span><span class="sxs-lookup"><span data-stu-id="20c89-110">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-112">Significado semántico, también denominado uso.</span><span class="sxs-lookup"><span data-stu-id="20c89-112">Semantic meaning, also called the usage.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-113">**Clase**</span><span class="sxs-lookup"><span data-stu-id="20c89-113">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-114">Type: **[ **\_ clase D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-114">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-115">Clase de parámetro.</span><span class="sxs-lookup"><span data-stu-id="20c89-115">Parameter class.</span></span> <span data-ttu-id="20c89-116">Establézcalo en uno de los valores de la [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="20c89-116">Set this to one of the values in [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c89-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20c89-117">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-118">Tipo: **[ **D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-118">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-119">Tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="20c89-119">Parameter type.</span></span> <span data-ttu-id="20c89-120">Establézcalo en uno de los valores del [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="20c89-120">Set this to one of the values in [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c89-121">**Filas**</span><span class="sxs-lookup"><span data-stu-id="20c89-121">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-123">Número de filas de la matriz.</span><span class="sxs-lookup"><span data-stu-id="20c89-123">Number of rows in the array.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-124">**Columnas**</span><span class="sxs-lookup"><span data-stu-id="20c89-124">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-126">Número de columnas de la matriz.</span><span class="sxs-lookup"><span data-stu-id="20c89-126">Number of columns in the array.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-127">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="20c89-127">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-129">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="20c89-129">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-130">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="20c89-130">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-131">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-132">Número de anotaciones.</span><span class="sxs-lookup"><span data-stu-id="20c89-132">Number of annotations.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-133">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="20c89-133">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-135">Número de miembros de estructura.</span><span class="sxs-lookup"><span data-stu-id="20c89-135">Number of structure members.</span></span>

</dd> <dt>

<span data-ttu-id="20c89-136">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="20c89-136">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-137">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-138">Atributos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="20c89-138">Parameter attributes.</span></span> <span data-ttu-id="20c89-139">Vea [constantes de efecto](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="20c89-139">See [Effect Constants](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c89-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="20c89-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="20c89-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c89-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="20c89-142">Tamaño del parámetro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="20c89-142">The size of the parameter, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20c89-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20c89-143">Requirements</span></span>



| <span data-ttu-id="20c89-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="20c89-144">Requirement</span></span> | <span data-ttu-id="20c89-145">Value</span><span class="sxs-lookup"><span data-stu-id="20c89-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c89-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20c89-146">Header</span></span><br/> | <dl> <span data-ttu-id="20c89-147"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c89-147"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c89-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="20c89-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c89-149">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="20c89-149">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
