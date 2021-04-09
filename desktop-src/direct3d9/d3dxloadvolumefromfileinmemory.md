---
description: Carga un volumen de un archivo en memoria.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: Función D3DXLoadVolumeFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003800"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a><span data-ttu-id="8ffbe-103">D3DXLoadVolumeFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="8ffbe-103">D3DXLoadVolumeFromFileInMemory function</span></span>

<span data-ttu-id="8ffbe-104">Carga un volumen de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-104">Loads a volume from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffbe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ffbe-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8ffbe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ffbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffbe-107">*pDestVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="8ffbe-109">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="8ffbe-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="8ffbe-110">Especifica el volumen de destino.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8ffbe-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8ffbe-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-114">*pDestBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ffbe-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="8ffbe-116">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffbe-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="8ffbe-117">Especifica el cuadro de destino.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-117">Specifies the destination box.</span></span> <span data-ttu-id="8ffbe-118">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-119">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ffbe-121">Puntero al archivo en la memoria desde el que se va a cargar el volumen.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-121">Pointer to the file in memory from which to load the volume.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-122">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-122">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ffbe-124">Tamaño en bytes del archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-124">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-125">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-126">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ffbe-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="8ffbe-127">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffbe-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="8ffbe-128">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-128">Specifies the source box.</span></span> <span data-ttu-id="8ffbe-129">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-130">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ffbe-132">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="8ffbe-133">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8ffbe-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-134">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="8ffbe-136">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="8ffbe-137">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="8ffbe-138">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="8ffbe-139">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="8ffbe-140">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffbe-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffbe-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ffbe-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="8ffbe-142">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffbe-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ffbe-143">Return value</span></span>

<span data-ttu-id="8ffbe-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ffbe-145">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8ffbe-146">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffbe-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ffbe-147">Remarks</span></span>

<span data-ttu-id="8ffbe-148">Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="8ffbe-149">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="8ffbe-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="8ffbe-150">La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-150">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="8ffbe-151">Si se llama a **D3DXLoadVolumeFromFileInMemory** y la textura no se ha modificado todavía (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="8ffbe-151">If **D3DXLoadVolumeFromFileInMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffbe-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ffbe-152">Requirements</span></span>



| <span data-ttu-id="8ffbe-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffbe-153">Requirement</span></span> | <span data-ttu-id="8ffbe-154">Value</span><span class="sxs-lookup"><span data-stu-id="8ffbe-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffbe-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ffbe-155">Header</span></span><br/>  | <dl> <span data-ttu-id="8ffbe-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ffbe-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8ffbe-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ffbe-157">Library</span></span><br/> | <dl> <span data-ttu-id="8ffbe-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ffbe-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8ffbe-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ffbe-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffbe-160">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-160">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="8ffbe-161">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-161">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="8ffbe-162">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-162">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="8ffbe-163">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="8ffbe-163">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="8ffbe-164">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8ffbe-164">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
