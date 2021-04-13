---
description: Define las caras de un mapa.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: Enumeración D3DCUBEMAP_FACES (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362480"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="9c74d-103">\_Enumeración de caras de D3DCUBEMAP</span><span class="sxs-lookup"><span data-stu-id="9c74d-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="9c74d-104">Define las caras de un mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c74d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c74d-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="9c74d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9c74d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c74d-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ facial \_ positivo \_ X**</span><span class="sxs-lookup"><span data-stu-id="9c74d-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-108">Letra x positiva del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP de \_ superficie \_ negativa \_ X**</span><span class="sxs-lookup"><span data-stu-id="9c74d-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-110">Letra x negativa del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ facial \_ positivo \_ Y**</span><span class="sxs-lookup"><span data-stu-id="9c74d-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-112">Caras y positivas del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP a la \_ esfera \_ negativa \_ Y**</span><span class="sxs-lookup"><span data-stu-id="9c74d-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-114">Letra y negativa del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ sonriente \_ positivo \_ Z**</span><span class="sxs-lookup"><span data-stu-id="9c74d-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-116">Letra z positiva del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP a la \_ esfera \_ negativo \_ Z**</span><span class="sxs-lookup"><span data-stu-id="9c74d-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-118">Letra z negativa del mapa.</span><span class="sxs-lookup"><span data-stu-id="9c74d-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="9c74d-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**\_DWORD de \_ fuerza de D3DCUBEMAP \_**</span><span class="sxs-lookup"><span data-stu-id="9c74d-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9c74d-120">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="9c74d-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9c74d-121">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9c74d-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9c74d-122">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9c74d-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c74d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c74d-123">Requirements</span></span>



| <span data-ttu-id="9c74d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c74d-124">Requirement</span></span> | <span data-ttu-id="9c74d-125">Value</span><span class="sxs-lookup"><span data-stu-id="9c74d-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c74d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c74d-126">Header</span></span><br/> | <dl> <span data-ttu-id="9c74d-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c74d-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c74d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c74d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c74d-129">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9c74d-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9c74d-130">**IDirect3DCubeTexture9::AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="9c74d-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="9c74d-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="9c74d-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="9c74d-132">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="9c74d-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="9c74d-133">**IDirect3DCubeTexture9::UnlockRect**</span><span class="sxs-lookup"><span data-stu-id="9c74d-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
