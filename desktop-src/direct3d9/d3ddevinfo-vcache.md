---
description: Sugerencias de optimización de caché de vértices.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: D3DDEVINFO_VCACHE estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 80870c330adf185a869ac5e3543055c82fc7115c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678779"
---
# <a name="d3ddevinfo_vcache-structure"></a><span data-ttu-id="32b43-103">D3DDEVINFO \_ VCACHE (estructura)</span><span class="sxs-lookup"><span data-stu-id="32b43-103">D3DDEVINFO\_VCACHE structure</span></span>

<span data-ttu-id="32b43-104">Sugerencias de optimización de caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="32b43-104">Vertex cache optimization hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32b43-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a><span data-ttu-id="32b43-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="32b43-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32b43-107">**Patrón**</span><span class="sxs-lookup"><span data-stu-id="32b43-107">**Pattern**</span></span>
</dt> <dd>

<span data-ttu-id="32b43-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b43-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32b43-109">Patrón de bits.</span><span class="sxs-lookup"><span data-stu-id="32b43-109">Bit pattern.</span></span> <span data-ttu-id="32b43-110">El valor devuelto debe ser el FOURCC (' C ', ' A ', ' C ', ' H ').</span><span class="sxs-lookup"><span data-stu-id="32b43-110">Return value must be the FOURCC ('C', 'A', 'C', 'H').</span></span>

</dd> <dt>

<span data-ttu-id="32b43-111">**OptMethod**</span><span class="sxs-lookup"><span data-stu-id="32b43-111">**OptMethod**</span></span>
</dt> <dd>

<span data-ttu-id="32b43-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b43-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32b43-113">Método Optimizations.</span><span class="sxs-lookup"><span data-stu-id="32b43-113">Optimizations method.</span></span> <span data-ttu-id="32b43-114">Use 0 para obtener las franjas más largas.</span><span class="sxs-lookup"><span data-stu-id="32b43-114">Use 0 to get the longest strips.</span></span> <span data-ttu-id="32b43-115">Use 1 para optimizar el uso de la caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="32b43-115">Use 1 to optimize the vertex cache usage.</span></span>

</dd> <dt>

<span data-ttu-id="32b43-116">**CacheSize**</span><span class="sxs-lookup"><span data-stu-id="32b43-116">**CacheSize**</span></span>
</dt> <dd>

<span data-ttu-id="32b43-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b43-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32b43-118">Tamaño de caché usado como destino para la optimización.</span><span class="sxs-lookup"><span data-stu-id="32b43-118">Cache size used as a target for optimization.</span></span> <span data-ttu-id="32b43-119">Esto solo es necesario si OptMethod es 1.</span><span class="sxs-lookup"><span data-stu-id="32b43-119">This is required only if OptMethod is 1.</span></span>

</dd> <dt>

<span data-ttu-id="32b43-120">**MagicNumber**</span><span class="sxs-lookup"><span data-stu-id="32b43-120">**MagicNumber**</span></span>
</dt> <dd>

<span data-ttu-id="32b43-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32b43-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="32b43-122">Lo usan los métodos de optimización interna para determinar cuándo reiniciar las tiras.</span><span class="sxs-lookup"><span data-stu-id="32b43-122">Used by internal optimization methods to determine when to restart strips.</span></span> <span data-ttu-id="32b43-123">Un usuario no puede establecer o modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="32b43-123">This cannot be set or modified by a user.</span></span> <span data-ttu-id="32b43-124">Esto solo es necesario si OptMethod es 1.</span><span class="sxs-lookup"><span data-stu-id="32b43-124">This is required only if OptMethod is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32b43-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b43-125">Requirements</span></span>



| <span data-ttu-id="32b43-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b43-126">Requirement</span></span> | <span data-ttu-id="32b43-127">Value</span><span class="sxs-lookup"><span data-stu-id="32b43-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32b43-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32b43-128">Header</span></span><br/> | <dl> <span data-ttu-id="32b43-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="32b43-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b43-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="32b43-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b43-131">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="32b43-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="32b43-132">**GetData**</span><span class="sxs-lookup"><span data-stu-id="32b43-132">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
