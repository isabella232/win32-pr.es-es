---
description: Define las operaciones de Blend admitidas. Vea comentarios para obtener definiciones de términos.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumeración D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717670"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="92f16-104">Enumeración D3DBLENDOP</span><span class="sxs-lookup"><span data-stu-id="92f16-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="92f16-105">Define las operaciones de Blend admitidas.</span><span class="sxs-lookup"><span data-stu-id="92f16-105">Defines the supported blend operations.</span></span> <span data-ttu-id="92f16-106">Vea comentarios para obtener definiciones de términos.</span><span class="sxs-lookup"><span data-stu-id="92f16-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="92f16-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92f16-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="92f16-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="92f16-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92f16-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Agregar**</span><span class="sxs-lookup"><span data-stu-id="92f16-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-110">El resultado es el destino agregado al origen.</span><span class="sxs-lookup"><span data-stu-id="92f16-110">The result is the destination added to the source.</span></span> <span data-ttu-id="92f16-111">Resultado = origen + destino</span><span class="sxs-lookup"><span data-stu-id="92f16-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="92f16-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**Resta de D3DBLENDOP \_**</span><span class="sxs-lookup"><span data-stu-id="92f16-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-113">El resultado es el destino que se resta de al origen.</span><span class="sxs-lookup"><span data-stu-id="92f16-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="92f16-114">Resultado = origen-destino</span><span class="sxs-lookup"><span data-stu-id="92f16-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="92f16-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="92f16-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-116">El resultado es el origen que se resta del destino.</span><span class="sxs-lookup"><span data-stu-id="92f16-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="92f16-117">Resultado = destino-origen</span><span class="sxs-lookup"><span data-stu-id="92f16-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="92f16-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ mín.**</span><span class="sxs-lookup"><span data-stu-id="92f16-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-119">El resultado es el mínimo del origen y del destino.</span><span class="sxs-lookup"><span data-stu-id="92f16-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="92f16-120">Resultado = MIN (origen, destino)</span><span class="sxs-lookup"><span data-stu-id="92f16-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="92f16-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="92f16-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-122">El resultado es el máximo del origen y del destino.</span><span class="sxs-lookup"><span data-stu-id="92f16-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="92f16-123">Resultado = MAX (origen, destino)</span><span class="sxs-lookup"><span data-stu-id="92f16-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="92f16-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="92f16-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="92f16-125">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="92f16-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="92f16-126">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92f16-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="92f16-127">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="92f16-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92f16-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92f16-128">Remarks</span></span>

<span data-ttu-id="92f16-129">Origen, destino y resultado se definen como:</span><span class="sxs-lookup"><span data-stu-id="92f16-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="92f16-130">Término</span><span class="sxs-lookup"><span data-stu-id="92f16-130">Term</span></span>        | <span data-ttu-id="92f16-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="92f16-131">Type</span></span>   | <span data-ttu-id="92f16-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="92f16-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="92f16-133">Source</span><span class="sxs-lookup"><span data-stu-id="92f16-133">Source</span></span>      | <span data-ttu-id="92f16-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f16-134">Input</span></span>  | <span data-ttu-id="92f16-135">Color del píxel de origen antes de la operación.</span><span class="sxs-lookup"><span data-stu-id="92f16-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="92f16-136">Destination</span><span class="sxs-lookup"><span data-stu-id="92f16-136">Destination</span></span> | <span data-ttu-id="92f16-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="92f16-137">Input</span></span>  | <span data-ttu-id="92f16-138">Color del píxel en el búfer de destino antes de la operación.</span><span class="sxs-lookup"><span data-stu-id="92f16-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="92f16-139">Resultado</span><span class="sxs-lookup"><span data-stu-id="92f16-139">Result</span></span>      | <span data-ttu-id="92f16-140">Output</span><span class="sxs-lookup"><span data-stu-id="92f16-140">Output</span></span> | <span data-ttu-id="92f16-141">Valor devuelto que es el color mezclado resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="92f16-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="92f16-142">Este tipo enumerado define los valores utilizados por los siguientes Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="92f16-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="92f16-143">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="92f16-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="92f16-144">D3DRS \_ BLENDOPALPHA</span><span class="sxs-lookup"><span data-stu-id="92f16-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="92f16-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92f16-145">Requirements</span></span>



| <span data-ttu-id="92f16-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="92f16-146">Requirement</span></span> | <span data-ttu-id="92f16-147">Value</span><span class="sxs-lookup"><span data-stu-id="92f16-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92f16-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92f16-148">Header</span></span><br/> | <dl> <span data-ttu-id="92f16-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="92f16-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92f16-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="92f16-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f16-151">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="92f16-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="92f16-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="92f16-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="92f16-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="92f16-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
