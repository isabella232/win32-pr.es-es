---
description: Especifica cómo combinar los datos de glifo de las superficies de origen y de destino en una llamada a ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Enumeración D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717663"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="2e49f-103">Enumeración D3DCOMPOSERECTSOP</span><span class="sxs-lookup"><span data-stu-id="2e49f-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="2e49f-104">Especifica cómo combinar los datos de glifo de las superficies de origen y de destino en una llamada a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span><span class="sxs-lookup"><span data-stu-id="2e49f-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e49f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e49f-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="2e49f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2e49f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2e49f-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**Copia de D3DCOMPOSERECTS \_**</span><span class="sxs-lookup"><span data-stu-id="2e49f-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="2e49f-108">Copie el origen en el destino.</span><span class="sxs-lookup"><span data-stu-id="2e49f-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="2e49f-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ o**</span><span class="sxs-lookup"><span data-stu-id="2e49f-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="2e49f-110">Bit a bit o el origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="2e49f-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="2e49f-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ y**</span><span class="sxs-lookup"><span data-stu-id="2e49f-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="2e49f-112">And bit a bit y el origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="2e49f-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="2e49f-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ NEG**</span><span class="sxs-lookup"><span data-stu-id="2e49f-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="2e49f-114">Copie el origen negado en el destino (DST & ~ src).</span><span class="sxs-lookup"><span data-stu-id="2e49f-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="2e49f-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2e49f-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2e49f-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="2e49f-116">Reserved.</span></span> <span data-ttu-id="2e49f-117">Se usa para forzar la enumeración a 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="2e49f-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e49f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e49f-118">Requirements</span></span>



| <span data-ttu-id="2e49f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e49f-119">Requirement</span></span> | <span data-ttu-id="2e49f-120">Value</span><span class="sxs-lookup"><span data-stu-id="2e49f-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e49f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e49f-121">Header</span></span><br/> | <dl> <span data-ttu-id="2e49f-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e49f-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e49f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e49f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e49f-124">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2e49f-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




