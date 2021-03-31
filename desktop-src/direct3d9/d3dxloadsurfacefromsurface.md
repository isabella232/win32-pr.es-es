---
description: Carga una superficie desde otra superficie con conversión de color.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: Función D3DXLoadSurfaceFromSurface (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821271"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="96eb7-103">D3DXLoadSurfaceFromSurface función)</span><span class="sxs-lookup"><span data-stu-id="96eb7-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="96eb7-104">Carga una superficie desde otra superficie con conversión de color.</span><span class="sxs-lookup"><span data-stu-id="96eb7-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="96eb7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96eb7-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="96eb7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96eb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96eb7-107">*pDestSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="96eb7-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="96eb7-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="96eb7-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="96eb7-110">Especifica la superficie de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="96eb7-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="96eb7-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="96eb7-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="96eb7-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-114">*pDestRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="96eb7-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="96eb7-116">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96eb7-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="96eb7-117">Especifica el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="96eb7-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="96eb7-118">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="96eb7-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-119">*pSrcSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-120">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="96eb7-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="96eb7-121">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que representa la superficie de origen.</span><span class="sxs-lookup"><span data-stu-id="96eb7-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-122">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-123">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="96eb7-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="96eb7-124">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="96eb7-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-125">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="96eb7-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="96eb7-127">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96eb7-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="96eb7-128">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="96eb7-128">Specifies the source rectangle.</span></span> <span data-ttu-id="96eb7-129">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="96eb7-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-130">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96eb7-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96eb7-132">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="96eb7-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="96eb7-133">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="96eb7-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="96eb7-134">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96eb7-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96eb7-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="96eb7-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="96eb7-136">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="96eb7-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="96eb7-137">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="96eb7-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="96eb7-138">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="96eb7-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="96eb7-139">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="96eb7-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96eb7-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96eb7-140">Return value</span></span>

<span data-ttu-id="96eb7-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96eb7-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96eb7-142">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96eb7-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="96eb7-143">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="96eb7-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="96eb7-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96eb7-144">Remarks</span></span>

<span data-ttu-id="96eb7-145">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="96eb7-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="96eb7-146">La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="96eb7-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="96eb7-147">Si se llama a **D3DXLoadSurfaceFromSurface** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="96eb7-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="96eb7-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96eb7-148">Requirements</span></span>



| <span data-ttu-id="96eb7-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="96eb7-149">Requirement</span></span> | <span data-ttu-id="96eb7-150">Value</span><span class="sxs-lookup"><span data-stu-id="96eb7-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96eb7-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96eb7-151">Header</span></span><br/>  | <dl> <span data-ttu-id="96eb7-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="96eb7-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="96eb7-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96eb7-153">Library</span></span><br/> | <dl> <span data-ttu-id="96eb7-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96eb7-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96eb7-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="96eb7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96eb7-156">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="96eb7-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
