---
description: Una descripción de la tabla de constantes.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: D3DXCONSTANTTABLE_DESC estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821151"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="a4925-103">D3DXCONSTANTTABLE \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="a4925-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="a4925-104">Una descripción de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="a4925-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4925-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4925-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="a4925-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4925-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4925-107">**Creador**</span><span class="sxs-lookup"><span data-stu-id="a4925-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="a4925-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4925-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4925-109">Nombre del creador de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="a4925-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="a4925-110">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a4925-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a4925-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4925-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4925-112">Versión del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a4925-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="a4925-113">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="a4925-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="a4925-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4925-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a4925-115">Número de constantes en la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="a4925-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4925-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4925-116">Requirements</span></span>



| <span data-ttu-id="a4925-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4925-117">Requirement</span></span> | <span data-ttu-id="a4925-118">Value</span><span class="sxs-lookup"><span data-stu-id="a4925-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4925-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4925-119">Header</span></span><br/> | <dl> <span data-ttu-id="a4925-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4925-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4925-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4925-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4925-122">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="a4925-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a4925-123">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a4925-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
