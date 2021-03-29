---
description: Carga una superficie de un recurso.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: Función D3DXLoadSurfaceFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003766"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="f1f14-103">D3DXLoadSurfaceFromResource función)</span><span class="sxs-lookup"><span data-stu-id="f1f14-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="f1f14-104">Carga una superficie de un recurso.</span><span class="sxs-lookup"><span data-stu-id="f1f14-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1f14-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f1f14-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1f14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f14-107">*pDestSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="f1f14-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="f1f14-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="f1f14-110">Especifica la superficie de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="f1f14-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="f1f14-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f1f14-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="f1f14-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-114">*pDestRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="f1f14-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="f1f14-116">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1f14-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="f1f14-117">Especifica el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="f1f14-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="f1f14-118">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="f1f14-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-119">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-120">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1f14-121">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f1f14-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-122">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-123">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1f14-124">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="f1f14-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="f1f14-125">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f1f14-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f1f14-126">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f1f14-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f1f14-127">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f1f14-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-128">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-129">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="f1f14-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="f1f14-130">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1f14-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="f1f14-131">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="f1f14-131">Specifies the source rectangle.</span></span> <span data-ttu-id="f1f14-132">Establezca este parámetro en **null** para especificar la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="f1f14-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-133">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1f14-135">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="f1f14-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="f1f14-136">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f1f14-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-137">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-138">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="f1f14-139">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="f1f14-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="f1f14-140">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="f1f14-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="f1f14-141">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas, por lo que, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="f1f14-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="f1f14-142">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f1f14-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f14-143">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1f14-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="f1f14-144">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="f1f14-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f14-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1f14-145">Return value</span></span>

<span data-ttu-id="f1f14-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1f14-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1f14-147">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1f14-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1f14-148">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f1f14-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f14-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1f14-149">Remarks</span></span>

<span data-ttu-id="f1f14-150">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="f1f14-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f1f14-151">Si se define Unicode, la llamada de función se resuelve como D3DXLoadSurfaceFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="f1f14-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="f1f14-152">De lo contrario, la llamada de función se resuelve como D3DXLoadSurfaceFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1f14-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="f1f14-153">El recurso que se está cargando debe ser de tipo RT \_ Bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="f1f14-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="f1f14-154">El tipo de recurso RT \_ RCDATA se usa para cargar formatos distintos de los mapas de bits (como. TGA,. jpg y. DDS).</span><span class="sxs-lookup"><span data-stu-id="f1f14-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="f1f14-155">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="f1f14-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="f1f14-156">La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="f1f14-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="f1f14-157">Si se llama a [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="f1f14-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f14-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1f14-158">Requirements</span></span>



| <span data-ttu-id="f1f14-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1f14-159">Requirement</span></span> | <span data-ttu-id="f1f14-160">Value</span><span class="sxs-lookup"><span data-stu-id="f1f14-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f14-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1f14-161">Header</span></span><br/>  | <dl> <span data-ttu-id="f1f14-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f14-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f1f14-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1f14-163">Library</span></span><br/> | <dl> <span data-ttu-id="f1f14-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1f14-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1f14-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1f14-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f14-166">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f1f14-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
