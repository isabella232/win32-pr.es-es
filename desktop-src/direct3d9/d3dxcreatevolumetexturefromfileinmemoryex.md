---
description: Crea una textura de volumen a partir de un archivo. Esta es una función más avanzada que D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: Función D3DXCreateVolumeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698260"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a><span data-ttu-id="e3402-104">D3DXCreateVolumeTextureFromFileInMemoryEx función)</span><span class="sxs-lookup"><span data-stu-id="e3402-104">D3DXCreateVolumeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="e3402-105">Crea una textura de volumen a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-105">Creates a volume texture from a file.</span></span> <span data-ttu-id="e3402-106">Esta es una función más avanzada que [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e3402-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3402-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3402-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="e3402-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3402-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3402-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e3402-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e3402-111">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="e3402-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-114">Puntero al archivo en la memoria desde el que se va a crear la textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="e3402-114">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-115">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-117">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e3402-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-118">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-120">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e3402-120">Width in pixels.</span></span> <span data-ttu-id="e3402-121">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e3402-122">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e3402-122">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e3402-123">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-125">Alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e3402-125">Height, in pixels.</span></span> <span data-ttu-id="e3402-126">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e3402-127">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e3402-127">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e3402-128">*Nivel de detalle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-128">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-130">Profundidad, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e3402-130">Depth, in pixels.</span></span> <span data-ttu-id="e3402-131">Si este valor es cero o el valor predeterminado de D3DX \_ , las dimensiones se toman del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-131">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e3402-132">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="e3402-132">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e3402-133">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-133">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-135">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="e3402-135">Number of mip levels requested.</span></span> <span data-ttu-id="e3402-136">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="e3402-136">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-137">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-137">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-139">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="e3402-139">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="e3402-140">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="e3402-140">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e3402-141">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="e3402-141">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="e3402-142">Si \_ se especifica D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, el *Grupo* debe establecerse en D3DPOOL \_ default y la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e3402-142">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="e3402-143">D3DUSAGE \_ Dynamic indica que la superficie se debe controlar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="e3402-143">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="e3402-144">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="e3402-144">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3402-145">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-145">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-146">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-146">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e3402-147">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="e3402-147">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="e3402-148">La textura devuelta puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="e3402-148">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="e3402-149">Las aplicaciones deben comprobar el formato de la textura devuelta.</span><span class="sxs-lookup"><span data-stu-id="e3402-149">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="e3402-150">Si [D3DFMT es \_ desconocido](other-d3dx-constants.md), el formato se toma del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-150">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="e3402-151">Si D3DFMT \_ del \_ archivo, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3402-151">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-152">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-152">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-153">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-153">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e3402-154">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="e3402-154">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-155">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-155">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-157">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="e3402-157">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e3402-158">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e3402-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-159">*MipFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-159">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-160">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-160">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3402-161">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="e3402-161">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e3402-162">Especificar \_ el valor predeterminado de d3dx para este parámetro equivale a especificar el cuadro de filtro de d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e3402-162">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="e3402-163">Además, use bits 27-31 para especificar el número de niveles de MIP que se van a omitir (desde la parte superior de la cadena de mapas de bits) cuando se carga una textura. DDS en la memoria; Esto le permite omitir hasta 32 niveles.</span><span class="sxs-lookup"><span data-stu-id="e3402-163">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-164">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3402-164">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-165">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e3402-165">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e3402-166">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="e3402-166">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e3402-167">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="e3402-167">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e3402-168">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="e3402-168">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e3402-169">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e3402-169">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-170">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3402-170">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-171">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3402-171">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="e3402-172">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="e3402-172">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-173">*pPalette* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3402-173">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-174">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="e3402-174">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e3402-175">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores que se va a rellenar o **null**.</span><span class="sxs-lookup"><span data-stu-id="e3402-175">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3402-176">*ppVolumeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3402-176">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3402-177">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e3402-177">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="e3402-178">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="e3402-178">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3402-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3402-179">Return value</span></span>

<span data-ttu-id="e3402-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3402-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3402-181">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3402-181">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e3402-182">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e3402-182">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3402-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3402-183">Remarks</span></span>

<span data-ttu-id="e3402-184">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="e3402-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e3402-185">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e3402-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="e3402-186">Al omitir los niveles de mipmap mientras se carga un archivo. DDS, use la macro de D3DX \_ SKIP \_ DDS \_ MIP \_ Levels para generar el valor de *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="e3402-186">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="e3402-187">Esta macro toma el número de niveles que se omiten y el tipo de filtro, y devuelve el valor de filtro, que se pasaría al parámetro *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="e3402-187">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3402-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3402-188">Requirements</span></span>



| <span data-ttu-id="e3402-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3402-189">Requirement</span></span> | <span data-ttu-id="e3402-190">Value</span><span class="sxs-lookup"><span data-stu-id="e3402-190">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3402-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3402-191">Header</span></span><br/>  | <dl> <span data-ttu-id="e3402-192"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3402-192"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e3402-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3402-193">Library</span></span><br/> | <dl> <span data-ttu-id="e3402-194"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3402-194"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3402-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3402-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3402-196">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="e3402-196">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="e3402-197">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="e3402-197">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="e3402-198">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e3402-198">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="e3402-199">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="e3402-199">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="e3402-200">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="e3402-200">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="e3402-201">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e3402-201">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
