---
description: Descripción de una constante en una tabla de constantes.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718446"
---
# <a name="d3dxconstant_desc-structure"></a><span data-ttu-id="b4a88-103">D3DXCONSTANT \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="b4a88-103">D3DXCONSTANT\_DESC structure</span></span>

<span data-ttu-id="b4a88-104">Descripción de una constante en una tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="b4a88-104">A description of a constant in a constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a88-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4a88-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a><span data-ttu-id="b4a88-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4a88-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4a88-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b4a88-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-109">Nombre de la constante.</span><span class="sxs-lookup"><span data-stu-id="b4a88-109">Name of the constant.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-110">**RegisterSet**</span><span class="sxs-lookup"><span data-stu-id="b4a88-110">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-111">Tipo: **[ **D3DXREGISTER \_ set**](./d3dxregister-set.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-111">Type: **[**D3DXREGISTER\_SET**](./d3dxregister-set.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-112">Tipo de datos constante.</span><span class="sxs-lookup"><span data-stu-id="b4a88-112">Constant data type.</span></span> <span data-ttu-id="b4a88-113">Vea [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="b4a88-113">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-114">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="b4a88-114">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-116">Índice de base cero de la constante de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b4a88-116">Zero-based index of the constant in the table.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-117">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="b4a88-117">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-119">Número de registros que contienen datos.</span><span class="sxs-lookup"><span data-stu-id="b4a88-119">Number of registers that contain data.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-120">**Clase**</span><span class="sxs-lookup"><span data-stu-id="b4a88-120">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-121">Type: **[ **\_ clase D3DXPARAMETER**](./d3dxparameter-class.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-121">Type: **[**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-122">Clase de parámetro.</span><span class="sxs-lookup"><span data-stu-id="b4a88-122">Parameter class.</span></span> <span data-ttu-id="b4a88-123">Vea [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).</span><span class="sxs-lookup"><span data-stu-id="b4a88-123">See [**D3DXPARAMETER\_CLASS**](./d3dxparameter-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4a88-124">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-125">Tipo: **[ **D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-125">Type: **[**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-126">Tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="b4a88-126">Parameter type.</span></span> <span data-ttu-id="b4a88-127">Consulte [**\_ tipo de D3DXPARAMETER**](./d3dxparameter-type.md).</span><span class="sxs-lookup"><span data-stu-id="b4a88-127">See [**D3DXPARAMETER\_TYPE**](./d3dxparameter-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-128">**Filas**</span><span class="sxs-lookup"><span data-stu-id="b4a88-128">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-130">Número de filas.</span><span class="sxs-lookup"><span data-stu-id="b4a88-130">Number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-131">**Columnas**</span><span class="sxs-lookup"><span data-stu-id="b4a88-131">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-133">Número de columnas.</span><span class="sxs-lookup"><span data-stu-id="b4a88-133">Number of columns.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-134">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="b4a88-134">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-136">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="b4a88-136">Number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-137">**StructMembers**</span><span class="sxs-lookup"><span data-stu-id="b4a88-137">**StructMembers**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-138">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-139">Número de subparámetros de miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="b4a88-139">Number of structure member sub-parameters.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-140">**Bytes**</span><span class="sxs-lookup"><span data-stu-id="b4a88-140">**Bytes**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-141">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-141">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-142">Tamaño de los datos en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="b4a88-142">Data size in number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b4a88-143">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="b4a88-143">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="b4a88-144">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a88-144">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b4a88-145">Puntero al valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b4a88-145">Pointer to the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4a88-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a88-146">Requirements</span></span>



| <span data-ttu-id="b4a88-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a88-147">Requirement</span></span> | <span data-ttu-id="b4a88-148">Value</span><span class="sxs-lookup"><span data-stu-id="b4a88-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a88-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4a88-149">Header</span></span><br/> | <dl> <span data-ttu-id="b4a88-150"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a88-150"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a88-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4a88-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a88-152">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="b4a88-152">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="b4a88-153">**D3DXCONSTANTTABLE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="b4a88-153">**D3DXCONSTANTTABLE\_DESC**</span></span>](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
