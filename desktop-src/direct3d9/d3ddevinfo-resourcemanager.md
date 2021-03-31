---
description: Estadísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: D3DDEVINFO_ResourceManager estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820978"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="7e63a-103">D3DDEVINFO ( \_ estructura de ResourceManager)</span><span class="sxs-lookup"><span data-stu-id="7e63a-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="7e63a-104">Estadísticas de uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e63a-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e63a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e63a-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="7e63a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e63a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e63a-107">**stats**</span><span class="sxs-lookup"><span data-stu-id="7e63a-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="7e63a-108">Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="7e63a-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e63a-109">Matriz de elementos de estadísticas de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e63a-109">Array of resource statistics elements.</span></span> <span data-ttu-id="7e63a-110">Vea [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="7e63a-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e63a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e63a-111">Remarks</span></span>

<span data-ttu-id="7e63a-112">D3DRTYPECOUNT hace referencia al número de enumeraciones de [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="7e63a-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e63a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e63a-113">Requirements</span></span>



| <span data-ttu-id="7e63a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e63a-114">Requirement</span></span> | <span data-ttu-id="7e63a-115">Value</span><span class="sxs-lookup"><span data-stu-id="7e63a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e63a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e63a-116">Header</span></span><br/> | <dl> <span data-ttu-id="7e63a-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e63a-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e63a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e63a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e63a-119">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7e63a-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
