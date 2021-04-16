---
description: Define operaciones de búfer de estarcido.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumeración D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678787"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="97bf0-103">Enumeración D3DSTENCILOP</span><span class="sxs-lookup"><span data-stu-id="97bf0-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="97bf0-104">Define operaciones de búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="97bf0-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bf0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97bf0-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="97bf0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="97bf0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="97bf0-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ mantener**</span><span class="sxs-lookup"><span data-stu-id="97bf0-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-108">No actualice la entrada en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="97bf0-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="97bf0-109">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="97bf0-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ cero**</span><span class="sxs-lookup"><span data-stu-id="97bf0-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-111">Establezca la entrada de búfer de estarcido en 0.</span><span class="sxs-lookup"><span data-stu-id="97bf0-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ reemplazar**</span><span class="sxs-lookup"><span data-stu-id="97bf0-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-113">Reemplace la entrada del búfer de la galería de símbolos por un valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="97bf0-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**</span><span class="sxs-lookup"><span data-stu-id="97bf0-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-115">Incremente la entrada del búfer de la galería de símbolos y la fijación al valor máximo.</span><span class="sxs-lookup"><span data-stu-id="97bf0-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**</span><span class="sxs-lookup"><span data-stu-id="97bf0-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-117">Disminuya la entrada del búfer de la galería de símbolos, de la abrazadera a cero.</span><span class="sxs-lookup"><span data-stu-id="97bf0-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**\_Invertir D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="97bf0-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-119">Invierta los bits en la entrada de búfer de la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="97bf0-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ incr**</span><span class="sxs-lookup"><span data-stu-id="97bf0-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-121">Incremente la entrada del búfer de la galería de símbolos, ajustándola a cero si el nuevo valor supera el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="97bf0-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ decr (**</span><span class="sxs-lookup"><span data-stu-id="97bf0-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-123">Disminuye la entrada del búfer de estarcido, ajustándola al valor máximo si el nuevo valor es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="97bf0-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="97bf0-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="97bf0-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="97bf0-125">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="97bf0-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="97bf0-126">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="97bf0-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="97bf0-127">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="97bf0-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97bf0-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97bf0-128">Remarks</span></span>

<span data-ttu-id="97bf0-129">Las entradas de búfer de estarcido son valores enteros comprendidos entre 0 y 2 ⁿ-1, donde n es la profundidad de bits del búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="97bf0-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="97bf0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97bf0-130">Requirements</span></span>



| <span data-ttu-id="97bf0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="97bf0-131">Requirement</span></span> | <span data-ttu-id="97bf0-132">Value</span><span class="sxs-lookup"><span data-stu-id="97bf0-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97bf0-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97bf0-133">Header</span></span><br/> | <dl> <span data-ttu-id="97bf0-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="97bf0-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97bf0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="97bf0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bf0-136">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="97bf0-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




