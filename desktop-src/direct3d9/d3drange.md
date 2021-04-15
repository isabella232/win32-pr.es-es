---
description: Define un intervalo.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: Estructura D3DRANGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707927"
---
# <a name="d3drange-structure"></a><span data-ttu-id="23e3c-103">Estructura D3DRANGE</span><span class="sxs-lookup"><span data-stu-id="23e3c-103">D3DRANGE structure</span></span>

<span data-ttu-id="23e3c-104">Define un intervalo.</span><span class="sxs-lookup"><span data-stu-id="23e3c-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e3c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23e3c-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="23e3c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="23e3c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="23e3c-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="23e3c-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23e3c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="23e3c-109">Desplazamiento, en bytes.</span><span class="sxs-lookup"><span data-stu-id="23e3c-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-110">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="23e3c-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23e3c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="23e3c-112">Tamaño, en bytes.</span><span class="sxs-lookup"><span data-stu-id="23e3c-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23e3c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23e3c-113">Requirements</span></span>



| <span data-ttu-id="23e3c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e3c-114">Requirement</span></span> | <span data-ttu-id="23e3c-115">Value</span><span class="sxs-lookup"><span data-stu-id="23e3c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e3c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23e3c-116">Header</span></span><br/> | <dl> <span data-ttu-id="23e3c-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e3c-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e3c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="23e3c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e3c-119">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="23e3c-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
