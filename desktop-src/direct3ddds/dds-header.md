---
title: Estructura de DDS_HEADER (DDS. h)
description: Describe un encabezado de archivo DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- Estructura de DDS_HEADER DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717624"
---
# <a name="dds_header-structure"></a><span data-ttu-id="67475-104">\_Estructura del encabezado DDS</span><span class="sxs-lookup"><span data-stu-id="67475-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="67475-105">Describe un encabezado de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="67475-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67475-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="67475-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="67475-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="67475-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="67475-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="67475-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-110">Tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="67475-110">Size of structure.</span></span> <span data-ttu-id="67475-111">Este miembro debe establecerse en 124.</span><span class="sxs-lookup"><span data-stu-id="67475-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="67475-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="67475-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="67475-113">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-114">Marcas para indicar qué miembros contienen datos válidos.</span><span class="sxs-lookup"><span data-stu-id="67475-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="67475-115">Marca</span><span class="sxs-lookup"><span data-stu-id="67475-115">Flag</span></span>              | <span data-ttu-id="67475-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="67475-116">Description</span></span>                                                  | <span data-ttu-id="67475-117">Value</span><span class="sxs-lookup"><span data-stu-id="67475-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="67475-118">\_Cap DDSD</span><span class="sxs-lookup"><span data-stu-id="67475-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="67475-119">Se requiere en cada archivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="67475-120">0x1</span><span class="sxs-lookup"><span data-stu-id="67475-120">0x1</span></span>      |
| <span data-ttu-id="67475-121">alto de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="67475-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="67475-122">Se requiere en cada archivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="67475-123">0x2</span><span class="sxs-lookup"><span data-stu-id="67475-123">0x2</span></span>      |
| <span data-ttu-id="67475-124">ancho de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="67475-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="67475-125">Se requiere en cada archivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="67475-126">0x4</span><span class="sxs-lookup"><span data-stu-id="67475-126">0x4</span></span>      |
| <span data-ttu-id="67475-127">paso de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="67475-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="67475-128">Obligatorio cuando se proporciona el tono para una textura sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="67475-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="67475-129">0x8</span><span class="sxs-lookup"><span data-stu-id="67475-129">0x8</span></span>      |
| <span data-ttu-id="67475-130">DDSD \_ PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="67475-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="67475-131">Se requiere en cada archivo. DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="67475-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="67475-132">0x1000</span></span>   |
| <span data-ttu-id="67475-133">DDSD \_ MIPMAPCOUNT</span><span class="sxs-lookup"><span data-stu-id="67475-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="67475-134">Obligatorio en una textura de mipmapped.</span><span class="sxs-lookup"><span data-stu-id="67475-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="67475-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="67475-135">0x20000</span></span>  |
| <span data-ttu-id="67475-136">DDSD \_ LINEARSIZE</span><span class="sxs-lookup"><span data-stu-id="67475-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="67475-137">Obligatorio cuando se proporciona el tono para una textura comprimida.</span><span class="sxs-lookup"><span data-stu-id="67475-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="67475-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="67475-138">0x80000</span></span>  |
| <span data-ttu-id="67475-139">profundidad de DDSD \_</span><span class="sxs-lookup"><span data-stu-id="67475-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="67475-140">Obligatorio en una textura de profundidad.</span><span class="sxs-lookup"><span data-stu-id="67475-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="67475-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="67475-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="67475-142">Al escribir archivos. DDS, debe establecer las \_ marcas DDSD Caps y DDSD \_ PIXELFORMAT, y para las texturas de mipmapped, también debe establecer la marca DDSD \_ MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="67475-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="67475-143">Sin embargo, cuando se lee un archivo. DDS, no se debe confiar en las \_ marcas DDSD Cap, DDSD \_ PIXELFORMAT y DDSD \_ MIPMAPCOUNT que se establecen porque es posible que algunos escritores de este tipo de archivo no establezcan estas marcas.</span><span class="sxs-lookup"><span data-stu-id="67475-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="67475-144">La \_ marca de \_ textura de marcas de encabezado DDS \_ , que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSD caps, DDSD \_ height, DDSD \_ width y DDSD \_ PIXELFORMAT.</span><span class="sxs-lookup"><span data-stu-id="67475-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="67475-145">La \_ \_ \_ marca de MIPMAP de marcadores de encabezado de DDS, que se define en DDS. h, es igual a la \_ marca MIPMAPCOUNT de DDSD.</span><span class="sxs-lookup"><span data-stu-id="67475-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="67475-146">La \_ \_ \_ marca de volumen de marcas de encabezado DDS, que se define en DDS. h, es igual a la \_ marca de profundidad DDSD.</span><span class="sxs-lookup"><span data-stu-id="67475-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="67475-147">La \_ \_ \_ marca de paso de marcador de encabezado DDS, que se define en DDS. h, es igual a la marca de paso de DDSD \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="67475-148">La \_ marca LINEARSIZE de marcadores de encabezado DDS \_ \_ , que se define en DDS. h, es igual a la \_ marca LINEARSIZE de DDSD.</span><span class="sxs-lookup"><span data-stu-id="67475-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="67475-149">**dwHeight**</span><span class="sxs-lookup"><span data-stu-id="67475-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="67475-150">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-151">Alto de superficie (en píxeles).</span><span class="sxs-lookup"><span data-stu-id="67475-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="67475-152">**dwWidth**</span><span class="sxs-lookup"><span data-stu-id="67475-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="67475-153">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-154">Ancho de la superficie (en píxeles).</span><span class="sxs-lookup"><span data-stu-id="67475-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="67475-155">**dwPitchOrLinearSize**</span><span class="sxs-lookup"><span data-stu-id="67475-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="67475-156">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-157">El paso o el número de bytes por línea de examen en una textura sin comprimir; número total de bytes en la textura de nivel superior para una textura comprimida.</span><span class="sxs-lookup"><span data-stu-id="67475-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="67475-158">Para obtener información sobre cómo calcular el paso, consulte la sección sobre el diseño del archivo DDS de la [Guía de programación para DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="67475-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="67475-159">**dwDepth**</span><span class="sxs-lookup"><span data-stu-id="67475-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="67475-160">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-161">Profundidad de una textura de volumen (en píxeles), de lo contrario, sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="67475-162">**dwMipMapCount**</span><span class="sxs-lookup"><span data-stu-id="67475-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="67475-163">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-164">Número de niveles de mipmap, de lo contrario, sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="67475-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="67475-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="67475-166">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-167">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="67475-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="67475-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="67475-169">Tipo: **[ **\_ PIXELFORMAT de DDS**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="67475-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-170">El formato de píxel (consulte las letras de la [**DDS \_**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="67475-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="67475-171">**dwCaps**</span><span class="sxs-lookup"><span data-stu-id="67475-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="67475-172">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-173">Especifica la complejidad de las superficies almacenadas.</span><span class="sxs-lookup"><span data-stu-id="67475-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="67475-174">Marca</span><span class="sxs-lookup"><span data-stu-id="67475-174">Flag</span></span>             | <span data-ttu-id="67475-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="67475-175">Description</span></span>                                                                                                                              | <span data-ttu-id="67475-176">Value</span><span class="sxs-lookup"><span data-stu-id="67475-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="67475-177">\_complejo DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="67475-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="67475-178">Opta debe usarse en cualquier archivo que contenga más de una superficie (un mipmap, un mapa de entorno cúbico o una textura de volumen mipmapped).</span><span class="sxs-lookup"><span data-stu-id="67475-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="67475-179">0x8</span><span class="sxs-lookup"><span data-stu-id="67475-179">0x8</span></span>      |
| <span data-ttu-id="67475-180">\_MIPMAP DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="67475-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="67475-181">Opta debe utilizarse para un mipmap.</span><span class="sxs-lookup"><span data-stu-id="67475-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="67475-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="67475-182">0x400000</span></span> |
| <span data-ttu-id="67475-183">\_textura DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="67475-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="67475-184">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="67475-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="67475-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="67475-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="67475-186">Al escribir archivos. DDS, debe establecer la \_ marca de textura DDSCAPS y, en el caso de varias superficies, también debe establecer la \_ marca DDSCAPS Complex.</span><span class="sxs-lookup"><span data-stu-id="67475-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="67475-187">Sin embargo, al leer un archivo. DDS, no debe confiar en las marcas DDSCAPS \_ Texture y DDSCAPS \_ Complex que se establecen porque algunos escritores de este tipo de archivo podrían no establecer estas marcas.</span><span class="sxs-lookup"><span data-stu-id="67475-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="67475-188">La \_ marca del mipmap de marcas de la superficie DDS \_ \_ , que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas de mipmap complejo y DDSCAPS de DDSCAPS \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="67475-189">La \_ \_ \_ marca de textura de las marcas de la superficie DDS, que se define en DDS. h, es igual a la \_ marca de textura DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="67475-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="67475-190">La \_ marca DDS Surface \_ Flags \_ mapa, que se define en DDS. h, es igual a la \_ marca compleja DDSCAPS.</span><span class="sxs-lookup"><span data-stu-id="67475-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="67475-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="67475-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="67475-192">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-193">Detalles adicionales sobre las superficies almacenadas.</span><span class="sxs-lookup"><span data-stu-id="67475-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="67475-194">Marca</span><span class="sxs-lookup"><span data-stu-id="67475-194">Flag</span></span>                         | <span data-ttu-id="67475-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="67475-195">Description</span></span>                                            | <span data-ttu-id="67475-196">Value</span><span class="sxs-lookup"><span data-stu-id="67475-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="67475-197">DDSCAPS2 \_ mapa</span><span class="sxs-lookup"><span data-stu-id="67475-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="67475-198">Obligatorio para un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-198">Required for a cube map.</span></span>                               | <span data-ttu-id="67475-199">0x200</span><span class="sxs-lookup"><span data-stu-id="67475-199">0x200</span></span>    |
| <span data-ttu-id="67475-200">DDSCAPS2 \_ mapa \_ POSITIVEX</span><span class="sxs-lookup"><span data-stu-id="67475-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="67475-201">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-202">0x400</span><span class="sxs-lookup"><span data-stu-id="67475-202">0x400</span></span>    |
| <span data-ttu-id="67475-203">DDSCAPS2 \_ mapa \_ NEGATIVEX</span><span class="sxs-lookup"><span data-stu-id="67475-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="67475-204">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-205">0x800</span><span class="sxs-lookup"><span data-stu-id="67475-205">0x800</span></span>    |
| <span data-ttu-id="67475-206">DDSCAPS2 \_ mapa \_ positivo</span><span class="sxs-lookup"><span data-stu-id="67475-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="67475-207">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="67475-208">0x1000</span></span>   |
| <span data-ttu-id="67475-209">DDSCAPS2 \_ mapa \_ negativo</span><span class="sxs-lookup"><span data-stu-id="67475-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="67475-210">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="67475-211">0x2000</span></span>   |
| <span data-ttu-id="67475-212">DDSCAPS2 \_ mapa \_ POSITIVEZ</span><span class="sxs-lookup"><span data-stu-id="67475-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="67475-213">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="67475-214">0x4000</span></span>   |
| <span data-ttu-id="67475-215">DDSCAPS2 \_ mapa \_ NEGATIVEZ</span><span class="sxs-lookup"><span data-stu-id="67475-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="67475-216">Obligatorio cuando estas superficies están almacenadas en un mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="67475-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="67475-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="67475-217">0x8000</span></span>   |
| <span data-ttu-id="67475-218">\_Volumen DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="67475-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="67475-219">Obligatorio para una textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="67475-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="67475-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="67475-220">0x200000</span></span> |



 

