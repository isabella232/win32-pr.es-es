---
description: Define el diseño de los datos de vértices. Cada vértice puede contener uno o más tipos de datos, y cada tipo de datos lo describe un elemento de vértice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Estructura D3DVERTEXELEMENT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e6c5e9508185124673ca7464b31d741cdf8035c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670243"
---
# <a name="d3dvertexelement9-structure"></a><span data-ttu-id="00e2f-104">Estructura D3DVERTEXELEMENT9</span><span class="sxs-lookup"><span data-stu-id="00e2f-104">D3DVERTEXELEMENT9 structure</span></span>

<span data-ttu-id="00e2f-105">Define el diseño de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="00e2f-105">Defines the vertex data layout.</span></span> <span data-ttu-id="00e2f-106">Cada vértice puede contener uno o más tipos de datos, y cada tipo de datos lo describe un elemento de vértice.</span><span class="sxs-lookup"><span data-stu-id="00e2f-106">Each vertex can contain one or more data types, and each data type is described by a vertex element.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e2f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00e2f-107">Syntax</span></span>


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a><span data-ttu-id="00e2f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="00e2f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00e2f-109">**Stream**</span><span class="sxs-lookup"><span data-stu-id="00e2f-109">**Stream**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-111">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="00e2f-111">Stream number.</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-112">**Offset**</span><span class="sxs-lookup"><span data-stu-id="00e2f-112">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-113">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-113">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-114">Desplazamiento desde el principio de los datos del vértice hasta los datos asociados con el tipo de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="00e2f-114">Offset from the beginning of the vertex data to the data associated with the particular data type.</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="00e2f-115">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-116">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-116">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-117">El tipo de datos, especificado como [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="00e2f-117">The data type, specified as a [**D3DDECLTYPE**](./d3ddecltype.md).</span></span> <span data-ttu-id="00e2f-118">Uno de varios tipos predefinidos que definen el tamaño de los datos.</span><span class="sxs-lookup"><span data-stu-id="00e2f-118">One of several predefined types that define the data size.</span></span> <span data-ttu-id="00e2f-119">Algunos métodos tienen un tipo implícito.</span><span class="sxs-lookup"><span data-stu-id="00e2f-119">Some methods have an implied type.</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-120">**Método**</span><span class="sxs-lookup"><span data-stu-id="00e2f-120">**Method**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-121">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-121">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-122">El método especifica el procesamiento de del teselador, que determina cómo del teselador interpreta (o opera) los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="00e2f-122">The method specifies the tessellator processing, which determines how the tessellator interprets (or operates on) the vertex data.</span></span> <span data-ttu-id="00e2f-123">Para obtener más información, vea [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="00e2f-123">For more information, see [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-124">**Uso**</span><span class="sxs-lookup"><span data-stu-id="00e2f-124">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-126">Define para qué se usarán los datos; es decir, la interoperabilidad entre los diseños de datos de vértice y los sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="00e2f-126">Defines what the data will be used for; that is, the interoperability between vertex data layouts and vertex shaders.</span></span> <span data-ttu-id="00e2f-127">Cada uso actúa para enlazar una declaración de vértice a un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="00e2f-127">Each usage acts to bind a vertex declaration to a vertex shader.</span></span> <span data-ttu-id="00e2f-128">En algunos casos, tienen una interpretación especial.</span><span class="sxs-lookup"><span data-stu-id="00e2f-128">In some cases, they have a special interpretation.</span></span> <span data-ttu-id="00e2f-129">Por ejemplo, un elemento que especifica \_ la posición D3DDECLUSAGE normal o D3DDECLUSAGE \_ se usa en la del teselador N-patch para configurar la teselación.</span><span class="sxs-lookup"><span data-stu-id="00e2f-129">For example, an element that specifies D3DDECLUSAGE\_NORMAL or D3DDECLUSAGE\_POSITION is used by the N-patch tessellator to set up tessellation.</span></span> <span data-ttu-id="00e2f-130">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md) para obtener una lista de la semántica disponible.</span><span class="sxs-lookup"><span data-stu-id="00e2f-130">See [**D3DDECLUSAGE**](./d3ddeclusage.md) for a list of the available semantics.</span></span> <span data-ttu-id="00e2f-131">D3DDECLUSAGE \_ TEXCOORD se puede usar para campos definidos por el usuario (que no tienen definido un uso existente).</span><span class="sxs-lookup"><span data-stu-id="00e2f-131">D3DDECLUSAGE\_TEXCOORD can be used for user-defined fields (which don't have an existing usage defined).</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-132">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="00e2f-132">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-133">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00e2f-133">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00e2f-134">Modifica los datos de uso para permitir al usuario especificar varios tipos de uso.</span><span class="sxs-lookup"><span data-stu-id="00e2f-134">Modifies the usage data to allow the user to specify multiple usage types.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00e2f-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00e2f-135">Remarks</span></span>

<span data-ttu-id="00e2f-136">Los datos de vértice se definen mediante una matriz de estructuras **D3DVERTEXELEMENT9** .</span><span class="sxs-lookup"><span data-stu-id="00e2f-136">Vertex data is defined using an array of **D3DVERTEXELEMENT9** structures.</span></span> <span data-ttu-id="00e2f-137">Use [**D3DDECL \_ End**](d3ddecl-end.md) para declarar el último elemento de la declaración.</span><span class="sxs-lookup"><span data-stu-id="00e2f-137">Use [**D3DDECL\_END**](d3ddecl-end.md) to declare the last element in the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e2f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00e2f-138">Requirements</span></span>



| <span data-ttu-id="00e2f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="00e2f-139">Requirement</span></span> | <span data-ttu-id="00e2f-140">Value</span><span class="sxs-lookup"><span data-stu-id="00e2f-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00e2f-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00e2f-141">Header</span></span><br/> | <dl> <span data-ttu-id="00e2f-142"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="00e2f-142"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e2f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="00e2f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e2f-144">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="00e2f-144">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="00e2f-145">Declaración de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="00e2f-145">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
