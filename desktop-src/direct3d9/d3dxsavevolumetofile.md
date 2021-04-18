---
description: Guarda un volumen en un archivo en disco.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Función D3DXSaveVolumeToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698224"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="6c080-103">D3DXSaveVolumeToFile función)</span><span class="sxs-lookup"><span data-stu-id="6c080-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="6c080-104">Guarda un volumen en un archivo en disco.</span><span class="sxs-lookup"><span data-stu-id="6c080-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c080-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c080-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="6c080-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c080-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c080-107">*pDestFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c080-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c080-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c080-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c080-109">Puntero a una cadena que especifica el nombre de archivo de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="6c080-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="6c080-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6c080-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6c080-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6c080-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6c080-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6c080-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6c080-113">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c080-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c080-114">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6c080-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="6c080-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="6c080-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="6c080-116">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="6c080-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="6c080-117">*pSrcVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c080-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c080-118">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="6c080-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="6c080-119">Puntero a la interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contiene la imagen que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="6c080-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="6c080-120">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c080-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c080-121">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6c080-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6c080-122">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="6c080-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="6c080-123">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6c080-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c080-124">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c080-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c080-125">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c080-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6c080-126">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6c080-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6c080-127">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="6c080-127">Specifies the source box.</span></span> <span data-ttu-id="6c080-128">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="6c080-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c080-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c080-129">Return value</span></span>

<span data-ttu-id="6c080-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c080-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c080-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c080-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c080-132">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6c080-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6c080-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c080-133">Remarks</span></span>

<span data-ttu-id="6c080-134">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="6c080-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6c080-135">Si se define Unicode, la llamada de función se resuelve como D3DXSaveVolumeToFileW.</span><span class="sxs-lookup"><span data-stu-id="6c080-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="6c080-136">De lo contrario, la llamada de función se resuelve en >D3DXSaveVolumeToFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c080-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="6c080-137">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="6c080-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="6c080-138">Si el volumen no es dinámico (debido a un parámetro de uso establecido en 0 en la creación) y se encuentra en la memoria de vídeo (el grupo de memoria se establece en el \_ valor predeterminado de D3DPOOL), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) producirá un error porque D3DX no bloquea volúmenes no dinámicos ubicados en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6c080-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c080-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c080-139">Requirements</span></span>



| <span data-ttu-id="6c080-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c080-140">Requirement</span></span> | <span data-ttu-id="6c080-141">Value</span><span class="sxs-lookup"><span data-stu-id="6c080-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c080-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c080-142">Header</span></span><br/>  | <dl> <span data-ttu-id="6c080-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c080-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6c080-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c080-144">Library</span></span><br/> | <dl> <span data-ttu-id="6c080-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c080-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6c080-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c080-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c080-147">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6c080-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6c080-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="6c080-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="6c080-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="6c080-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="6c080-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6c080-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
