---
description: Crea una textura de cubo a partir de un archivo. Esta es una función más avanzada que D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: Función D3DXCreateCubeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721539"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="6a60f-104">D3DXCreateCubeTextureFromFileEx función)</span><span class="sxs-lookup"><span data-stu-id="6a60f-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="6a60f-105">Crea una textura de cubo a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="6a60f-106">Esta es una función más avanzada que [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="6a60f-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a60f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a60f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6a60f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a60f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a60f-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a60f-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-112">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-114">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="6a60f-115">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6a60f-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6a60f-116">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6a60f-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6a60f-117">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6a60f-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-118">*Tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-120">Ancho y alto de la textura del cubo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6a60f-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="6a60f-121">Por ejemplo, si la textura del cubo es un cubo de 8 píxeles por 8 píxeles, el valor de este parámetro debe ser 8.</span><span class="sxs-lookup"><span data-stu-id="6a60f-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="6a60f-122">Si este valor es 0 o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-123">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-125">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="6a60f-125">Number of mip levels requested.</span></span> <span data-ttu-id="6a60f-126">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="6a60f-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-127">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-129">0 o D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="6a60f-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="6a60f-130">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="6a60f-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="6a60f-131">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="6a60f-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="6a60f-132">Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="6a60f-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="6a60f-133">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="6a60f-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="6a60f-134">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="6a60f-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-135">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-136">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6a60f-137">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="6a60f-138">La textura del cubo devuelto puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="6a60f-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="6a60f-139">Las aplicaciones deben comprobar el formato de la textura del cubo devuelta.</span><span class="sxs-lookup"><span data-stu-id="6a60f-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="6a60f-140">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="6a60f-141">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-142">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="6a60f-144">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="6a60f-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-145">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-146">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-147">Combinación de una o varias constantes [de \_ filtro de D3DX](d3dx-filter.md) , que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="6a60f-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="6a60f-148">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6a60f-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-149">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-150">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a60f-151">Combinación de una o varias constantes [de \_ filtro de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="6a60f-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="6a60f-152">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6a60f-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="6a60f-153">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="6a60f-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-154">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-155">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6a60f-156">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="6a60f-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="6a60f-157">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="6a60f-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="6a60f-158">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="6a60f-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="6a60f-159">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="6a60f-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-160">*pSrcInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-161">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a60f-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6a60f-162">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="6a60f-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-163">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-164">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="6a60f-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6a60f-165">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="6a60f-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a60f-166">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6a60f-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a60f-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6a60f-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="6a60f-168">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="6a60f-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a60f-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a60f-169">Return value</span></span>

<span data-ttu-id="6a60f-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a60f-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a60f-171">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a60f-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a60f-172">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6a60f-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a60f-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a60f-173">Remarks</span></span>

<span data-ttu-id="6a60f-174">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="6a60f-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6a60f-175">Si se define Unicode, la llamada de función se resuelve como **D3DXCreateCubeTextureFromFileExW**.</span><span class="sxs-lookup"><span data-stu-id="6a60f-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="6a60f-176">De lo contrario, la llamada de función se resuelve como **D3DXCreateCubeTextureFromFileExA** porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="6a60f-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="6a60f-177">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="6a60f-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="6a60f-178">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="6a60f-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="6a60f-179">Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.</span><span class="sxs-lookup"><span data-stu-id="6a60f-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="6a60f-180">Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="6a60f-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="6a60f-181">**D3DXCreateCubeTextureFromFileEx** usa el formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="6a60f-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="6a60f-182">El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="6a60f-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="6a60f-183">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="6a60f-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="6a60f-184">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="6a60f-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="6a60f-185">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="6a60f-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="6a60f-186">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="6a60f-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a60f-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a60f-187">Requirements</span></span>



| <span data-ttu-id="6a60f-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a60f-188">Requirement</span></span> | <span data-ttu-id="6a60f-189">Value</span><span class="sxs-lookup"><span data-stu-id="6a60f-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a60f-190">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a60f-190">Header</span></span><br/>  | <dl> <span data-ttu-id="6a60f-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a60f-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6a60f-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a60f-192">Library</span></span><br/> | <dl> <span data-ttu-id="6a60f-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a60f-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6a60f-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a60f-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a60f-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="6a60f-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="6a60f-196">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6a60f-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
