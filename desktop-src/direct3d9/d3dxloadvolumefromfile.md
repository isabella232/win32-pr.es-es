---
description: Carga un volumen desde un archivo.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: Función D3DXLoadVolumeFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707744"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="0574f-103">D3DXLoadVolumeFromFile función)</span><span class="sxs-lookup"><span data-stu-id="0574f-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="0574f-104">Carga un volumen desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="0574f-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0574f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0574f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0574f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0574f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0574f-107">*pDestVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="0574f-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="0574f-109">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="0574f-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="0574f-110">Especifica el volumen de destino.</span><span class="sxs-lookup"><span data-stu-id="0574f-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="0574f-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="0574f-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="0574f-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-114">*pDestBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="0574f-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="0574f-116">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="0574f-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="0574f-117">Especifica el cuadro de destino.</span><span class="sxs-lookup"><span data-stu-id="0574f-117">Specifies the destination box.</span></span> <span data-ttu-id="0574f-118">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="0574f-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-119">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0574f-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0574f-121">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="0574f-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="0574f-122">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0574f-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0574f-123">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0574f-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0574f-124">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0574f-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-125">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-126">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="0574f-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="0574f-127">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="0574f-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="0574f-128">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="0574f-128">Specifies the source box.</span></span> <span data-ttu-id="0574f-129">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="0574f-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-130">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0574f-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0574f-132">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="0574f-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="0574f-133">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0574f-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-134">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="0574f-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="0574f-136">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="0574f-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="0574f-137">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="0574f-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="0574f-138">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="0574f-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="0574f-139">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="0574f-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="0574f-140">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0574f-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0574f-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0574f-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="0574f-142">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="0574f-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0574f-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0574f-143">Return value</span></span>

<span data-ttu-id="0574f-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0574f-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0574f-145">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0574f-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0574f-146">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="0574f-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0574f-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0574f-147">Remarks</span></span>

<span data-ttu-id="0574f-148">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="0574f-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0574f-149">Si se define Unicode, la llamada de función se resuelve como D3DXLoadVolumeFromFileW.</span><span class="sxs-lookup"><span data-stu-id="0574f-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="0574f-150">De lo contrario, la llamada de función se resuelve como D3DXLoadVolumeFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="0574f-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="0574f-151">Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="0574f-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="0574f-152">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="0574f-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="0574f-153">La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="0574f-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="0574f-154">Si se llama a **D3DXLoadVolumeFromFile** y la textura no se ha modificado todavía (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="0574f-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0574f-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0574f-155">Requirements</span></span>



| <span data-ttu-id="0574f-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="0574f-156">Requirement</span></span> | <span data-ttu-id="0574f-157">Value</span><span class="sxs-lookup"><span data-stu-id="0574f-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0574f-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0574f-158">Header</span></span><br/>  | <dl> <span data-ttu-id="0574f-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0574f-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0574f-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0574f-160">Library</span></span><br/> | <dl> <span data-ttu-id="0574f-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0574f-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0574f-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0574f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0574f-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="0574f-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="0574f-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="0574f-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="0574f-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="0574f-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="0574f-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="0574f-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="0574f-167">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0574f-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
