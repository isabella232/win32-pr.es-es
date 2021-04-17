---
description: Guarda una superficie en un archivo.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: Función D3DXSaveSurfaceToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717743"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="b2196-103">D3DXSaveSurfaceToFile función)</span><span class="sxs-lookup"><span data-stu-id="b2196-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="b2196-104">Guarda una superficie en un archivo.</span><span class="sxs-lookup"><span data-stu-id="b2196-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2196-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2196-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="b2196-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2196-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2196-107">*pDestFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2196-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2196-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2196-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2196-109">Puntero a una cadena que especifica el nombre de archivo de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="b2196-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="b2196-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b2196-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b2196-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b2196-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b2196-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b2196-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b2196-113">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2196-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2196-114">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b2196-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="b2196-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="b2196-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="b2196-116">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="b2196-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="b2196-117">*pSrcSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2196-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2196-118">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="b2196-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="b2196-119">Puntero a la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que contiene la imagen que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="b2196-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b2196-120">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2196-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2196-121">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="b2196-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b2196-122">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="b2196-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="b2196-123">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b2196-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b2196-124">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2196-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2196-125">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="b2196-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="b2196-126">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b2196-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="b2196-127">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="b2196-127">Specifies the source rectangle.</span></span> <span data-ttu-id="b2196-128">Establezca este parámetro en **null** para especificar la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="b2196-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2196-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2196-129">Return value</span></span>

<span data-ttu-id="b2196-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2196-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2196-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2196-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2196-132">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b2196-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b2196-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2196-133">Remarks</span></span>

<span data-ttu-id="b2196-134">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="b2196-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b2196-135">Si se define Unicode, la llamada de función se resuelve como D3DXSaveSurfaceToFileW.</span><span class="sxs-lookup"><span data-stu-id="b2196-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="b2196-136">De lo contrario, la llamada de función se resuelve como D3DXSaveSurfaceToFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="b2196-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="b2196-137">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="b2196-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2196-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2196-138">Requirements</span></span>



| <span data-ttu-id="b2196-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2196-139">Requirement</span></span> | <span data-ttu-id="b2196-140">Value</span><span class="sxs-lookup"><span data-stu-id="b2196-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2196-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2196-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b2196-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2196-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b2196-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2196-143">Library</span></span><br/> | <dl> <span data-ttu-id="b2196-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2196-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b2196-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2196-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2196-146">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b2196-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b2196-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="b2196-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="b2196-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="b2196-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
