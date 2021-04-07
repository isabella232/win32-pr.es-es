---
description: Crea una textura de volumen a partir de un recurso especificado por una cadena. Esta es una función más avanzada que D3DXCreateVolumeTextureFromResource.
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: Función D3DXCreateVolumeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003820"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="f710f-104">D3DXCreateVolumeTextureFromResourceEx función)</span><span class="sxs-lookup"><span data-stu-id="f710f-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="f710f-105">Crea una textura de volumen a partir de un recurso especificado por una cadena.</span><span class="sxs-lookup"><span data-stu-id="f710f-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="f710f-106">Esta es una función más avanzada que [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="f710f-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f710f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f710f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f710f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f710f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f710f-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f710f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f710f-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="f710f-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-112">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-113">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-114">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f710f-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-115">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-117">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="f710f-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="f710f-118">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f710f-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f710f-119">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f710f-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f710f-120">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f710f-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-121">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-123">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f710f-123">Width in pixels.</span></span> <span data-ttu-id="f710f-124">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="f710f-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="f710f-125">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f710f-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f710f-126">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-128">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f710f-128">Height, in pixels.</span></span> <span data-ttu-id="f710f-129">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="f710f-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="f710f-130">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f710f-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f710f-131">*Nivel de detalle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-133">Profundidad, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f710f-133">Depth, in pixels.</span></span> <span data-ttu-id="f710f-134">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="f710f-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="f710f-135">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f710f-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f710f-136">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-138">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="f710f-138">Number of mip levels requested.</span></span> <span data-ttu-id="f710f-139">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="f710f-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-140">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-142">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="f710f-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="f710f-143">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f710f-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="f710f-144">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="f710f-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="f710f-145">Si \_ se especifica D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="f710f-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="f710f-146">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="f710f-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="f710f-147">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="f710f-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="f710f-148">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-149">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f710f-150">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="f710f-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="f710f-151">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="f710f-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="f710f-152">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="f710f-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="f710f-153">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="f710f-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="f710f-154">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f710f-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-155">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-156">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="f710f-157">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="f710f-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-158">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-159">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-160">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="f710f-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="f710f-161">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f710f-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-162">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-163">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f710f-164">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="f710f-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="f710f-165">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f710f-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-166">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f710f-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-167">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="f710f-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="f710f-168">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="f710f-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="f710f-169">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="f710f-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="f710f-170">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="f710f-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="f710f-171">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="f710f-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-172">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f710f-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-173">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f710f-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="f710f-174">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="f710f-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-175">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f710f-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-176">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="f710f-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f710f-177">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="f710f-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f710f-178">*ppVolumeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f710f-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f710f-179">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="f710f-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="f710f-180">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="f710f-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f710f-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f710f-181">Return value</span></span>

<span data-ttu-id="f710f-182">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f710f-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f710f-183">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f710f-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f710f-184">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f710f-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f710f-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f710f-185">Remarks</span></span>

<span data-ttu-id="f710f-186">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="f710f-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f710f-187">Si se define Unicode, la llamada de función se resuelve como D3DXCreateVolumeTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="f710f-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="f710f-188">De lo contrario, la llamada de función se resuelve como D3DXCreateVolumeTextureFromResourceExA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="f710f-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="f710f-189">El recurso que se está cargando debe ser un recurso definido por la aplicación (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="f710f-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="f710f-190">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="f710f-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="f710f-191">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="f710f-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f710f-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f710f-192">Requirements</span></span>



| <span data-ttu-id="f710f-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="f710f-193">Requirement</span></span> | <span data-ttu-id="f710f-194">Value</span><span class="sxs-lookup"><span data-stu-id="f710f-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f710f-195">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f710f-195">Header</span></span><br/>  | <dl> <span data-ttu-id="f710f-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f710f-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f710f-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f710f-197">Library</span></span><br/> | <dl> <span data-ttu-id="f710f-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f710f-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f710f-199">Vea también</span><span class="sxs-lookup"><span data-stu-id="f710f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f710f-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="f710f-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="f710f-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="f710f-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="f710f-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="f710f-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="f710f-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="f710f-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="f710f-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="f710f-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="f710f-205">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f710f-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
