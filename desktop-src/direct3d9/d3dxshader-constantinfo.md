---
description: D3DXSHADER \_ estructura CONSTANTINFO
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: D3DXSHADER_CONSTANTINFO estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280302"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="5f311-103">D3DXSHADER \_ estructura CONSTANTINFO</span><span class="sxs-lookup"><span data-stu-id="5f311-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="5f311-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f311-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="5f311-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f311-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f311-106">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5f311-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-107">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-108">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información de constante.</span><span class="sxs-lookup"><span data-stu-id="5f311-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="5f311-109">**RegisterSet**</span><span class="sxs-lookup"><span data-stu-id="5f311-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-110">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-111">Conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="5f311-111">Register set.</span></span> <span data-ttu-id="5f311-112">Vea [**D3DXREGISTER \_ set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="5f311-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f311-113">**RegisterIndex**</span><span class="sxs-lookup"><span data-stu-id="5f311-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-115">Índice de registro.</span><span class="sxs-lookup"><span data-stu-id="5f311-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="5f311-116">**RegisterCount**</span><span class="sxs-lookup"><span data-stu-id="5f311-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-117">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-118">Número de registros.</span><span class="sxs-lookup"><span data-stu-id="5f311-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="5f311-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5f311-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-120">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5f311-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5f311-122">**Requerida**</span><span class="sxs-lookup"><span data-stu-id="5f311-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-124">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información de [**\_ TYPEINFO de D3DXSHADER**](d3dxshader-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5f311-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="5f311-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="5f311-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="5f311-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f311-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f311-127">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5f311-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f311-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f311-128">Requirements</span></span>



| <span data-ttu-id="5f311-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f311-129">Requirement</span></span> | <span data-ttu-id="5f311-130">Value</span><span class="sxs-lookup"><span data-stu-id="5f311-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f311-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f311-131">Header</span></span><br/> | <dl> <span data-ttu-id="5f311-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f311-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f311-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f311-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f311-134">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="5f311-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
