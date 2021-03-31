---
description: Define las primitivas admitidas por Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Enumeración D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157204"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="9eafc-103">Enumeración D3DPRIMITIVETYPE</span><span class="sxs-lookup"><span data-stu-id="9eafc-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="9eafc-104">Define las primitivas admitidas por Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9eafc-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eafc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9eafc-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="9eafc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9eafc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9eafc-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="9eafc-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-108">Representa los vértices como una colección de puntos aislados.</span><span class="sxs-lookup"><span data-stu-id="9eafc-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="9eafc-109">Este valor no se admite para los primitivos indizados.</span><span class="sxs-lookup"><span data-stu-id="9eafc-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="9eafc-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-111">Representa los vértices como una lista de segmentos de línea recta aislados.</span><span class="sxs-lookup"><span data-stu-id="9eafc-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="9eafc-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-113">Representa los vértices como una sola polilínea.</span><span class="sxs-lookup"><span data-stu-id="9eafc-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="9eafc-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-115">Representa los vértices especificados como una secuencia de triángulos aislados.</span><span class="sxs-lookup"><span data-stu-id="9eafc-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="9eafc-116">Cada grupo de tres vértices define un triángulo independiente.</span><span class="sxs-lookup"><span data-stu-id="9eafc-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="9eafc-117">La selección de la cara posterior se ve afectada por el estado de representación del orden de paso actual.</span><span class="sxs-lookup"><span data-stu-id="9eafc-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="9eafc-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-119">Representa los vértices como una franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="9eafc-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="9eafc-120">La marca de selección de código en la superficie se voltea automáticamente en los triángulos con numeración uniforme.</span><span class="sxs-lookup"><span data-stu-id="9eafc-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="9eafc-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-122">Representa los vértices como un ventilador de triángulo.</span><span class="sxs-lookup"><span data-stu-id="9eafc-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="9eafc-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9eafc-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9eafc-124">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="9eafc-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9eafc-125">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9eafc-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9eafc-126">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9eafc-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9eafc-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9eafc-127">Remarks</span></span>

<span data-ttu-id="9eafc-128">El uso de [franjas de triángulo](triangle-strips.md) o de [triángulo (Direct3D 9)](triangle-fans.md) suele ser más eficaz que el uso de listas de triángulos, ya que se duplican menos vértices.</span><span class="sxs-lookup"><span data-stu-id="9eafc-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eafc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eafc-129">Requirements</span></span>



| <span data-ttu-id="9eafc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eafc-130">Requirement</span></span> | <span data-ttu-id="9eafc-131">Value</span><span class="sxs-lookup"><span data-stu-id="9eafc-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eafc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9eafc-132">Header</span></span><br/> | <dl> <span data-ttu-id="9eafc-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eafc-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eafc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eafc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eafc-135">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9eafc-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9eafc-136">**IDirect3DDevice9::D rawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9eafc-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="9eafc-137">**IDirect3DDevice9::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9eafc-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="9eafc-138">**IDirect3DDevice9::D rawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9eafc-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="9eafc-139">**IDirect3DDevice9::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9eafc-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
