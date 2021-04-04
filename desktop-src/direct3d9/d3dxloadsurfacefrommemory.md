---
description: Carga una superficie de la memoria.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Función D3DXLoadSurfaceFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083706"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="08f4b-103">D3DXLoadSurfaceFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="08f4b-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="08f4b-104">Carga una superficie de la memoria.</span><span class="sxs-lookup"><span data-stu-id="08f4b-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08f4b-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="08f4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f4b-107">*pDestSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="08f4b-109">Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="08f4b-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="08f4b-110">Especifica la superficie de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="08f4b-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="08f4b-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="08f4b-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-114">*pDestRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="08f4b-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="08f4b-116">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="08f4b-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="08f4b-117">Especifica el rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="08f4b-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="08f4b-118">Establezca este parámetro en **null** para especificar toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="08f4b-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-119">*pSrcMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08f4b-121">Puntero en la esquina superior izquierda de la imagen de origen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="08f4b-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-122">*SrcFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="08f4b-124">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , el formato de píxel de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="08f4b-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-125">*SrcPitch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08f4b-127">Tono de la imagen de origen, en bytes.</span><span class="sxs-lookup"><span data-stu-id="08f4b-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="08f4b-128">En el caso de los formatos DXT, este número debe representar el ancho de una fila de celdas, en bytes.</span><span class="sxs-lookup"><span data-stu-id="08f4b-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-129">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-130">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="08f4b-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="08f4b-131">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-132">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-133">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="08f4b-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="08f4b-134">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="08f4b-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="08f4b-135">Especifica las dimensiones de la imagen de origen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="08f4b-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="08f4b-136">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="08f4b-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-137">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08f4b-139">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="08f4b-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="08f4b-140">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08f4b-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="08f4b-141">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08f4b-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f4b-142">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="08f4b-143">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="08f4b-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="08f4b-144">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="08f4b-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="08f4b-145">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="08f4b-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="08f4b-146">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="08f4b-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f4b-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08f4b-147">Return value</span></span>

<span data-ttu-id="08f4b-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08f4b-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08f4b-149">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08f4b-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08f4b-150">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="08f4b-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f4b-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08f4b-151">Remarks</span></span>

<span data-ttu-id="08f4b-152">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="08f4b-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="08f4b-153">La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="08f4b-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="08f4b-154">Si se llama a **D3DXLoadSurfaceFromMemory** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="08f4b-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f4b-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f4b-155">Requirements</span></span>



| <span data-ttu-id="08f4b-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f4b-156">Requirement</span></span> | <span data-ttu-id="08f4b-157">Value</span><span class="sxs-lookup"><span data-stu-id="08f4b-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08f4b-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08f4b-158">Header</span></span><br/>  | <dl> <span data-ttu-id="08f4b-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f4b-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="08f4b-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08f4b-160">Library</span></span><br/> | <dl> <span data-ttu-id="08f4b-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08f4b-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="08f4b-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="08f4b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f4b-163">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="08f4b-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
