---
title: Estructura de DDS_PIXELFORMAT (DDS. h)
description: Formato de píxel de la superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- Estructura de DDS_PIXELFORMAT DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717623"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="94d36-104">Estructura de PIXELFORMAT de DDS \_</span><span class="sxs-lookup"><span data-stu-id="94d36-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="94d36-105">Formato de píxel de la superficie.</span><span class="sxs-lookup"><span data-stu-id="94d36-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d36-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94d36-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="94d36-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="94d36-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="94d36-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="94d36-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-110">Tamaño de la estructura; establézcalo en 32 (bytes).</span><span class="sxs-lookup"><span data-stu-id="94d36-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="94d36-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="94d36-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-112">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-113">Valores que indican qué tipo de datos se encuentra en la superficie.</span><span class="sxs-lookup"><span data-stu-id="94d36-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="94d36-114">Marca</span><span class="sxs-lookup"><span data-stu-id="94d36-114">Flag</span></span>              | <span data-ttu-id="94d36-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="94d36-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="94d36-116">Value</span><span class="sxs-lookup"><span data-stu-id="94d36-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="94d36-117">DDPF \_ ALPHAPIXELS</span><span class="sxs-lookup"><span data-stu-id="94d36-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="94d36-118">La textura contiene datos alfa; **dwRGBAlphaBitMask** contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="94d36-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="94d36-119">0x1</span><span class="sxs-lookup"><span data-stu-id="94d36-119">0x1</span></span>     |
| <span data-ttu-id="94d36-120">\_alfa DDPF</span><span class="sxs-lookup"><span data-stu-id="94d36-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="94d36-121">Se usa en algunos archivos DDS más antiguos para el canal alfa solo datos sin comprimir (dwRGBBitCount contiene el canal alfa bitCount; dwABitMask contiene datos válidos)</span><span class="sxs-lookup"><span data-stu-id="94d36-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="94d36-122">0x2</span><span class="sxs-lookup"><span data-stu-id="94d36-122">0x2</span></span>     |
| <span data-ttu-id="94d36-123">\_FourCC DDPF</span><span class="sxs-lookup"><span data-stu-id="94d36-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="94d36-124">La textura contiene datos RGB comprimidos; **dwFourCC** contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="94d36-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="94d36-125">0x4</span><span class="sxs-lookup"><span data-stu-id="94d36-125">0x4</span></span>     |
| <span data-ttu-id="94d36-126">DDPF \_ RGB</span><span class="sxs-lookup"><span data-stu-id="94d36-126">DDPF\_RGB</span></span>         | <span data-ttu-id="94d36-127">La textura contiene datos RGB sin comprimir; **dwRGBBitCount** y las máscaras RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contienen datos válidos.</span><span class="sxs-lookup"><span data-stu-id="94d36-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="94d36-128">0x40</span><span class="sxs-lookup"><span data-stu-id="94d36-128">0x40</span></span>    |
| <span data-ttu-id="94d36-129">DDPF \_ YUV</span><span class="sxs-lookup"><span data-stu-id="94d36-129">DDPF\_YUV</span></span>         | <span data-ttu-id="94d36-130">Se usa en algunos archivos DDS más antiguos para datos YUV sin comprimir (dwRGBBitCount contiene el número de bits YUV; dwRBitMask contiene la máscara Y, dwGBitMask contiene la máscara U, dwBBitMask contiene la máscara V)</span><span class="sxs-lookup"><span data-stu-id="94d36-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="94d36-131">0x200</span><span class="sxs-lookup"><span data-stu-id="94d36-131">0x200</span></span>   |
| <span data-ttu-id="94d36-132">\_luminancia DDPF</span><span class="sxs-lookup"><span data-stu-id="94d36-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="94d36-133">Se usa en algunos archivos DDS más antiguos para los datos sin comprimir de color de canal único (dwRGBBitCount contiene el número de bits de canal de luminancia; dwRBitMask contiene la máscara de canal).</span><span class="sxs-lookup"><span data-stu-id="94d36-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="94d36-134">Se puede combinar con DDPF \_ ALPHAPIXELS para un archivo DDS de dos canales.</span><span class="sxs-lookup"><span data-stu-id="94d36-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="94d36-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="94d36-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="94d36-136">**dwFourCC**</span><span class="sxs-lookup"><span data-stu-id="94d36-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-137">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-138">Códigos de cuatro caracteres para especificar formatos comprimidos o personalizados.</span><span class="sxs-lookup"><span data-stu-id="94d36-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="94d36-139">Los valores posibles son: *DXT1*, *DXT2*, *DXT3*, *DXT4* o *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="94d36-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="94d36-140">Un elemento FourCC de contenido DX10 indica el prescense del [**encabezado \_ DDS \_ DXT10**](dds-header-dxt10.md) el encabezado extendido y el miembro dxgiFormat de esa estructura indica el formato verdadero.</span><span class="sxs-lookup"><span data-stu-id="94d36-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="94d36-141">Cuando se usa un código de cuatro caracteres, dwFlags debe incluir *DDPF \_ FourCC*.</span><span class="sxs-lookup"><span data-stu-id="94d36-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="94d36-142">**dwRGBBitCount**</span><span class="sxs-lookup"><span data-stu-id="94d36-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-143">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-144">Número de bits en un formato RGB (posiblemente incluido alfa).</span><span class="sxs-lookup"><span data-stu-id="94d36-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="94d36-145">Válido cuando **dwFlags** incluye *DDPF \_ RGB*, *\_ luminancia DDPF* o *DDPF \_ YUV*.</span><span class="sxs-lookup"><span data-stu-id="94d36-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="94d36-146">**dwRBitMask**</span><span class="sxs-lookup"><span data-stu-id="94d36-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-147">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-148">Máscara roja (o lumiannce o Y) para leer los datos de color.</span><span class="sxs-lookup"><span data-stu-id="94d36-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="94d36-149">Por ejemplo, dado el formato A8R8G8B8, la máscara roja sería 0x00ff0000.</span><span class="sxs-lookup"><span data-stu-id="94d36-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="94d36-150">**dwGBitMask**</span><span class="sxs-lookup"><span data-stu-id="94d36-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-151">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-152">Máscara verde (o U) para leer los datos de color.</span><span class="sxs-lookup"><span data-stu-id="94d36-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="94d36-153">Por ejemplo, dado el formato A8R8G8B8, la máscara verde sería 0x0000ff00.</span><span class="sxs-lookup"><span data-stu-id="94d36-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="94d36-154">**dwBBitMask**</span><span class="sxs-lookup"><span data-stu-id="94d36-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-155">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-156">Máscara azul (o V) para leer los datos de color.</span><span class="sxs-lookup"><span data-stu-id="94d36-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="94d36-157">Por ejemplo, dado el formato A8R8G8B8, la máscara azul sería 0x000000ff.</span><span class="sxs-lookup"><span data-stu-id="94d36-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="94d36-158">**dwABitMask**</span><span class="sxs-lookup"><span data-stu-id="94d36-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="94d36-159">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="94d36-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="94d36-160">Máscara alfa para leer datos alfa.</span><span class="sxs-lookup"><span data-stu-id="94d36-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="94d36-161">dwFlags debe incluir *DDPF \_ ALPHAPIXELS* o *DDPF \_ Alpha*.</span><span class="sxs-lookup"><span data-stu-id="94d36-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="94d36-162">Por ejemplo, dado el formato A8R8G8B8, la máscara alfa sería 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="94d36-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94d36-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94d36-163">Remarks</span></span>

