---
description: Define los tipos de recursos.
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: Enumeración D3DRESOURCETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d7fab861d85a2c0289ba1636dece0e76c7819e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003774"
---
# <a name="d3dresourcetype-enumeration"></a><span data-ttu-id="a7264-103">Enumeración D3DRESOURCETYPE</span><span class="sxs-lookup"><span data-stu-id="a7264-103">D3DRESOURCETYPE enumeration</span></span>

<span data-ttu-id="a7264-104">Define los tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7264-104">Defines resource types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7264-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7264-105">Syntax</span></span>


```C++
typedef enum D3DRESOURCETYPE { 
  D3DRTYPE_SURFACE        = 1,
  D3DRTYPE_VOLUME         = 2,
  D3DRTYPE_TEXTURE        = 3,
  D3DRTYPE_VOLUMETEXTURE  = 4,
  D3DRTYPE_CubeTexture    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a><span data-ttu-id="a7264-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7264-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7264-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**\_Superficie D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="a7264-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE\_SURFACE**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-108">Recurso de Surface.</span><span class="sxs-lookup"><span data-stu-id="a7264-108">Surface resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**\_Volumen D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="a7264-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-110">Recurso de volumen.</span><span class="sxs-lookup"><span data-stu-id="a7264-110">Volume resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**\_Textura D3DRTYPE**</span><span class="sxs-lookup"><span data-stu-id="a7264-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-112">Recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="a7264-112">Texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE \_ VOLUMETEXTURE**</span><span class="sxs-lookup"><span data-stu-id="a7264-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE\_VOLUMETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-114">Recurso de textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="a7264-114">Volume texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE \_ CubeTexture**</span><span class="sxs-lookup"><span data-stu-id="a7264-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE\_CubeTexture**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-116">Recurso de textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="a7264-116">Cube texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ VERTEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="a7264-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE\_VERTEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-118">Recurso de búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="a7264-118">Vertex buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE \_ INDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="a7264-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE\_INDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-120">Recurso de búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="a7264-120">Index buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="a7264-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7264-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a7264-122">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="a7264-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a7264-123">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a7264-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a7264-124">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a7264-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7264-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7264-125">Requirements</span></span>



| <span data-ttu-id="a7264-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7264-126">Requirement</span></span> | <span data-ttu-id="a7264-127">Value</span><span class="sxs-lookup"><span data-stu-id="a7264-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7264-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7264-128">Header</span></span><br/> | <dl> <span data-ttu-id="a7264-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7264-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7264-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7264-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7264-131">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a7264-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a7264-132">**IDirect3DResource9:: GetType**</span><span class="sxs-lookup"><span data-stu-id="a7264-132">**IDirect3DResource9::GetType**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
