---
description: Carga un volumen de la memoria.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Función D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707743"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="2227f-103">D3DXLoadVolumeFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="2227f-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="2227f-104">Carga un volumen de la memoria.</span><span class="sxs-lookup"><span data-stu-id="2227f-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="2227f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2227f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="2227f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2227f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2227f-107">*pDestVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="2227f-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="2227f-109">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="2227f-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="2227f-110">Especifica el volumen de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="2227f-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="2227f-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2227f-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="2227f-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-114">*pDestBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="2227f-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="2227f-116">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="2227f-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="2227f-117">Especifica el cuadro de destino.</span><span class="sxs-lookup"><span data-stu-id="2227f-117">Specifies the destination box.</span></span> <span data-ttu-id="2227f-118">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="2227f-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-119">*pSrcMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2227f-121">Puntero en la esquina superior izquierda del volumen de origen en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2227f-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-122">*SrcFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2227f-124">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , el formato de píxel del volumen de origen.</span><span class="sxs-lookup"><span data-stu-id="2227f-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-125">*SrcRowPitch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2227f-127">Tono de la imagen de origen, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2227f-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="2227f-128">En el caso de los formatos de DXT (formatos de textura comprimidos), este número debe representar el tamaño de una fila de celdas, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2227f-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-129">*SrcSlicePitch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2227f-131">Tono de la imagen de origen, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2227f-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="2227f-132">En el caso de los formatos de DXT (formatos de textura comprimidos), este número debe representar el tamaño de un segmento de celdas, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2227f-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-133">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-134">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="2227f-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2227f-135">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="2227f-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-136">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-137">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="2227f-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="2227f-138">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="2227f-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="2227f-139">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2227f-139">Specifies the source box.</span></span> <span data-ttu-id="2227f-140">**Null** no es un valor válido para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="2227f-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-141">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-142">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2227f-143">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="2227f-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2227f-144">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2227f-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2227f-145">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2227f-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2227f-146">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2227f-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2227f-147">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="2227f-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2227f-148">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="2227f-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2227f-149">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="2227f-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2227f-150">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="2227f-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2227f-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2227f-151">Return value</span></span>

<span data-ttu-id="2227f-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2227f-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2227f-153">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2227f-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2227f-154">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2227f-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2227f-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2227f-155">Remarks</span></span>

<span data-ttu-id="2227f-156">La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="2227f-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="2227f-157">Si se llama a **D3DXLoadVolumeFromMemory** y la textura no se ha modificado todavía (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="2227f-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2227f-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2227f-158">Requirements</span></span>



| <span data-ttu-id="2227f-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="2227f-159">Requirement</span></span> | <span data-ttu-id="2227f-160">Value</span><span class="sxs-lookup"><span data-stu-id="2227f-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2227f-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2227f-161">Header</span></span><br/>  | <dl> <span data-ttu-id="2227f-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2227f-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2227f-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2227f-163">Library</span></span><br/> | <dl> <span data-ttu-id="2227f-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2227f-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2227f-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="2227f-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2227f-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="2227f-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="2227f-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="2227f-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="2227f-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="2227f-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="2227f-169">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2227f-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
