---
description: Define un rectángulo.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: Estructura D3DRECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821154"
---
# <a name="d3drect-structure"></a><span data-ttu-id="07f16-103">Estructura D3DRECT</span><span class="sxs-lookup"><span data-stu-id="07f16-103">D3DRECT structure</span></span>

<span data-ttu-id="07f16-104">Define un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f16-104">Defines a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07f16-105">Syntax</span></span>


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a><span data-ttu-id="07f16-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="07f16-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07f16-107">**x1**</span><span class="sxs-lookup"><span data-stu-id="07f16-107">**x1**</span></span>
</dt> <dd>

<span data-ttu-id="07f16-108">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f16-108">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07f16-109">Coordenada X de la esquina superior izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f16-109">The x-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="07f16-110">**y1**</span><span class="sxs-lookup"><span data-stu-id="07f16-110">**y1**</span></span>
</dt> <dd>

<span data-ttu-id="07f16-111">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f16-111">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07f16-112">Coordenada Y de la esquina superior izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f16-112">The y-coordinate of the upper-left corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="07f16-113">**RCA**</span><span class="sxs-lookup"><span data-stu-id="07f16-113">**x2**</span></span>
</dt> <dd>

<span data-ttu-id="07f16-114">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f16-114">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07f16-115">Coordenada x de la esquina inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f16-115">The x-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="07f16-116">**a2**</span><span class="sxs-lookup"><span data-stu-id="07f16-116">**y2**</span></span>
</dt> <dd>

<span data-ttu-id="07f16-117">Tipo: **[ **Long**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07f16-117">Type: **[**LONG**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07f16-118">Coordenada y de la esquina inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="07f16-118">The y-coordinate of the lower-right corner of the rectangle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07f16-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07f16-119">Requirements</span></span>



| <span data-ttu-id="07f16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f16-120">Requirement</span></span> | <span data-ttu-id="07f16-121">Value</span><span class="sxs-lookup"><span data-stu-id="07f16-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07f16-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07f16-122">Header</span></span><br/> | <dl> <span data-ttu-id="07f16-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f16-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f16-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f16-125">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="07f16-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="07f16-126">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="07f16-126">**Clear**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
