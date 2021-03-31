---
description: Carga una superficie de un archivo.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Función D3DXLoadSurfaceFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821471"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="84233-103">D3DXLoadSurfaceFromFile función)</span><span class="sxs-lookup"><span data-stu-id="84233-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="84233-104">Carga una superficie de un archivo.</span><span class="sxs-lookup"><span data-stu-id="84233-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="84233-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84233-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="84233-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84233-107">*pDestSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="84233-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="84233-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="84233-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="84233-110">Especifica la superficie de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="84233-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="84233-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="84233-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="84233-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="84233-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="84233-114">*pDestRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="84233-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="84233-116">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84233-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="84233-117">Especifica el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="84233-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="84233-118">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="84233-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="84233-119">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84233-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84233-121">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="84233-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="84233-122">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="84233-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="84233-123">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="84233-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="84233-124">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="84233-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="84233-125">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="84233-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="84233-127">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="84233-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="84233-128">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="84233-128">Specifies the source rectangle.</span></span> <span data-ttu-id="84233-129">Establezca este parámetro en **null** para especificar la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="84233-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="84233-130">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="84233-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84233-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84233-132">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="84233-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="84233-133">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="84233-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="84233-134">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84233-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="84233-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="84233-136">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="84233-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="84233-137">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="84233-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="84233-138">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas, por lo que, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="84233-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="84233-139">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84233-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84233-140">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="84233-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="84233-141">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="84233-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84233-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84233-142">Return value</span></span>

<span data-ttu-id="84233-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84233-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84233-144">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="84233-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84233-145">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="84233-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="84233-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84233-146">Remarks</span></span>

<span data-ttu-id="84233-147">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="84233-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="84233-148">Si se define Unicode, la llamada de función se resuelve como D3DXLoadSurfaceFromFileW.</span><span class="sxs-lookup"><span data-stu-id="84233-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="84233-149">De lo contrario, la llamada de función se resuelve como D3DXLoadSurfaceFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="84233-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="84233-150">Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="84233-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="84233-151">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="84233-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="84233-152">La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="84233-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="84233-153">Si se llama a **D3DXLoadSurfaceFromFile** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="84233-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="84233-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84233-154">Requirements</span></span>



| <span data-ttu-id="84233-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="84233-155">Requirement</span></span> | <span data-ttu-id="84233-156">Value</span><span class="sxs-lookup"><span data-stu-id="84233-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84233-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84233-157">Header</span></span><br/>  | <dl> <span data-ttu-id="84233-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="84233-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="84233-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84233-159">Library</span></span><br/> | <dl> <span data-ttu-id="84233-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84233-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="84233-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="84233-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84233-162">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="84233-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
