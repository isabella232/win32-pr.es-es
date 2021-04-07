---
description: Crea una textura a partir de un archivo en memoria. Esta es una función más avanzada que D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: Función D3DXCreateTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003824"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="c446b-104">D3DXCreateTextureFromFileInMemoryEx función)</span><span class="sxs-lookup"><span data-stu-id="c446b-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="c446b-105">Crea una textura a partir de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="c446b-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="c446b-106">Esta es una función más avanzada que [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c446b-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c446b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c446b-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c446b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c446b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c446b-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c446b-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c446b-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="c446b-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-114">Puntero al archivo en la memoria desde el que se va a crear la textura.</span><span class="sxs-lookup"><span data-stu-id="c446b-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-115">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-117">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c446b-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-118">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-120">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c446b-120">Width in pixels.</span></span> <span data-ttu-id="c446b-121">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="c446b-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-122">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-124">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c446b-124">Height, in pixels.</span></span> <span data-ttu-id="c446b-125">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="c446b-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-126">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-128">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="c446b-128">Number of mip levels requested.</span></span> <span data-ttu-id="c446b-129">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="c446b-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-130">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-132">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="c446b-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="c446b-133">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="c446b-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="c446b-134">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="c446b-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="c446b-135">Si \_ se especifica D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="c446b-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="c446b-136">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="c446b-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="c446b-137">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-138">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="c446b-139">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="c446b-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="c446b-140">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="c446b-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="c446b-141">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="c446b-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="c446b-142">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="c446b-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="c446b-143">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c446b-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-144">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-145">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="c446b-146">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="c446b-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-147">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-148">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-149">Combinación de una o varias marcas que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="c446b-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="c446b-150">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c446b-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="c446b-151">Cada filtro válido debe contener una de las marcas en [el \_ filtro de D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c446b-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="c446b-152">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c446b-154">Combinación de una o varias marcas que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="c446b-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="c446b-155">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c446b-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="c446b-156">Cada filtro válido debe contener una de las marcas en [el \_ filtro de D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c446b-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="c446b-157">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="c446b-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-158">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c446b-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-159">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="c446b-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="c446b-160">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="c446b-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="c446b-161">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="c446b-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="c446b-162">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="c446b-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="c446b-163">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="c446b-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-164">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c446b-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-165">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c446b-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="c446b-166">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="c446b-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-167">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c446b-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-168">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="c446b-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c446b-169">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="c446b-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="c446b-170">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c446b-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c446b-171">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c446b-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c446b-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="c446b-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="c446b-173">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="c446b-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c446b-174">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c446b-174">Return value</span></span>

<span data-ttu-id="c446b-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c446b-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c446b-176">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c446b-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c446b-177">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c446b-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c446b-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c446b-178">Remarks</span></span>

<span data-ttu-id="c446b-179">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="c446b-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c446b-180">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="c446b-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c446b-181">Para obtener más información sobre [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vea Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="c446b-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="c446b-182">Tenga en cuenta que, a partir de DirectX 8,0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c446b-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="c446b-183">El miembro peFlags es ahora el canal alfa para formatos de paleta de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c446b-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="c446b-184">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="c446b-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="c446b-185">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="c446b-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c446b-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c446b-186">Requirements</span></span>



| <span data-ttu-id="c446b-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="c446b-187">Requirement</span></span> | <span data-ttu-id="c446b-188">Value</span><span class="sxs-lookup"><span data-stu-id="c446b-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c446b-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c446b-189">Header</span></span><br/>  | <dl> <span data-ttu-id="c446b-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c446b-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c446b-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c446b-191">Library</span></span><br/> | <dl> <span data-ttu-id="c446b-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c446b-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c446b-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="c446b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c446b-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="c446b-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="c446b-195">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c446b-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
