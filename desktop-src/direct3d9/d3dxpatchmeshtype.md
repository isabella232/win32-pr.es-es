---
description: Tipos de revisión de malla.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Enumeración D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717560"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="72be6-103">Enumeración D3DXPATCHMESHTYPE</span><span class="sxs-lookup"><span data-stu-id="72be6-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="72be6-104">Tipos de revisión de malla.</span><span class="sxs-lookup"><span data-stu-id="72be6-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="72be6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72be6-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="72be6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="72be6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="72be6-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="72be6-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="72be6-108">Tipo de malla de revisión de rectángulo.</span><span class="sxs-lookup"><span data-stu-id="72be6-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="72be6-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**</span><span class="sxs-lookup"><span data-stu-id="72be6-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="72be6-110">Tipo de malla de revisión de triángulo.</span><span class="sxs-lookup"><span data-stu-id="72be6-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="72be6-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**</span><span class="sxs-lookup"><span data-stu-id="72be6-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="72be6-112">Tipo de malla N-patch.</span><span class="sxs-lookup"><span data-stu-id="72be6-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="72be6-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="72be6-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="72be6-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="72be6-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="72be6-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="72be6-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="72be6-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="72be6-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72be6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72be6-117">Remarks</span></span>

<span data-ttu-id="72be6-118">Las revisiones de triángulo tienen tres lados y se describen en [**\_ información de D3DTRIPATCH**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="72be6-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="72be6-119">Las revisiones de los rectángulos están en cuatro caras y se describen en [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="72be6-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72be6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72be6-120">Requirements</span></span>



| <span data-ttu-id="72be6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="72be6-121">Requirement</span></span> | <span data-ttu-id="72be6-122">Value</span><span class="sxs-lookup"><span data-stu-id="72be6-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72be6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72be6-123">Header</span></span><br/> | <dl> <span data-ttu-id="72be6-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="72be6-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72be6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="72be6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72be6-126">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="72be6-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="72be6-127">Usar primitivas de Higher-Order (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="72be6-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