<span data-ttu-id="94d36-164">Para almacenar formatos de DXGI como datos de punto flotante, use un valor de **dwFlags** de DDPF \_ FourCC y establezca **dwFourCC** en ' d ', ' X ', ' 1 ', ' 0 '.</span><span class="sxs-lookup"><span data-stu-id="94d36-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="94d36-165">Use el encabezado de extensión [**DDS \_ Header \_ DXT10**](dds-header-dxt10.md) para almacenar el formato de DXGI en el miembro **dxgiFormat** .</span><span class="sxs-lookup"><span data-stu-id="94d36-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="94d36-166">Tenga en cuenta que hay variantes no estándar de archivos DDS donde **dwFlags** tiene DDPF \_ FourCC y el valor **dwFourCC** se establece directamente en un valor de enumeración de formato D3DFORMAT o DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="94d36-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="94d36-167">No es posible eliminar la ambigüedad de los valores de formato de D3DFORMAT frente a DXGI \_ mediante este esquema no estándar, por lo que se recomienda el encabezado de extensión contenido DX10 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="94d36-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d36-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d36-168">Requirements</span></span>



| <span data-ttu-id="94d36-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d36-169">Requirement</span></span> | <span data-ttu-id="94d36-170">Value</span><span class="sxs-lookup"><span data-stu-id="94d36-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="94d36-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94d36-171">Header</span></span><br/> | <dl> <span data-ttu-id="94d36-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d36-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d36-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="94d36-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d36-174">Referencia de DDS</span><span class="sxs-lookup"><span data-stu-id="94d36-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

