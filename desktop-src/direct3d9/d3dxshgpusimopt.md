---
description: Describe la resolución de la sombra del búfer de z que se usará en la simulación de iluminación directa de Radiance Transfer (PRT) precalculada en la GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumeración D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718420"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="ca989-103">Enumeración D3DXSHGPUSIMOPT</span><span class="sxs-lookup"><span data-stu-id="ca989-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="ca989-104">Describe la resolución de la sombra del búfer de z que se usará en la simulación de iluminación directa de Radiance Transfer (PRT) precalculada en la GPU.</span><span class="sxs-lookup"><span data-stu-id="ca989-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="ca989-105">También se puede especificar un búfer z de mayor calidad para reducir el ruido en los resultados de la simulación de iluminación directa, aunque la simulación será más lenta.</span><span class="sxs-lookup"><span data-stu-id="ca989-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca989-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca989-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="ca989-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ca989-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ca989-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="ca989-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-109">Simulación de baja resolución.</span><span class="sxs-lookup"><span data-stu-id="ca989-109">Low resolution simulation.</span></span> <span data-ttu-id="ca989-110">En la simulación se usa una textura de 256 x 256 píxeles para codificar la sombra del búfer de z.</span><span class="sxs-lookup"><span data-stu-id="ca989-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ca989-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="ca989-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-112">Simulación de resolución media.</span><span class="sxs-lookup"><span data-stu-id="ca989-112">Medium resolution simulation.</span></span> <span data-ttu-id="ca989-113">En la simulación se usa una textura de 512 x 512 píxeles para codificar la sombra del búfer de z.</span><span class="sxs-lookup"><span data-stu-id="ca989-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="ca989-114">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca989-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="ca989-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="ca989-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-116">Simulación de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="ca989-116">High resolution simulation.</span></span> <span data-ttu-id="ca989-117">En la simulación se usa una textura de 1024 x 1024 píxeles para codificar la sombra del búfer de z.</span><span class="sxs-lookup"><span data-stu-id="ca989-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ca989-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="ca989-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-119">Simulación de resolución más alta.</span><span class="sxs-lookup"><span data-stu-id="ca989-119">Highest resolution simulation.</span></span> <span data-ttu-id="ca989-120">En la simulación se usa una textura de 2048 x 2048 píxeles para codificar la sombra del búfer de z.</span><span class="sxs-lookup"><span data-stu-id="ca989-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ca989-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ highquality**</span><span class="sxs-lookup"><span data-stu-id="ca989-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-122">La simulación es de alta precisión, independientemente de la resolución seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ca989-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="ca989-123">Si se establece este valor, se reducirá el ruido de los resultados de la simulación de iluminación directa, aunque la simulación será más lenta.</span><span class="sxs-lookup"><span data-stu-id="ca989-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="ca989-124">Puede combinarse con uno de los valores de resolución.</span><span class="sxs-lookup"><span data-stu-id="ca989-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="ca989-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca989-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ca989-126">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="ca989-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ca989-127">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ca989-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ca989-128">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ca989-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca989-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca989-129">Remarks</span></span>

<span data-ttu-id="ca989-130">Solo se puede especificar uno de los valores de resolución y se puede combinar con el valor de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="ca989-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca989-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca989-131">Requirements</span></span>



| <span data-ttu-id="ca989-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca989-132">Requirement</span></span> | <span data-ttu-id="ca989-133">Value</span><span class="sxs-lookup"><span data-stu-id="ca989-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca989-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca989-134">Header</span></span><br/> | <dl> <span data-ttu-id="ca989-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca989-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca989-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca989-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca989-137">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="ca989-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




