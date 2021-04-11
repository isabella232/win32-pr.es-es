---
description: Crea una textura de cubo a partir de un recurso especificado por una cadena. Esta es una función más avanzada que D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Función D3DXCreateCubeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362734"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="af239-104">D3DXCreateCubeTextureFromResourceEx función)</span><span class="sxs-lookup"><span data-stu-id="af239-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="af239-105">Crea una textura de cubo a partir de un recurso especificado por una cadena.</span><span class="sxs-lookup"><span data-stu-id="af239-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="af239-106">Esta es una función más avanzada que [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="af239-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="af239-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af239-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="af239-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af239-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="af239-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="af239-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="af239-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="af239-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-114">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="af239-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="af239-115">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-117">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="af239-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="af239-118">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="af239-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="af239-119">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="af239-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="af239-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="af239-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="af239-121">*Tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="af239-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-123">Ancho y alto de la textura del cubo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="af239-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="af239-124">Por ejemplo, si la textura del cubo es un cubo de 8 píxeles por 8 píxeles, el valor de este parámetro debe ser 8.</span><span class="sxs-lookup"><span data-stu-id="af239-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="af239-125">Si este valor es 0 o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="af239-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="af239-126">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-128">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="af239-128">Number of mip levels requested.</span></span> <span data-ttu-id="af239-129">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="af239-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="af239-130">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="af239-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-132">0 o D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="af239-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="af239-133">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="af239-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="af239-134">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="af239-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="af239-135">Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="af239-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="af239-136">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="af239-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="af239-137">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="af239-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="af239-138">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-139">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="af239-140">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="af239-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="af239-141">La textura del cubo devuelto puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="af239-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="af239-142">Las aplicaciones deben comprobar el formato de la textura del cubo devuelta.</span><span class="sxs-lookup"><span data-stu-id="af239-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="af239-143">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="af239-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="af239-144">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af239-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="af239-145">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="af239-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-146">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="af239-147">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="af239-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="af239-148">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="af239-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-150">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="af239-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="af239-151">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="af239-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="af239-152">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af239-154">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="af239-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="af239-155">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="af239-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="af239-156">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af239-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-157">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="af239-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="af239-158">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="af239-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="af239-159">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="af239-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="af239-160">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="af239-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="af239-161">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="af239-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="af239-162">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="af239-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-163">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="af239-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="af239-164">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="af239-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="af239-165">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af239-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-166">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="af239-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="af239-167">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="af239-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="af239-168">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af239-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af239-169">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="af239-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="af239-170">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="af239-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af239-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af239-171">Return value</span></span>

<span data-ttu-id="af239-172">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af239-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af239-173">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af239-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af239-174">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="af239-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="af239-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af239-175">Remarks</span></span>

<span data-ttu-id="af239-176">La configuración del compilador determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="af239-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="af239-177">Si se define Unicode, la llamada de función se resuelve como **D3DXCreateCubeTextureFromResourceExW**.</span><span class="sxs-lookup"><span data-stu-id="af239-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="af239-178">De lo contrario, la llamada de función se resuelve como **D3DXCreateCubeTextureFromResourceExA** porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="af239-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="af239-179">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="af239-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="af239-180">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="af239-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="af239-181">Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.</span><span class="sxs-lookup"><span data-stu-id="af239-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="af239-182">Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="af239-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="af239-183">**D3DXCreateCubeTextureFromResourceEx** usa el formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="af239-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="af239-184">El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="af239-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="af239-185">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="af239-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="af239-186">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="af239-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af239-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af239-187">Requirements</span></span>



| <span data-ttu-id="af239-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="af239-188">Requirement</span></span> | <span data-ttu-id="af239-189">Value</span><span class="sxs-lookup"><span data-stu-id="af239-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af239-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af239-190">Header</span></span><br/>  | <dl> <span data-ttu-id="af239-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="af239-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="af239-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af239-192">Library</span></span><br/> | <dl> <span data-ttu-id="af239-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af239-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="af239-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="af239-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af239-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="af239-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="af239-196">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="af239-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
