---
description: Crea una textura a partir de un archivo. Esta es una función más avanzada que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Función D3DXCreateTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914722"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="3c260-104">D3DXCreateTextureFromFileEx función)</span><span class="sxs-lookup"><span data-stu-id="3c260-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="3c260-105">Crea una textura a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="3c260-105">Creates a texture from a file.</span></span> <span data-ttu-id="3c260-106">Esta es una función más avanzada que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="3c260-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c260-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c260-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="3c260-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c260-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3c260-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3c260-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="3c260-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-112">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-114">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3c260-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="3c260-115">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3c260-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3c260-116">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3c260-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3c260-117">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3c260-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-118">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-120">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c260-120">Width in pixels.</span></span> <span data-ttu-id="3c260-121">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo y se redondean a una potencia de dos.</span><span class="sxs-lookup"><span data-stu-id="3c260-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="3c260-122">Si el dispositivo admite la no potencia de 2 texturas y se especifica el [ \_ valor predeterminado de D3DX \_ NONPOW2](other-d3dx-constants.md) , no se redondeará el tamaño.</span><span class="sxs-lookup"><span data-stu-id="3c260-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-123">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-125">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c260-125">Height, in pixels.</span></span> <span data-ttu-id="3c260-126">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo y se redondean a una potencia de dos.</span><span class="sxs-lookup"><span data-stu-id="3c260-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="3c260-127">Si el dispositivo admite 2 texturas y el [valor predeterminado de D3DX \_ \_ ](other-d3dx-constants.md) es sepcified, no se redondeará el tamaño.</span><span class="sxs-lookup"><span data-stu-id="3c260-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-128">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-130">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="3c260-130">Number of mip levels requested.</span></span> <span data-ttu-id="3c260-131">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="3c260-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="3c260-132">Si D3DX \_ desde \_ File, el tamaño se tomará exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c260-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-133">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-135">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="3c260-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="3c260-136">Al establecer esta marca en **D3DUSAGE \_ RENDERTARGET** , se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="3c260-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="3c260-137">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="3c260-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="3c260-138">Si se especifica **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="3c260-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="3c260-139">**D3DUSAGE \_ DINÁMICA** indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="3c260-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="3c260-140">Vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="3c260-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c260-141">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="3c260-143">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="3c260-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="3c260-144">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="3c260-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="3c260-145">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="3c260-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="3c260-146">Si D3DFMT \_ es desconocido, el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="3c260-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="3c260-147">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c260-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-148">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="3c260-150">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="3c260-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-151">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-153">Combinación de una o varias constantes [de \_ filtro de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="3c260-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="3c260-154">Especificar el [ \_ valor predeterminado de d3dx](other-d3dx-constants.md) para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3c260-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-155">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c260-157">Combinación de una o varias constantes [de \_ filtro de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="3c260-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="3c260-158">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3c260-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="3c260-159">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="3c260-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-160">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c260-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-161">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="3c260-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="3c260-162">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar la clave de color.</span><span class="sxs-lookup"><span data-stu-id="3c260-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="3c260-163">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="3c260-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="3c260-164">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="3c260-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="3c260-165">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="3c260-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-166">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3c260-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-167">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c260-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="3c260-168">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="3c260-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-169">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c260-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-170">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="3c260-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="3c260-171">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="3c260-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3c260-172">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c260-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c260-173">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="3c260-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="3c260-174">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="3c260-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c260-175">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c260-175">Return value</span></span>

<span data-ttu-id="3c260-176">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c260-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c260-177">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c260-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c260-178">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3c260-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c260-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c260-179">Remarks</span></span>

<span data-ttu-id="3c260-180">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="3c260-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3c260-181">Si se define Unicode, la llamada de función se resuelve como D3DXCreateTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="3c260-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="3c260-182">De lo contrario, la llamada de función se resuelve como D3DXCreateTextureFromFileExA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="3c260-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="3c260-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para determinar si el dispositivo puede admitir la textura según el estado actual.</span><span class="sxs-lookup"><span data-stu-id="3c260-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="3c260-184">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="3c260-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="3c260-185">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="3c260-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="3c260-186">Las texturas de Mipmapped automáticamente tienen cada nivel rellenado con la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="3c260-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="3c260-187">Al cargar imágenes en texturas de mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="3c260-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="3c260-188">Si esto ocurre, las imágenes deben cargarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="3c260-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="3c260-189">Para obtener el mejor rendimiento cuando se usa **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="3c260-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="3c260-190">El escalado de imágenes y la conversión de formato en tiempo de carga puede ser lento.</span><span class="sxs-lookup"><span data-stu-id="3c260-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="3c260-191">Almacenar imágenes en el formato y la resolución que se usarán.</span><span class="sxs-lookup"><span data-stu-id="3c260-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="3c260-192">Si el hardware de destino requiere potencia de 2 dimensiones, cree y almacene imágenes con potencia de 2 dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3c260-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="3c260-193">Para la creación de imágenes de mipmap en tiempo de carga, filtre mediante el [ \_ \_ cuadro de filtro de D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3c260-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="3c260-194">Un filtro de cuadro es mucho más rápido que otros tipos de filtro, como el triángulo de filtro de D3DX \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3c260-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="3c260-195">Considere la posibilidad de utilizar archivos DDS.</span><span class="sxs-lookup"><span data-stu-id="3c260-195">Consider using DDS files.</span></span> <span data-ttu-id="3c260-196">Como los archivos DDS se pueden usar para representar cualquier formato de textura de Direct3D 9, son muy fáciles de leer para D3DX.</span><span class="sxs-lookup"><span data-stu-id="3c260-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="3c260-197">Además, pueden almacenar mapas MIP, por lo que los algoritmos de generación de mipmap se pueden usar para crear las imágenes.</span><span class="sxs-lookup"><span data-stu-id="3c260-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="3c260-198">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de MipFilter.</span><span class="sxs-lookup"><span data-stu-id="3c260-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="3c260-199">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="3c260-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c260-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c260-200">Requirements</span></span>



| <span data-ttu-id="3c260-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c260-201">Requirement</span></span> | <span data-ttu-id="3c260-202">Value</span><span class="sxs-lookup"><span data-stu-id="3c260-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c260-203">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c260-203">Header</span></span><br/>  | <dl> <span data-ttu-id="3c260-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c260-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3c260-205">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c260-205">Library</span></span><br/> | <dl> <span data-ttu-id="3c260-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c260-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3c260-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c260-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c260-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="3c260-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="3c260-209">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="3c260-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
