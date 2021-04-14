---
description: Define los tipos de textura de muestra para los sombreadores de vértices.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumeración D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424331"
---
# <a name="d3dsampler_texture_type-enumeration"></a><span data-ttu-id="42234-103">\_Enumeración de tipo de textura D3DSAMPLER \_</span><span class="sxs-lookup"><span data-stu-id="42234-103">D3DSAMPLER\_TEXTURE\_TYPE enumeration</span></span>

<span data-ttu-id="42234-104">Define los tipos de textura de muestra para los sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="42234-104">Defines the sampler texture types for vertex shaders.</span></span>

## <a name="syntax"></a><span data-ttu-id="42234-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42234-105">Syntax</span></span>


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="42234-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="42234-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42234-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="42234-107"><span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="42234-108">Valor sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="42234-108">Uninitialized value.</span></span> <span data-ttu-id="42234-109">El valor de este elemento es 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="42234-109">The value of this element is 0 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="42234-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**</span><span class="sxs-lookup"><span data-stu-id="42234-110"><span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT\_2D**</span></span>
</dt> <dd>

<span data-ttu-id="42234-111">Declarar una textura 2D.</span><span class="sxs-lookup"><span data-stu-id="42234-111">Declaring a 2D texture.</span></span> <span data-ttu-id="42234-112">El valor de este elemento es 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="42234-112">The value of this element is 2 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="42234-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="42234-113"><span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**D3DSTT\_CUBE**</span></span>
</dt> <dd>

<span data-ttu-id="42234-114">Declarar una textura de cubo.</span><span class="sxs-lookup"><span data-stu-id="42234-114">Declaring a cube texture.</span></span> <span data-ttu-id="42234-115">El valor de este elemento es 3 &lt; &lt; D3DSP de \_ TEXTURETYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="42234-115">The value of this element is 3 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="42234-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volumen D3DSTT**</span><span class="sxs-lookup"><span data-stu-id="42234-116"><span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**D3DSTT\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="42234-117">Declarar una textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="42234-117">Declaring a volume texture.</span></span> <span data-ttu-id="42234-118">El valor de este elemento es 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.</span><span class="sxs-lookup"><span data-stu-id="42234-118">The value of this element is 4 &lt;&lt; D3DSP\_TEXTURETYPE\_SHIFT.</span></span>

</dd> <dt>

<span data-ttu-id="42234-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42234-119"><span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="42234-120">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="42234-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="42234-121">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42234-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="42234-122">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42234-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42234-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42234-123">Requirements</span></span>



| <span data-ttu-id="42234-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42234-124">Requirement</span></span> | <span data-ttu-id="42234-125">Value</span><span class="sxs-lookup"><span data-stu-id="42234-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42234-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42234-126">Header</span></span><br/> | <dl> <span data-ttu-id="42234-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="42234-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42234-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="42234-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42234-129">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="42234-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




