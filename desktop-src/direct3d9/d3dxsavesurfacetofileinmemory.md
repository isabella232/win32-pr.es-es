---
description: Guarda una superficie en un archivo de imagen.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: Función D3DXSaveSurfaceToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698226"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="e3384-103">D3DXSaveSurfaceToFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="e3384-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="e3384-104">Guarda una superficie en un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="e3384-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3384-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3384-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="e3384-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3384-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3384-107">*ppDestBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3384-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3384-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3384-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e3384-109">Dirección de un puntero a un [**ID3DXBuffer**](id3dxbuffer.md) que almacenará la imagen.</span><span class="sxs-lookup"><span data-stu-id="e3384-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="e3384-110">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3384-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3384-111">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e3384-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="e3384-112">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="e3384-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="e3384-113">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="e3384-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="e3384-114">*pSrcSurface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3384-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3384-115">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e3384-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e3384-116">Puntero a la interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) que contiene la imagen que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="e3384-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="e3384-117">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3384-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3384-118">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e3384-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e3384-119">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="e3384-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="e3384-120">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e3384-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3384-121">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3384-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3384-122">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e3384-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e3384-123">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e3384-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e3384-124">Especifica el rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="e3384-124">Specifies the source rectangle.</span></span> <span data-ttu-id="e3384-125">Establezca este parámetro en **null** para especificar la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="e3384-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3384-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3384-126">Return value</span></span>

<span data-ttu-id="e3384-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3384-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3384-128">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3384-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e3384-129">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e3384-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3384-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3384-130">Remarks</span></span>

<span data-ttu-id="e3384-131">Esta función controla la conversión a y desde formatos de textura comprimidos.</span><span class="sxs-lookup"><span data-stu-id="e3384-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3384-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3384-132">Requirements</span></span>



| <span data-ttu-id="e3384-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3384-133">Requirement</span></span> | <span data-ttu-id="e3384-134">Value</span><span class="sxs-lookup"><span data-stu-id="e3384-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3384-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3384-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e3384-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3384-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e3384-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3384-137">Library</span></span><br/> | <dl> <span data-ttu-id="e3384-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3384-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3384-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3384-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3384-140">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e3384-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="e3384-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e3384-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
