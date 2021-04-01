---
description: Guarda una textura en un archivo de imagen.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: Función D3DXSaveTextureToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157176"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="80b87-103">D3DXSaveTextureToFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="80b87-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="80b87-104">Guarda una textura en un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="80b87-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b87-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80b87-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="80b87-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80b87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b87-107">*ppDestBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80b87-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80b87-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="80b87-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="80b87-109">Dirección de un puntero a un [**ID3DXBuffer**](id3dxbuffer.md) que almacenará la imagen.</span><span class="sxs-lookup"><span data-stu-id="80b87-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="80b87-110">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80b87-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b87-111">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="80b87-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="80b87-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="80b87-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="80b87-113">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="80b87-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="80b87-114">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80b87-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b87-115">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="80b87-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="80b87-116">Puntero a la interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que contiene la imagen que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="80b87-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="80b87-117">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80b87-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b87-118">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="80b87-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="80b87-119">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="80b87-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="80b87-120">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="80b87-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b87-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80b87-121">Return value</span></span>

<span data-ttu-id="80b87-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80b87-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80b87-123">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80b87-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80b87-124">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="80b87-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="80b87-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80b87-125">Remarks</span></span>

<span data-ttu-id="80b87-126">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="80b87-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b87-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b87-127">Requirements</span></span>



| <span data-ttu-id="80b87-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b87-128">Requirement</span></span> | <span data-ttu-id="80b87-129">Value</span><span class="sxs-lookup"><span data-stu-id="80b87-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80b87-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80b87-130">Header</span></span><br/>  | <dl> <span data-ttu-id="80b87-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b87-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="80b87-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80b87-132">Library</span></span><br/> | <dl> <span data-ttu-id="80b87-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80b87-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="80b87-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="80b87-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b87-135">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="80b87-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="80b87-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="80b87-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="80b87-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="80b87-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
