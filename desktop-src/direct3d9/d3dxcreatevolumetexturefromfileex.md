---
description: Crea una textura de volumen a partir de un archivo.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Función D3DXCreateVolumeTextureFromFileEx (D3dx9tex. h)
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
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362579"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="ab883-103">D3DXCreateVolumeTextureFromFileEx función)</span><span class="sxs-lookup"><span data-stu-id="ab883-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="ab883-104">Crea una textura de volumen a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab883-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab883-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ab883-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab883-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ab883-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ab883-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="ab883-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-112">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ab883-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ab883-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ab883-114">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ab883-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ab883-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ab883-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-116">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-118">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab883-118">Width in pixels.</span></span> <span data-ttu-id="ab883-119">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ab883-120">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ab883-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ab883-121">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-123">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab883-123">Height, in pixels.</span></span> <span data-ttu-id="ab883-124">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ab883-125">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ab883-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ab883-126">*Nivel de detalle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-128">Profundidad, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ab883-128">Depth, in pixels.</span></span> <span data-ttu-id="ab883-129">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ab883-130">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ab883-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ab883-131">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-133">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="ab883-133">Number of mip levels requested.</span></span> <span data-ttu-id="ab883-134">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="ab883-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-135">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-137">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="ab883-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ab883-138">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ab883-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ab883-139">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="ab883-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="ab883-140">Si \_ se especifica D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ab883-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ab883-141">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ab883-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="ab883-142">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ab883-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab883-143">*Format*</span><span class="sxs-lookup"><span data-stu-id="ab883-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="ab883-144">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ab883-145">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="ab883-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="ab883-146">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="ab883-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ab883-147">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="ab883-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="ab883-148">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ab883-149">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab883-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-150">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-151">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ab883-152">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="ab883-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-153">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-155">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="ab883-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ab883-156">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab883-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-157">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-158">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab883-159">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="ab883-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ab883-160">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab883-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="ab883-161">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="ab883-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-162">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab883-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-163">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ab883-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ab883-164">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="ab883-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ab883-165">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="ab883-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ab883-166">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="ab883-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ab883-167">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ab883-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-168">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab883-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-169">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab883-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ab883-170">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="ab883-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-171">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab883-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-172">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ab883-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ab883-173">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="ab883-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab883-174">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab883-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab883-175">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ab883-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ab883-176">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="ab883-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab883-177">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab883-177">Return value</span></span>

<span data-ttu-id="ab883-178">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab883-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab883-179">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab883-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab883-180">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab883-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab883-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab883-181">Remarks</span></span>

<span data-ttu-id="ab883-182">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="ab883-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ab883-183">Si se define Unicode, la llamada de función se resuelve como D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="ab883-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="ab883-184">De lo contrario, la llamada de función se resuelve como D3DXCreateVolumeTextureFromFileExA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="ab883-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="ab883-185">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="ab883-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ab883-186">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ab883-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ab883-187">Las texturas de Mipmapped automáticamente tienen cada nivel rellenado con la textura de volumen cargada.</span><span class="sxs-lookup"><span data-stu-id="ab883-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="ab883-188">Al cargar imágenes en texturas de mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="ab883-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="ab883-189">Si esto ocurre, las imágenes deben cargarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="ab883-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="ab883-190">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="ab883-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="ab883-191">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="ab883-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab883-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab883-192">Requirements</span></span>



| <span data-ttu-id="ab883-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab883-193">Requirement</span></span> | <span data-ttu-id="ab883-194">Value</span><span class="sxs-lookup"><span data-stu-id="ab883-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab883-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab883-195">Header</span></span><br/>  | <dl> <span data-ttu-id="ab883-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab883-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ab883-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab883-197">Library</span></span><br/> | <dl> <span data-ttu-id="ab883-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab883-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ab883-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab883-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab883-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="ab883-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="ab883-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ab883-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ab883-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ab883-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="ab883-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="ab883-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="ab883-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="ab883-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="ab883-205">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ab883-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
