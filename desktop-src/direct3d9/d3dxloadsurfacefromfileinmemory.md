---
description: Carga una superficie de un archivo en la memoria.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: Función D3DXLoadSurfaceFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821466"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="92c08-103">D3DXLoadSurfaceFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="92c08-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="92c08-104">Carga una superficie de un archivo en la memoria.</span><span class="sxs-lookup"><span data-stu-id="92c08-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c08-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92c08-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="92c08-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c08-107">*pDestSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="92c08-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="92c08-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="92c08-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="92c08-110">Especifica la superficie de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="92c08-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="92c08-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="92c08-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="92c08-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-114">*pDestRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="92c08-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="92c08-116">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="92c08-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="92c08-117">Especifica el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="92c08-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="92c08-118">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="92c08-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-119">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c08-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92c08-121">Puntero al archivo en la memoria desde el que se va a cargar la superficie.</span><span class="sxs-lookup"><span data-stu-id="92c08-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-122">*SrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c08-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92c08-124">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="92c08-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-125">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="92c08-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="92c08-127">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="92c08-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="92c08-128">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="92c08-128">Specifies the source rectangle.</span></span> <span data-ttu-id="92c08-129">Establezca este parámetro en **null** para especificar la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="92c08-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-130">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92c08-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92c08-132">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="92c08-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="92c08-133">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="92c08-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-134">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92c08-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="92c08-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="92c08-136">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="92c08-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="92c08-137">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="92c08-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="92c08-138">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="92c08-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="92c08-139">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="92c08-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="92c08-140">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="92c08-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92c08-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="92c08-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="92c08-142">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="92c08-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c08-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92c08-143">Return value</span></span>

<span data-ttu-id="92c08-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92c08-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92c08-145">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92c08-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92c08-146">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="92c08-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c08-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92c08-147">Remarks</span></span>

<span data-ttu-id="92c08-148">Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="92c08-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="92c08-149">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="92c08-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="92c08-150">La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="92c08-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="92c08-151">Si se llama a **D3DXLoadSurfaceFromFileInMemory** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="92c08-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c08-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c08-152">Requirements</span></span>



| <span data-ttu-id="92c08-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c08-153">Requirement</span></span> | <span data-ttu-id="92c08-154">Value</span><span class="sxs-lookup"><span data-stu-id="92c08-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92c08-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92c08-155">Header</span></span><br/>  | <dl> <span data-ttu-id="92c08-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c08-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="92c08-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92c08-157">Library</span></span><br/> | <dl> <span data-ttu-id="92c08-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92c08-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="92c08-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="92c08-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c08-160">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="92c08-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
