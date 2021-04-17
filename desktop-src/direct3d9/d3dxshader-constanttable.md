---
description: Estructura de aplicación auxiliar para administrar una tabla de constantes de sombreador. Esto también se puede hacer mediante ID3DXConstantTable.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717740"
---
# <a name="d3dxshader_constanttable-structure"></a><span data-ttu-id="7f06d-104">D3DXSHADER \_ estructura CONSTANTTABLE</span><span class="sxs-lookup"><span data-stu-id="7f06d-104">D3DXSHADER\_CONSTANTTABLE structure</span></span>

<span data-ttu-id="7f06d-105">Estructura de aplicación auxiliar para administrar una tabla de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f06d-105">Helper structure for managing a shader constant table.</span></span> <span data-ttu-id="7f06d-106">Esto también se puede hacer mediante [**ID3DXConstantTable**](id3dxconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="7f06d-106">This can also be done using [**ID3DXConstantTable**](id3dxconstanttable.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f06d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f06d-107">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a><span data-ttu-id="7f06d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f06d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f06d-109">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="7f06d-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-111">Tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="7f06d-111">Size of the structure.</span></span> <span data-ttu-id="7f06d-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7f06d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-113">**Creador**</span><span class="sxs-lookup"><span data-stu-id="7f06d-113">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-115">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el nombre del creador.</span><span class="sxs-lookup"><span data-stu-id="7f06d-115">Offset from the beginning of this structure, in bytes, to the string that contains the name of the creator.</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-116">**Versión**</span><span class="sxs-lookup"><span data-stu-id="7f06d-116">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-118">Versión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f06d-118">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-119">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="7f06d-119">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-121">Número de constantes.</span><span class="sxs-lookup"><span data-stu-id="7f06d-121">Number of constants.</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-122">**ConstantInfo**</span><span class="sxs-lookup"><span data-stu-id="7f06d-122">**ConstantInfo**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-124">Matriz de información constante, constantes de D3DXSHADER \_ CONSTANTINFO \[  \] .</span><span class="sxs-lookup"><span data-stu-id="7f06d-124">Array of constant information, D3DXSHADER\_CONSTANTINFO\[*Constants*\].</span></span> <span data-ttu-id="7f06d-125">Vea [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).</span><span class="sxs-lookup"><span data-stu-id="7f06d-125">See [**D3DXSHADER\_CONSTANTINFO**](d3dxshader-constantinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-126">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="7f06d-126">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-128">[D3DXSHADER](d3dxshader-flags.md) marca las marcas que se usan para compilar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f06d-128">The [D3DXSHADER Flags](d3dxshader-flags.md) flags used to compile the shader.</span></span>

</dd> <dt>

<span data-ttu-id="7f06d-129">**Target**</span><span class="sxs-lookup"><span data-stu-id="7f06d-129">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="7f06d-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f06d-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7f06d-131">Desplazamiento en la cadena que contiene el destino.</span><span class="sxs-lookup"><span data-stu-id="7f06d-131">Offset into the string that contains the target.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f06d-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f06d-132">Remarks</span></span>

<span data-ttu-id="7f06d-133">La información de constantes del sombreador se incluye en una tabla de comentarios delimitada por tabuladores.</span><span class="sxs-lookup"><span data-stu-id="7f06d-133">Shader constant information is included in a tab-delimited table of comments.</span></span> <span data-ttu-id="7f06d-134">Todos los desplazamientos se miden en bytes desde el principio de la estructura.</span><span class="sxs-lookup"><span data-stu-id="7f06d-134">All offsets are measured in bytes from the beginning of the structure.</span></span> <span data-ttu-id="7f06d-135">Las entradas de la tabla Constant se ordenan por creador en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="7f06d-135">Entries in the constant table are sorted by Creator in ascending order.</span></span>

<span data-ttu-id="7f06d-136">Una tabla de constantes de sombreador se puede administrar con las interfaces [**ID3DXConstantTable**](id3dxconstanttable.md) .</span><span class="sxs-lookup"><span data-stu-id="7f06d-136">A shader constant table can be managed with the [**ID3DXConstantTable**](id3dxconstanttable.md) interfaces.</span></span> <span data-ttu-id="7f06d-137">Como alternativa, puede administrar la tabla de constantes con **D3DXSHADER \_ CONSTANTTABLE**.</span><span class="sxs-lookup"><span data-stu-id="7f06d-137">Alternatively, you can manage the constant table with **D3DXSHADER\_CONSTANTTABLE**.</span></span>

<span data-ttu-id="7f06d-138">Este miembro de tamaño se inicializa a menudo con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7f06d-138">This size member is often initialized using the following:</span></span>


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a><span data-ttu-id="7f06d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f06d-139">Requirements</span></span>



| <span data-ttu-id="7f06d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f06d-140">Requirement</span></span> | <span data-ttu-id="7f06d-141">Value</span><span class="sxs-lookup"><span data-stu-id="7f06d-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f06d-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f06d-142">Header</span></span><br/> | <dl> <span data-ttu-id="7f06d-143"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f06d-143"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f06d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f06d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f06d-145">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="7f06d-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7f06d-146">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="7f06d-146">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
