---
title: Enumeración D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Opciones de asignación normales. Puede combinar cualquier número de estas marcas mediante una operación OR bit a bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Enumeración de D3DX11_NORMALMAP_FLAG Direct3D 11
- LPD3DX11_NORMALMAP_FLAG puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280506"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="8ce55-107">D3DX11 \_ \_ enumeración de marca NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="8ce55-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="8ce55-108">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="8ce55-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="8ce55-109">Opciones de asignación normales.</span><span class="sxs-lookup"><span data-stu-id="8ce55-109">Normal map options.</span></span> <span data-ttu-id="8ce55-110">Puede combinar cualquier número de estas marcas mediante una operación OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="8ce55-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce55-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ce55-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="8ce55-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="8ce55-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8ce55-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ Mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="8ce55-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="8ce55-114">Indica que los píxeles que están fuera del borde de la textura en el eje U deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="8ce55-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="8ce55-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="8ce55-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="8ce55-116">Indica que los píxeles que están fuera del borde de la textura en el eje V deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="8ce55-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="8ce55-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**Reflejo de D3DX11 \_ NORMALMAP \_**</span><span class="sxs-lookup"><span data-stu-id="8ce55-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="8ce55-118">Igual que D3DX11 \_ NORMALMAP \_ Mirror \_ U \| D3DX11 \_ NORMALMAP \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="8ce55-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="8ce55-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**</span><span class="sxs-lookup"><span data-stu-id="8ce55-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="8ce55-120">Invierte la dirección de cada normal.</span><span class="sxs-lookup"><span data-stu-id="8ce55-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="8ce55-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ de \_ proceso de \_ NORMALMAP**</span><span class="sxs-lookup"><span data-stu-id="8ce55-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="8ce55-122">Calcula el término de oclusión por píxel y lo codifica en el alfa.</span><span class="sxs-lookup"><span data-stu-id="8ce55-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="8ce55-123">Un valor alfa de 1 significa que el píxel no está oculto de ningún modo, y un alfa de 0 significa que el píxel está completamente oculto.</span><span class="sxs-lookup"><span data-stu-id="8ce55-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ce55-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ce55-124">Remarks</span></span>

<span data-ttu-id="8ce55-125">[**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)usa estas marcas.</span><span class="sxs-lookup"><span data-stu-id="8ce55-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce55-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ce55-126">Requirements</span></span>



| <span data-ttu-id="8ce55-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce55-127">Requirement</span></span> | <span data-ttu-id="8ce55-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ce55-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce55-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ce55-129">Header</span></span><br/> | <dl> <span data-ttu-id="8ce55-130"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ce55-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce55-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ce55-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce55-132">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="8ce55-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





