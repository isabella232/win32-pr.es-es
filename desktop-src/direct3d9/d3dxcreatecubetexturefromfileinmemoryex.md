---
description: Crea una textura de cubo a partir de un archivo en memoria. Esta es una función más avanzada que D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Función D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083790"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="a9bc0-104">D3DXCreateCubeTextureFromFileInMemoryEx función)</span><span class="sxs-lookup"><span data-stu-id="a9bc0-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="a9bc0-105">Crea una textura de cubo a partir de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="a9bc0-106">Esta es una función más avanzada que [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9bc0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9bc0-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a9bc0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9bc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9bc0-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a9bc0-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-114">Puntero al archivo en la memoria desde el que se va a crear la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="a9bc0-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-116">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-118">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-119">*Tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-121">Ancho (o alto) en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-121">Width (or height) in pixels.</span></span> <span data-ttu-id="a9bc0-122">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-123">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-125">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-125">Number of mip levels requested.</span></span> <span data-ttu-id="a9bc0-126">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-127">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-129">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="a9bc0-130">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="a9bc0-131">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a9bc0-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a9bc0-132">Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="a9bc0-133">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-134">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-135">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="a9bc0-136">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="a9bc0-137">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="a9bc0-138">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="a9bc0-139">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="a9bc0-140">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-141">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-142">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="a9bc0-143">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-144">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-146">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="a9bc0-147">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a9bc0-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-148">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9bc0-150">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="a9bc0-151">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a9bc0-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="a9bc0-152">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-153">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-154">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a9bc0-155">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a9bc0-156">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a9bc0-157">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a9bc0-158">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-159">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-160">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9bc0-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a9bc0-161">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-162">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-163">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="a9bc0-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a9bc0-164">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="a9bc0-165">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a9bc0-166">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9bc0-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9bc0-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="a9bc0-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="a9bc0-168">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9bc0-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9bc0-169">Return value</span></span>

<span data-ttu-id="a9bc0-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9bc0-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9bc0-171">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9bc0-172">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bc0-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9bc0-173">Remarks</span></span>

<span data-ttu-id="a9bc0-174">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a9bc0-175">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a9bc0-176">Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="a9bc0-177">Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="a9bc0-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="a9bc0-178">Este método se ha diseñado para que se use para cargar archivos de imagen almacenados como RT \_ RCDATA, que es un recurso definido por la aplicación (datos sin procesar).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="a9bc0-179">De lo contrario, se producirá un error en este método.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="a9bc0-180">Para obtener más información sobre [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="a9bc0-181">Tenga en cuenta que, a partir de DirectX 8,0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="a9bc0-182">El miembro peFlags es ahora el canal alfa para formatos de paleta de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="a9bc0-183">**D3DXCreateCubeTextureFromFileInMemoryEx** usa el formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="a9bc0-184">El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="a9bc0-185">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="a9bc0-186">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="a9bc0-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="a9bc0-187">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="a9bc0-188">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="a9bc0-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bc0-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9bc0-189">Requirements</span></span>



| <span data-ttu-id="a9bc0-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9bc0-190">Requirement</span></span> | <span data-ttu-id="a9bc0-191">Value</span><span class="sxs-lookup"><span data-stu-id="a9bc0-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bc0-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9bc0-192">Header</span></span><br/>  | <dl> <span data-ttu-id="a9bc0-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc0-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a9bc0-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9bc0-194">Library</span></span><br/> | <dl> <span data-ttu-id="a9bc0-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9bc0-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a9bc0-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9bc0-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bc0-197">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a9bc0-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
