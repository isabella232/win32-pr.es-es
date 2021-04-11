---
description: Carga un volumen desde otro volumen.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: Función D3DXLoadVolumeFromVolume (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003910"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="bb5f9-103">D3DXLoadVolumeFromVolume función)</span><span class="sxs-lookup"><span data-stu-id="bb5f9-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="bb5f9-104">Carga un volumen desde otro volumen.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb5f9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="bb5f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb5f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5f9-107">*pDestVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="bb5f9-109">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="bb5f9-110">Especifica el volumen de destino, que recibe la imagen.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="bb5f9-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="bb5f9-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-114">*pDestBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb5f9-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="bb5f9-116">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="bb5f9-117">Especifica el cuadro de destino.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-117">Specifies the destination box.</span></span> <span data-ttu-id="bb5f9-118">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-119">*pSrcVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-120">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="bb5f9-121">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="bb5f9-122">Especifica el volumen de origen.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-123">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-124">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="bb5f9-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="bb5f9-125">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-126">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb5f9-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="bb5f9-128">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="bb5f9-129">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-129">Specifies the source box.</span></span> <span data-ttu-id="bb5f9-130">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-131">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb5f9-133">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="bb5f9-134">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f9-135">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb5f9-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5f9-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="bb5f9-137">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="bb5f9-138">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="bb5f9-139">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="bb5f9-140">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5f9-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb5f9-141">Return value</span></span>

<span data-ttu-id="bb5f9-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb5f9-143">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb5f9-144">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5f9-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb5f9-145">Remarks</span></span>

<span data-ttu-id="bb5f9-146">La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="bb5f9-147">Si se llama a **D3DXLoadVolumeFromVolume** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la superficie.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5f9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb5f9-148">Requirements</span></span>



| <span data-ttu-id="bb5f9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5f9-149">Requirement</span></span> | <span data-ttu-id="bb5f9-150">Value</span><span class="sxs-lookup"><span data-stu-id="bb5f9-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5f9-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb5f9-151">Header</span></span><br/>  | <dl> <span data-ttu-id="bb5f9-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5f9-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="bb5f9-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb5f9-153">Library</span></span><br/> | <dl> <span data-ttu-id="bb5f9-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb5f9-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bb5f9-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb5f9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5f9-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-160">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="bb5f9-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
