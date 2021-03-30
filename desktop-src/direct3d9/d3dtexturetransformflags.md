---
description: Define valores de transformación de coordenadas de textura.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumeración D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280261"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="d7f99-103">Enumeración D3DTEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="d7f99-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="d7f99-104">Define valores de transformación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d7f99-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7f99-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="d7f99-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d7f99-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7f99-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**Deshabilitación de D3DTTFF \_**</span><span class="sxs-lookup"><span data-stu-id="d7f99-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-108">Las coordenadas de textura se pasan directamente al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d7f99-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="d7f99-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-110">El rasterizador debería esperar coordenadas de textura 1D.</span><span class="sxs-lookup"><span data-stu-id="d7f99-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="d7f99-111">Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="d7f99-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="d7f99-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-113">El rasterizador debería esperar coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="d7f99-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="d7f99-114">Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="d7f99-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="d7f99-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-116">El rasterizador debería esperar coordenadas de textura 3D.</span><span class="sxs-lookup"><span data-stu-id="d7f99-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="d7f99-117">Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="d7f99-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="d7f99-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-119">El rasterizador debería esperar 4D coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d7f99-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="d7f99-120">Este valor lo utiliza el procesamiento de vértices de función fija; debe establecerse en 0 cuando se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="d7f99-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ previsto**</span><span class="sxs-lookup"><span data-stu-id="d7f99-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-122">Esta marca se respeta por la canalización de píxeles de función fija, así como por la canalización de píxeles programable en las versiones PS 1 \_ \_ a PS \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="d7f99-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="d7f99-123">Cuando se habilita la proyección de textura para una fase de textura, los cuatro valores de punto flotante se deben escribir en el registro de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d7f99-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="d7f99-124">Cada coordenada de textura se divide por el último elemento antes de pasarla al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d7f99-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="d7f99-125">Por ejemplo, si se especifica esta marca con la \_ marca D3DTTFF COUNT3, las coordenadas de textura primera y segunda se dividen por la tercera coordenada antes de pasarse al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d7f99-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="d7f99-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d7f99-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d7f99-127">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="d7f99-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d7f99-128">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d7f99-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d7f99-129">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d7f99-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7f99-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7f99-130">Remarks</span></span>

<span data-ttu-id="d7f99-131">Las coordenadas de textura se pueden transformar mediante una matriz de 4 x 4 antes de que los resultados se pasen al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d7f99-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="d7f99-132">Las transformaciones de coordenadas de textura se establecen mediante una llamada a [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api)y pasando el \_ Estado de fase de textura D3DTSS TEXTURETRANSFORMFLAGS y uno de los valores de **D3DTEXTURETRANSFORMFLAGS**.</span><span class="sxs-lookup"><span data-stu-id="d7f99-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="d7f99-133">Para obtener más información sobre las transformaciones de textura, vea [transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="d7f99-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f99-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f99-134">Requirements</span></span>



| <span data-ttu-id="d7f99-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f99-135">Requirement</span></span> | <span data-ttu-id="d7f99-136">Value</span><span class="sxs-lookup"><span data-stu-id="d7f99-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f99-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7f99-137">Header</span></span><br/> | <dl> <span data-ttu-id="d7f99-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f99-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f99-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f99-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f99-140">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d7f99-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d7f99-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d7f99-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
