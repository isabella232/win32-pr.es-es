---
description: Crea una textura a partir de un recurso. Esta es una función más avanzada que D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: Función D3DXCreateTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547910"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="ea542-104">D3DXCreateTextureFromResourceEx función)</span><span class="sxs-lookup"><span data-stu-id="ea542-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="ea542-105">Crea una textura a partir de un recurso.</span><span class="sxs-lookup"><span data-stu-id="ea542-105">Creates a texture from a resource.</span></span> <span data-ttu-id="ea542-106">Esta es una función más avanzada que [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="ea542-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea542-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea542-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="ea542-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea542-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea542-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ea542-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ea542-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="ea542-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-114">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ea542-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-115">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-117">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="ea542-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="ea542-118">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea542-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ea542-119">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ea542-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ea542-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ea542-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-121">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-123">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ea542-123">Width in pixels.</span></span> <span data-ttu-id="ea542-124">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="ea542-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-125">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-127">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ea542-127">Height, in pixels.</span></span> <span data-ttu-id="ea542-128">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="ea542-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-129">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-131">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="ea542-131">Number of mip levels requested.</span></span> <span data-ttu-id="ea542-132">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="ea542-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-133">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-135">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="ea542-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ea542-136">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ea542-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ea542-137">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ea542-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ea542-138">Si \_ se especifica D3DUSAGE RENDERTARGET o D3DUSAGE, el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ea542-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ea542-139">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ea542-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="ea542-140">Para obtener más información sobre el uso de texturas dinámicas, vea [optimizaciones de rendimiento (Direct3D 9)](performance-optimizations.md)mediante texturas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="ea542-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-141">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ea542-143">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="ea542-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="ea542-144">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="ea542-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ea542-145">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="ea542-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="ea542-146">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="ea542-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ea542-147">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea542-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-148">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ea542-150">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="ea542-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-151">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-153">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="ea542-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ea542-154">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ea542-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-155">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea542-157">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="ea542-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ea542-158">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ea542-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-159">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea542-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-160">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ea542-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ea542-161">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="ea542-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ea542-162">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="ea542-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ea542-163">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="ea542-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ea542-164">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ea542-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-165">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ea542-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-166">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea542-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ea542-167">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="ea542-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-168">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ea542-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-169">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ea542-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ea542-170">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="ea542-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ea542-171">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ea542-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea542-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ea542-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="ea542-173">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="ea542-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea542-174">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea542-174">Return value</span></span>

<span data-ttu-id="ea542-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea542-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea542-176">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea542-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea542-177">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ea542-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea542-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea542-178">Remarks</span></span>

<span data-ttu-id="ea542-179">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="ea542-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ea542-180">Si se define Unicode, la llamada de función se resuelve como D3DXCreateTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="ea542-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="ea542-181">De lo contrario, la llamada de función se resuelve como D3DXCreateTextureFromResourceExA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea542-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="ea542-182">El recurso que se está cargando debe ser de tipo RT \_ Bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="ea542-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="ea542-183">El tipo de recurso RT \_ RCDATA se usa para cargar formatos distintos de los mapas de bits (como. TGA,. jpg y. DDS).</span><span class="sxs-lookup"><span data-stu-id="ea542-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="ea542-184">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="ea542-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ea542-185">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ea542-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea542-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea542-186">Requirements</span></span>



| <span data-ttu-id="ea542-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea542-187">Requirement</span></span> | <span data-ttu-id="ea542-188">Value</span><span class="sxs-lookup"><span data-stu-id="ea542-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea542-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea542-189">Header</span></span><br/>  | <dl> <span data-ttu-id="ea542-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea542-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ea542-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea542-191">Library</span></span><br/> | <dl> <span data-ttu-id="ea542-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea542-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ea542-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea542-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea542-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="ea542-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="ea542-195">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ea542-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
