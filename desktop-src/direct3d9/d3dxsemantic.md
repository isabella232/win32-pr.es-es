---
description: La semántica asigna un parámetro a los registros del sombreador de vértices o píxeles. También pueden ser cadenas descriptivas opcionales adjuntas a parámetros que no son de registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Estructura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424372"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="e0802-104">Estructura D3DXSEMANTIC</span><span class="sxs-lookup"><span data-stu-id="e0802-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="e0802-105">La semántica asigna un parámetro a los registros del sombreador de vértices o píxeles.</span><span class="sxs-lookup"><span data-stu-id="e0802-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="e0802-106">También pueden ser cadenas descriptivas opcionales adjuntas a parámetros que no son de registro.</span><span class="sxs-lookup"><span data-stu-id="e0802-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0802-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0802-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="e0802-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0802-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0802-109">**Uso**</span><span class="sxs-lookup"><span data-stu-id="e0802-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="e0802-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0802-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0802-111">Opciones que identifican el modo en que se usan los recursos.</span><span class="sxs-lookup"><span data-stu-id="e0802-111">Options that identify how resources are used.</span></span> <span data-ttu-id="e0802-112">Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="e0802-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0802-113">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="e0802-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e0802-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0802-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0802-115">Opciones que modifican el modo en que se interpreta el uso.</span><span class="sxs-lookup"><span data-stu-id="e0802-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="e0802-116">El índice de uso y uso constituye una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="e0802-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="e0802-117">Vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="e0802-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0802-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0802-118">Remarks</span></span>

<span data-ttu-id="e0802-119">La semántica es necesaria para el sombreador de vértices y píxeles, los registros de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="e0802-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0802-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0802-120">Requirements</span></span>



| <span data-ttu-id="e0802-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0802-121">Requirement</span></span> | <span data-ttu-id="e0802-122">Value</span><span class="sxs-lookup"><span data-stu-id="e0802-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0802-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0802-123">Header</span></span><br/> | <dl> <span data-ttu-id="e0802-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0802-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0802-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0802-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0802-126">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="e0802-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
