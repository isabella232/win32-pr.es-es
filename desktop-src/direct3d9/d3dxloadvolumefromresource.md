---
description: Carga un volumen desde un recurso.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Función D3DXLoadVolumeFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707742"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="ef67a-103">D3DXLoadVolumeFromResource función)</span><span class="sxs-lookup"><span data-stu-id="ef67a-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="ef67a-104">Carga un volumen desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="ef67a-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef67a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef67a-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ef67a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef67a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef67a-107">*pDestVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="ef67a-109">Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="ef67a-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="ef67a-110">Especifica el volumen de destino.</span><span class="sxs-lookup"><span data-stu-id="ef67a-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-111">*pDestPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-112">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ef67a-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ef67a-113">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="ef67a-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-114">*pDestBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef67a-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ef67a-116">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ef67a-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ef67a-117">Especifica el cuadro de destino.</span><span class="sxs-lookup"><span data-stu-id="ef67a-117">Specifies the destination box.</span></span> <span data-ttu-id="ef67a-118">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="ef67a-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-119">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-120">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef67a-121">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ef67a-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-122">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef67a-124">Puntero a una cadena que especifica el nombre de archivo de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="ef67a-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="ef67a-125">Si se definen Unicode o \_ Unicode, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ef67a-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-126">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef67a-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ef67a-128">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ef67a-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ef67a-129">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="ef67a-129">Specifies the source box.</span></span> <span data-ttu-id="ef67a-130">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="ef67a-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-131">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ef67a-133">Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen.</span><span class="sxs-lookup"><span data-stu-id="ef67a-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="ef67a-134">Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ef67a-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-135">*ColorKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ef67a-137">Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey.</span><span class="sxs-lookup"><span data-stu-id="ef67a-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ef67a-138">Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="ef67a-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ef67a-139">Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas.</span><span class="sxs-lookup"><span data-stu-id="ef67a-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ef67a-140">Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ef67a-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ef67a-141">*pSrcInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ef67a-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef67a-142">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef67a-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ef67a-143">Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.</span><span class="sxs-lookup"><span data-stu-id="ef67a-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef67a-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef67a-144">Return value</span></span>

<span data-ttu-id="ef67a-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef67a-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef67a-146">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef67a-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef67a-147">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ef67a-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef67a-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef67a-148">Remarks</span></span>

<span data-ttu-id="ef67a-149">El recurso que se está cargando debe ser un recurso de mapa de bits ( \_ mapa de bits RT).</span><span class="sxs-lookup"><span data-stu-id="ef67a-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="ef67a-150">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="ef67a-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="ef67a-151">La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio.</span><span class="sxs-lookup"><span data-stu-id="ef67a-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ef67a-152">Si se llama a [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) y la textura no se ha modificado todavía (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="ef67a-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="ef67a-153">Esta función admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef67a-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef67a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef67a-154">Requirements</span></span>



| <span data-ttu-id="ef67a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef67a-155">Requirement</span></span> | <span data-ttu-id="ef67a-156">Value</span><span class="sxs-lookup"><span data-stu-id="ef67a-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef67a-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef67a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="ef67a-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef67a-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ef67a-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef67a-159">Library</span></span><br/> | <dl> <span data-ttu-id="ef67a-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef67a-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ef67a-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef67a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef67a-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="ef67a-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="ef67a-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ef67a-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ef67a-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ef67a-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="ef67a-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="ef67a-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="ef67a-166">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ef67a-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
