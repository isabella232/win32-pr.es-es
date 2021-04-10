---
description: Define constantes que describen los modos de direccionamiento de textura admitidos.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumeración D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083712"
---
# <a name="d3dtextureaddress-enumeration"></a><span data-ttu-id="b27ea-103">Enumeración D3DTEXTUREADDRESS</span><span class="sxs-lookup"><span data-stu-id="b27ea-103">D3DTEXTUREADDRESS enumeration</span></span>

<span data-ttu-id="b27ea-104">Define constantes que describen los modos de direccionamiento de textura admitidos.</span><span class="sxs-lookup"><span data-stu-id="b27ea-104">Defines constants that describe the supported texture-addressing modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b27ea-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a><span data-ttu-id="b27ea-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b27ea-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b27ea-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Wrap**</span><span class="sxs-lookup"><span data-stu-id="b27ea-107"><span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS\_WRAP**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-108">Coloque la textura en mosaico en cada unión de enteros.</span><span class="sxs-lookup"><span data-stu-id="b27ea-108">Tile the texture at every integer junction.</span></span> <span data-ttu-id="b27ea-109">Por ejemplo, para los valores entre 0 y 3, la textura se repite tres veces; no se realiza la creación de reflejo.</span><span class="sxs-lookup"><span data-stu-id="b27ea-109">For example, for u values between 0 and 3, the texture is repeated three times; no mirroring is performed.</span></span>

</dd> <dt>

<span data-ttu-id="b27ea-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**Reflejo de D3DTADDRESS \_**</span><span class="sxs-lookup"><span data-stu-id="b27ea-110"><span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-111">Similar a D3DTADDRESS \_ Wrap, salvo que la textura se voltea en cada unión de enteros.</span><span class="sxs-lookup"><span data-stu-id="b27ea-111">Similar to D3DTADDRESS\_WRAP, except that the texture is flipped at every integer junction.</span></span> <span data-ttu-id="b27ea-112">para los valores entre 0 y 1, por ejemplo, la textura se corrige normalmente; entre 1 y 2, la textura se voltea (reflejada). entre 2 y 3, la textura es normal de nuevo; etc.</span><span class="sxs-lookup"><span data-stu-id="b27ea-112">For u values between 0 and 1, for example, the texture is addressed normally; between 1 and 2, the texture is flipped (mirrored); between 2 and 3, the texture is normal again; and so on.</span></span>

</dd> <dt>

<span data-ttu-id="b27ea-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**\_Abrazadera D3DTADDRESS**</span><span class="sxs-lookup"><span data-stu-id="b27ea-113"><span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS\_CLAMP**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-114">Las coordenadas de textura fuera del intervalo \[ 0,0, 1,0 \] se establecen en el color de textura en 0,0 o 1,0, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b27ea-114">Texture coordinates outside the range \[0.0, 1.0\] are set to the texture color at 0.0 or 1.0, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b27ea-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**Borde de D3DTADDRESS \_**</span><span class="sxs-lookup"><span data-stu-id="b27ea-115"><span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**D3DTADDRESS\_BORDER**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-116">Las coordenadas de textura fuera del intervalo \[ 0,0, 1,0 \] se establecen en el color del borde.</span><span class="sxs-lookup"><span data-stu-id="b27ea-116">Texture coordinates outside the range \[0.0, 1.0\] are set to the border color.</span></span>

</dd> <dt>

<span data-ttu-id="b27ea-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**</span><span class="sxs-lookup"><span data-stu-id="b27ea-117"><span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS\_MIRRORONCE**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-118">Similar a D3DTADDRESS \_ Mirror y D3DTADDRESS \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="b27ea-118">Similar to D3DTADDRESS\_MIRROR and D3DTADDRESS\_CLAMP.</span></span> <span data-ttu-id="b27ea-119">Toma el valor absoluto de la coordenada de textura (por lo tanto, la creación de reflejo alrededor de 0) y, a continuación, se fija en el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="b27ea-119">Takes the absolute value of the texture coordinate (thus, mirroring around 0), and then clamps to the maximum value.</span></span> <span data-ttu-id="b27ea-120">El uso más común es para las texturas de volumen, donde la compatibilidad con el modo completo de D3DTADDRESS \_ MIRRORONCE Texture-Addressing no es necesario, pero los datos son simétricos alrededor de un eje.</span><span class="sxs-lookup"><span data-stu-id="b27ea-120">The most common usage is for volume textures, where support for the full D3DTADDRESS\_MIRRORONCE texture-addressing mode is not necessary, but the data is symmetric around the one axis.</span></span>

</dd> <dt>

<span data-ttu-id="b27ea-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b27ea-121"><span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b27ea-122">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b27ea-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b27ea-123">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b27ea-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b27ea-124">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b27ea-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b27ea-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b27ea-125">Requirements</span></span>



| <span data-ttu-id="b27ea-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27ea-126">Requirement</span></span> | <span data-ttu-id="b27ea-127">Value</span><span class="sxs-lookup"><span data-stu-id="b27ea-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b27ea-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b27ea-128">Header</span></span><br/> | <dl> <span data-ttu-id="b27ea-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27ea-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27ea-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b27ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27ea-131">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b27ea-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b27ea-132">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="b27ea-132">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
