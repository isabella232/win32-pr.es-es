---
description: 'Función D3DXCreateVolumeTextureFromFileEx: crea una textura de volumen a partir de un archivo.'
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Función D3DXCreateVolumeTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11be9da24be7fc9a03bab8e761e55a601715bd75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102753"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="7cc49-103">Función D3DXCreateVolumeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="7cc49-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="7cc49-104">Crea una textura de volumen a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cc49-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="7cc49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cc49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc49-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7cc49-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="7cc49-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-110">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-112">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="7cc49-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="7cc49-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7cc49-114">De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="7cc49-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="7cc49-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7cc49-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-116">*Ancho* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-118">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7cc49-118">Width in pixels.</span></span> <span data-ttu-id="7cc49-119">Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7cc49-120">La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="7cc49-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-121">*Alto* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-122">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-123">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7cc49-123">Height, in pixels.</span></span> <span data-ttu-id="7cc49-124">Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7cc49-125">La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="7cc49-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-126">*Profundidad* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-127">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-128">Profundidad, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7cc49-128">Depth, in pixels.</span></span> <span data-ttu-id="7cc49-129">Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="7cc49-130">La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="7cc49-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-131">*MipLevels* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-133">Número de niveles de mip solicitados.</span><span class="sxs-lookup"><span data-stu-id="7cc49-133">Number of mip levels requested.</span></span> <span data-ttu-id="7cc49-134">Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mip completa.</span><span class="sxs-lookup"><span data-stu-id="7cc49-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-135">*Uso* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-137">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="7cc49-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="7cc49-138">Establecer esta marca en D3DUSAGE RENDERTARGET indica que la superficie se \_ va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="7cc49-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="7cc49-139">A continuación, el recurso se puede pasar al *parámetro pNewRenderTarget* del [**método SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)</span><span class="sxs-lookup"><span data-stu-id="7cc49-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="7cc49-140">Si se especifica D3DUSAGE RENDERTARGET o D3DUSAGE DYNAMIC, pool debe establecerse en D3DPOOL DEFAULT y la aplicación debe comprobar que el dispositivo admite esta operación mediante una llamada a \_ \_  \_ [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="7cc49-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="7cc49-141">D3DUSAGE \_ DYNAMIC indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="7cc49-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="7cc49-142">Para obtener más información sobre el uso de texturas dinámicas, vea [Usar texturas dinámicas.](performance-optimizations.md)</span><span class="sxs-lookup"><span data-stu-id="7cc49-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-143">*Format*</span><span class="sxs-lookup"><span data-stu-id="7cc49-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc49-144">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="7cc49-145">Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="7cc49-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="7cc49-146">La textura devuelta puede tener un formato diferente del especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="7cc49-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="7cc49-147">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="7cc49-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="7cc49-148">Si [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="7cc49-149">Si D3DFMT FROM FILE, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cc49-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-150">*Grupo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-151">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="7cc49-152">Miembro del tipo [**enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="7cc49-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-153">*Filtro* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-155">Combinación de uno o varios filtros [D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="7cc49-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7cc49-156">Especificar D3DX DEFAULT para este parámetro equivale a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="7cc49-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-157">*MipFilter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-158">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cc49-159">Combinación de uno o varios filtros [D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="7cc49-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7cc49-160">Especificar D3DX \_ DEFAULT para este parámetro equivale a especificar D3DX FILTER \_ \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="7cc49-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="7cc49-161">Además, use los bits 27-31 para especificar el número de niveles de mip que se omitirán (desde la parte superior de la cadena mipmap) cuando se cargue una textura .dds en la memoria; esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="7cc49-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-162">*ColorKey* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-163">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7cc49-164">[**Valor D3DCOLOR que**](d3dcolor.md) se reemplazará por negro transparente o 0 para deshabilitar la clave de color.</span><span class="sxs-lookup"><span data-stu-id="7cc49-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7cc49-165">Siempre es un color ARGB de 32 bits, independientemente del formato de imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="7cc49-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7cc49-166">Alfa es significativo y normalmente debe establecerse en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="7cc49-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7cc49-167">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="7cc49-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-168">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-169">Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7cc49-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="7cc49-170">Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7cc49-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-171">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-172">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="7cc49-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7cc49-173">Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se rellenará, o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7cc49-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7cc49-174">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7cc49-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc49-175">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7cc49-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="7cc49-176">Dirección de un puntero a una [**interfaz IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="7cc49-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cc49-177">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cc49-177">Return value</span></span>

<span data-ttu-id="7cc49-178">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7cc49-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7cc49-179">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7cc49-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7cc49-180">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7cc49-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc49-181">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cc49-181">Remarks</span></span>

<span data-ttu-id="7cc49-182">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="7cc49-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7cc49-183">Si se define Unicode, la llamada a la función se resuelve en D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="7cc49-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="7cc49-184">De lo contrario, la llamada de función se resuelve en D3DXCreateVolumeTextureFromFileExA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="7cc49-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="7cc49-185">Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga.</span><span class="sxs-lookup"><span data-stu-id="7cc49-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7cc49-186">Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7cc49-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7cc49-187">Las texturas mipmapped rellenan automáticamente cada nivel con la textura de volumen cargada.</span><span class="sxs-lookup"><span data-stu-id="7cc49-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="7cc49-188">Al cargar imágenes en texturas mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="7cc49-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="7cc49-189">Si esto sucede, las imágenes deben cargarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="7cc49-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="7cc49-190">Al omitir los niveles de asignación mip al cargar un archivo .dds, use la macro D3DX SKIP DDS MIP LEVELS para generar el \_ \_ valor de \_ \_ *MipFilter.*</span><span class="sxs-lookup"><span data-stu-id="7cc49-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="7cc49-191">Esta macro toma el número de niveles que se omitirán y el tipo de filtro y devuelve el valor del filtro, que se pasará al *parámetro MipFilter.*</span><span class="sxs-lookup"><span data-stu-id="7cc49-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc49-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cc49-192">Requirements</span></span>



| <span data-ttu-id="7cc49-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cc49-193">Requirement</span></span> | <span data-ttu-id="7cc49-194">Value</span><span class="sxs-lookup"><span data-stu-id="7cc49-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc49-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cc49-195">Header</span></span><br/>  | <dl> <span data-ttu-id="7cc49-196"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="7cc49-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7cc49-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cc49-197">Library</span></span><br/> | <dl> <span data-ttu-id="7cc49-198"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cc49-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7cc49-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7cc49-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc49-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="7cc49-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="7cc49-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="7cc49-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="7cc49-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="7cc49-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="7cc49-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="7cc49-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="7cc49-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="7cc49-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="7cc49-205">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7cc49-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
