---
title: Estructura de DDS_HEADER_DXT10 (DDS. h)
description: Extensión de encabezado DDS para administrar matrices de recursos, formatos de píxeles de DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- Estructura de DDS_HEADER_DXT10 DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717625"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="5c885-104">\_Estructura DXT10 del encabezado DDS \_</span><span class="sxs-lookup"><span data-stu-id="5c885-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="5c885-105">Extensión de encabezado DDS para administrar matrices de recursos, formatos de píxeles de DXGI que no se asignan a las estructuras de formato de píxel de Microsoft DirectDraw heredadas y metadatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="5c885-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c885-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c885-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="5c885-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c885-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c885-108">**dxgiFormat**</span><span class="sxs-lookup"><span data-stu-id="5c885-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="5c885-109">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5c885-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="5c885-110">El formato de píxel de la superficie (consulte [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="5c885-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="5c885-111">**resourceDimension**</span><span class="sxs-lookup"><span data-stu-id="5c885-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="5c885-112">Tipo: **[ **\_ \_ dimensión de recursos D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="5c885-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="5c885-113">Identifica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c885-113">Identifies the type of resource.</span></span> <span data-ttu-id="5c885-114">Los valores siguientes para este miembro son un subconjunto de los valores de [**la \_ \_ dimensión de recursos D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) o la enumeración de [**\_ \_ dimensiones de recursos D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :</span><span class="sxs-lookup"><span data-stu-id="5c885-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="5c885-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c885-115">Type</span></span>                                                              | <span data-ttu-id="5c885-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c885-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="5c885-117">Value</span><span class="sxs-lookup"><span data-stu-id="5c885-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="5c885-118">\_TEXTURE1D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE1D)</span><span class="sxs-lookup"><span data-stu-id="5c885-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="5c885-119">El recurso es una [textura 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="5c885-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="5c885-120">El miembro **dwWidth** del [**\_ encabezado DDS**](dds-header.md) especifica el tamaño de la textura.</span><span class="sxs-lookup"><span data-stu-id="5c885-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="5c885-121">Normalmente, se establece el miembro **dwHeight** del **\_ encabezado DDS** en 1; también se debe establecer la \_ marca de alto DDSD en el miembro **dwFlags** del **\_ encabezado DDS**.</span><span class="sxs-lookup"><span data-stu-id="5c885-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="5c885-122">2</span><span class="sxs-lookup"><span data-stu-id="5c885-122">2</span></span>     |
| <span data-ttu-id="5c885-123">\_TEXTURE2D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE2D)</span><span class="sxs-lookup"><span data-stu-id="5c885-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="5c885-124">El recurso es una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un área especificada por los miembros **dwWidth** y **dwHeight** del [**\_ encabezado DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="5c885-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="5c885-125">También puede utilizar este tipo para identificar una textura de mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="5c885-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="5c885-126">Para obtener más información sobre cómo identificar una textura de mapa de cubos, vea **miscFlag** y **tamaño** members.</span><span class="sxs-lookup"><span data-stu-id="5c885-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="5c885-127">3</span><span class="sxs-lookup"><span data-stu-id="5c885-127">3</span></span>     |
| <span data-ttu-id="5c885-128">\_TEXTURE3D de dimensión DDS \_ ( \_ dimensión de recursos D3D10 \_ \_ TEXTURE3D)</span><span class="sxs-lookup"><span data-stu-id="5c885-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="5c885-129">El recurso es una [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) con un volumen especificado por los miembros **dwWidth**, **DwHeight** y **dwDepth** del [**\_ encabezado DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="5c885-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="5c885-130">También debe establecer la marca de \_ profundidad DDSD en el miembro **dwFlags** del **\_ encabezado DDS**.</span><span class="sxs-lookup"><span data-stu-id="5c885-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="5c885-131">4</span><span class="sxs-lookup"><span data-stu-id="5c885-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="5c885-132">**miscFlag**</span><span class="sxs-lookup"><span data-stu-id="5c885-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="5c885-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c885-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="5c885-134">Identifica otras opciones menos comunes para los recursos.</span><span class="sxs-lookup"><span data-stu-id="5c885-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="5c885-135">El siguiente valor para este miembro es un subconjunto de los valores de [**la \_ \_ \_ marca de recurso D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) o de la enumeración de [**\_ \_ varios \_ recursos D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :</span><span class="sxs-lookup"><span data-stu-id="5c885-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="5c885-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c885-136">Type</span></span>                             | <span data-ttu-id="5c885-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c885-137">Description</span></span>                                                                                                  | <span data-ttu-id="5c885-138">Value</span><span class="sxs-lookup"><span data-stu-id="5c885-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="5c885-139">\_TEXTURECUBE de recursos DDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="5c885-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="5c885-140">Indica que una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) es una textura de mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="5c885-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="5c885-141">0x4</span><span class="sxs-lookup"><span data-stu-id="5c885-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="5c885-142">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="5c885-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="5c885-143">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c885-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="5c885-144">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5c885-144">The number of elements in the array.</span></span>

<span data-ttu-id="5c885-145">En el caso de una [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) que también sea una textura de mapa de cubos, este número representa el número de cubos.</span><span class="sxs-lookup"><span data-stu-id="5c885-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="5c885-146">Este número es el mismo que el número del miembro **NumCubes** de [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) o [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="5c885-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="5c885-147">En este caso, el archivo DDS contiene  \* texturas de tamaño 6 2D.</span><span class="sxs-lookup"><span data-stu-id="5c885-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="5c885-148">Para obtener más información sobre este caso, vea la descripción de **miscFlag** .</span><span class="sxs-lookup"><span data-stu-id="5c885-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="5c885-149">En el caso de una [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), debe establecer este número en 1.</span><span class="sxs-lookup"><span data-stu-id="5c885-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="5c885-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="5c885-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="5c885-151">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c885-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="5c885-152">Contiene metadatos adicionales (antes estaba reservado).</span><span class="sxs-lookup"><span data-stu-id="5c885-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="5c885-153">Los 3 bits inferiores indican el modo alfa del recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="5c885-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="5c885-154">Los 29 bits superiores están reservados y normalmente son 0.</span><span class="sxs-lookup"><span data-stu-id="5c885-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="5c885-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c885-155">Type</span></span>                            | <span data-ttu-id="5c885-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c885-156">Description</span></span>                                                                                                                              | <span data-ttu-id="5c885-157">Value</span><span class="sxs-lookup"><span data-stu-id="5c885-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="5c885-158">\_modo Alpha de DDS \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="5c885-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="5c885-159">Se desconoce el contenido del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="5c885-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="5c885-160">Este es el valor de los archivos heredados, que normalmente se supone que es una alfa "recta".</span><span class="sxs-lookup"><span data-stu-id="5c885-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="5c885-161">0x0</span><span class="sxs-lookup"><span data-stu-id="5c885-161">0x0</span></span>   |
| <span data-ttu-id="5c885-162">\_modo Alpha de DDS \_ \_ recto</span><span class="sxs-lookup"><span data-stu-id="5c885-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="5c885-163">Se supone que todo el contenido del canal alfa usa alfa recto.</span><span class="sxs-lookup"><span data-stu-id="5c885-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="5c885-164">0x1</span><span class="sxs-lookup"><span data-stu-id="5c885-164">0x1</span></span>   |
| <span data-ttu-id="5c885-165">\_PREmultiplicado en modo alfa DDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="5c885-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="5c885-166">Cualquier contenido de canal alfa usa alfa premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="5c885-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="5c885-167">Los únicos formatos de archivo heredados que indican que esta información son "DX2" y "DX4".</span><span class="sxs-lookup"><span data-stu-id="5c885-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="5c885-168">0x2</span><span class="sxs-lookup"><span data-stu-id="5c885-168">0x2</span></span>   |
| <span data-ttu-id="5c885-169">\_modo Alpha de DDS \_ \_ opaco</span><span class="sxs-lookup"><span data-stu-id="5c885-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="5c885-170">Todo el contenido del canal alfa se establece en totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="5c885-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="5c885-171">0x3</span><span class="sxs-lookup"><span data-stu-id="5c885-171">0x3</span></span>   |
| <span data-ttu-id="5c885-172">\_modo Alpha de DDS \_ \_ personalizado</span><span class="sxs-lookup"><span data-stu-id="5c885-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="5c885-173">Cualquier contenido de canal alfa se utiliza como cuarto canal y no se ha diseñado para representar la transparencia (directa o premultiplicada).</span><span class="sxs-lookup"><span data-stu-id="5c885-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="5c885-174">0x4</span><span class="sxs-lookup"><span data-stu-id="5c885-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="5c885-175">Las bibliotecas de utilidades de D3DX 10 y [d3dx 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) heredadas no podrán cargar ninguno. El archivo DDS con **miscFlags2** no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="5c885-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c885-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c885-176">Remarks</span></span>

<span data-ttu-id="5c885-177">Use esta estructura junto con un [**\_ encabezado DDS**](dds-header.md) para almacenar una matriz de recursos en un archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="5c885-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="5c885-178">Para obtener más información, consulte [matrices de texturas](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="5c885-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="5c885-179">Este encabezado está presente si el miembro **dwFourCC** de la estructura de [**\_ PIXELFORMAT de DDS**](dds-pixelformat.md) se establece en ' contenido DX10 '.</span><span class="sxs-lookup"><span data-stu-id="5c885-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c885-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c885-180">Requirements</span></span>



| <span data-ttu-id="5c885-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c885-181">Requirement</span></span> | <span data-ttu-id="5c885-182">Value</span><span class="sxs-lookup"><span data-stu-id="5c885-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5c885-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c885-183">Header</span></span><br/> | <dl> <span data-ttu-id="5c885-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c885-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c885-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c885-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c885-186">Referencia de DDS</span><span class="sxs-lookup"><span data-stu-id="5c885-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