<span data-ttu-id="67475-221">La \_ marca DDS mapa \_ POSITIVEX, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa POSITIVEX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="67475-222">La \_ marca DDS mapa \_ NEGATIVEX, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa NEGATIVEX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="67475-223">La \_ marca DDS mapa \_ positivo, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas mapa DDSCAPS2 y DDSCAPS2 \_ mapa \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="67475-224">La \_ marca DDS mapa \_ Negative, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 \_ mapa \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="67475-225">La \_ marca DDS mapa \_ POSITIVEZ, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa POSITIVEZ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="67475-226">La \_ marca DDS mapa \_ NEGATIVEZ, que se define en DDS. h, es una combinación OR bit a bit de las \_ marcas DDSCAPS2 mapa y DDSCAPS2 mapa NEGATIVEZ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67475-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="67475-227">La \_ marca DDS mapa \_ ALLFACES, que se define en DDS. h, es una combinación bit a bit de las \_ marcas DDS mapa \_ POSITIVEX, DDS \_ mapa \_ NEGATIVEX, DDS \_ mapa \_ positivo, DDS \_ mapa \_ negativo, DDS \_ mapa \_ POSITIVEZ y \_ \_ DDSCAPS2 mapa NEGATIVEZ.</span><span class="sxs-lookup"><span data-stu-id="67475-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="67475-228">La \_ marca de volumen de marcas DDS \_ , que se define en DDS. h, es igual a la \_ marca de volumen DDSCAPS2.</span><span class="sxs-lookup"><span data-stu-id="67475-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="67475-229">Aunque Direct3D 9 admite mapas de cubos parciales, Direct3D 10, 10,1 y 11 requieren que se definan las seis caras del mapa de cubos (es decir, se debe establecer DDS \_ mapa \_ ALLFACES).</span><span class="sxs-lookup"><span data-stu-id="67475-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="67475-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="67475-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="67475-231">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-232">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="67475-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="67475-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="67475-234">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-235">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="67475-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="67475-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="67475-237">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67475-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="67475-238">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="67475-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67475-239">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67475-239">Remarks</span></span>

<span data-ttu-id="67475-240">Incluir marcas en **dwFlags** para los miembros de la estructura que contienen datos válidos.</span><span class="sxs-lookup"><span data-stu-id="67475-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="67475-241">Use esta estructura en combinación con un [**\_ encabezado DDS \_ DXT10**](dds-header-dxt10.md) para almacenar una matriz de recursos en un archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="67475-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="67475-242">Para obtener más información, consulte [matrices de texturas](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="67475-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="67475-243">**DDS \_ El encabezado** es idéntico a la estructura DDSURFACEDESC2 de DirectDraw sin dependencias de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="67475-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="67475-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67475-244">Requirements</span></span>



| <span data-ttu-id="67475-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="67475-245">Requirement</span></span> | <span data-ttu-id="67475-246">Value</span><span class="sxs-lookup"><span data-stu-id="67475-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67475-247">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67475-247">Header</span></span><br/> | <dl> <span data-ttu-id="67475-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="67475-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67475-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="67475-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67475-250">Referencia de DDS</span><span class="sxs-lookup"><span data-stu-id="67475-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

