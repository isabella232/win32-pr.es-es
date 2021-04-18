---
description: Almacena una entrada de tabla de atributos.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: D3DX10_ATTRIBUTE_RANGE estructura (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718434"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="63d7a-103">Estructura del intervalo del \_ atributo D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="63d7a-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="63d7a-104">Almacena una entrada de tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="63d7a-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63d7a-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="63d7a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="63d7a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="63d7a-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="63d7a-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="63d7a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63d7a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63d7a-109">Identificador de la tabla de atributos.</span><span class="sxs-lookup"><span data-stu-id="63d7a-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="63d7a-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="63d7a-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="63d7a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63d7a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63d7a-112">Superficie inicial.</span><span class="sxs-lookup"><span data-stu-id="63d7a-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="63d7a-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="63d7a-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="63d7a-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63d7a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63d7a-115">Recuento de caras.</span><span class="sxs-lookup"><span data-stu-id="63d7a-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="63d7a-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="63d7a-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="63d7a-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63d7a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63d7a-118">Vértice inicial.</span><span class="sxs-lookup"><span data-stu-id="63d7a-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="63d7a-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="63d7a-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="63d7a-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63d7a-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63d7a-121">Recuento de vértices.</span><span class="sxs-lookup"><span data-stu-id="63d7a-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63d7a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63d7a-122">Remarks</span></span>

<span data-ttu-id="63d7a-123">Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc.</span><span class="sxs-lookup"><span data-stu-id="63d7a-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="63d7a-124">Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (AttribId) al dibujar el marco.</span><span class="sxs-lookup"><span data-stu-id="63d7a-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="63d7a-125">El \_ tipo de intervalo de atributo LPD3DX \_ se define como un puntero a la estructura de intervalo de atributos de D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="63d7a-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="63d7a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63d7a-126">Requirements</span></span>



| <span data-ttu-id="63d7a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="63d7a-127">Requirement</span></span> | <span data-ttu-id="63d7a-128">Value</span><span class="sxs-lookup"><span data-stu-id="63d7a-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="63d7a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63d7a-129">Header</span></span><br/> | <dl> <span data-ttu-id="63d7a-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="63d7a-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d7a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="63d7a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d7a-132">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="63d7a-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
