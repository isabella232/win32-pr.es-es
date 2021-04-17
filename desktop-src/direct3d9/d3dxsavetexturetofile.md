---
description: Guarda una textura en un archivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Función D3DXSaveTextureToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698225"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="0d2d7-103">D3DXSaveTextureToFile función)</span><span class="sxs-lookup"><span data-stu-id="0d2d7-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="0d2d7-104">Guarda una textura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d2d7-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="0d2d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d2d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2d7-107">*pDestFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d2d7-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2d7-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d2d7-109">Puntero a una cadena que especifica el nombre de archivo de la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="0d2d7-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0d2d7-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0d2d7-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0d2d7-113">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d2d7-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2d7-114">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="0d2d7-115">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="0d2d7-116">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="0d2d7-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d7-117">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d2d7-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2d7-118">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="0d2d7-119">Puntero a la interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , que contiene la textura que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="0d2d7-120">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d2d7-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d2d7-121">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="0d2d7-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="0d2d7-122">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="0d2d7-123">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d2d7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d2d7-124">Return value</span></span>

<span data-ttu-id="0d2d7-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d2d7-126">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d2d7-127">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="0d2d7-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="0d2d7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d2d7-128">Remarks</span></span>

<span data-ttu-id="0d2d7-129">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0d2d7-130">Si se define Unicode, la llamada de función se resuelve como D3DXSaveTextureToFileW.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="0d2d7-131">De lo contrario, la llamada de función se resuelve como D3DXSaveTextureToFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="0d2d7-132">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="0d2d7-133">Si el volumen no es dinámico (debido a un parámetro de uso establecido en 0 en la creación) y se encuentra en la memoria de vídeo (el grupo de memoria se establece en el \_ valor predeterminado de D3DPOOL), **D3DXSaveTextureToFile** producirá un error porque D3DX no bloquea volúmenes no dinámicos ubicados en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0d2d7-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d2d7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d2d7-134">Requirements</span></span>



| <span data-ttu-id="0d2d7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2d7-135">Requirement</span></span> | <span data-ttu-id="0d2d7-136">Value</span><span class="sxs-lookup"><span data-stu-id="0d2d7-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2d7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d2d7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="0d2d7-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d2d7-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0d2d7-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d2d7-139">Library</span></span><br/> | <dl> <span data-ttu-id="0d2d7-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d2d7-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0d2d7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d2d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2d7-142">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0d2d7-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="0d2d7-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="0d2d7-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="0d2d7-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
