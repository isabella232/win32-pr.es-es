---
description: Estas marcas se utilizan para controlar el modo en que D3DX10ComputeNormalMap genera asignaciones normales. Cualquier número de estas marcas puede ser o combinarse en cualquier combinación.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Enumeración D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721484"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="5e04d-104">D3DX10 \_ \_ enumeración de marca NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="5e04d-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="5e04d-105">Estas marcas se utilizan para controlar el modo en que [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) genera asignaciones normales.</span><span class="sxs-lookup"><span data-stu-id="5e04d-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="5e04d-106">Cualquier número de estas marcas puede ser o combinarse en cualquier combinación.</span><span class="sxs-lookup"><span data-stu-id="5e04d-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e04d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e04d-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="5e04d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5e04d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e04d-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ Mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="5e04d-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="5e04d-110">Indica que los píxeles que están fuera del borde de la textura en el eje U deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="5e04d-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="5e04d-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="5e04d-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="5e04d-112">Indica que los píxeles que están fuera del borde de la textura en el eje V deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="5e04d-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="5e04d-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**Reflejo de D3DX10 \_ NORMALMAP \_**</span><span class="sxs-lookup"><span data-stu-id="5e04d-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="5e04d-114">Igual que D3DX10 \_ NORMALMAP \_ Mirror \_ U \| D3DX10 \_ NORMALMAP \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="5e04d-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="5e04d-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="5e04d-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="5e04d-116">Invierte la dirección de cada normal.</span><span class="sxs-lookup"><span data-stu-id="5e04d-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="5e04d-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ de \_ proceso de \_ NORMALMAP**</span><span class="sxs-lookup"><span data-stu-id="5e04d-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="5e04d-118">Calcula el término de oclusión por píxel y lo codifica en el alfa.</span><span class="sxs-lookup"><span data-stu-id="5e04d-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="5e04d-119">Un valor alfa de 1 significa que el píxel no está oculto de ningún modo, y un alfa de 0 significa que el píxel está completamente oculto.</span><span class="sxs-lookup"><span data-stu-id="5e04d-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e04d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e04d-120">Requirements</span></span>



| <span data-ttu-id="5e04d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e04d-121">Requirement</span></span> | <span data-ttu-id="5e04d-122">Value</span><span class="sxs-lookup"><span data-stu-id="5e04d-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e04d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e04d-123">Header</span></span><br/> | <dl> <span data-ttu-id="5e04d-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e04d-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e04d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e04d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e04d-126">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="5e04d-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




