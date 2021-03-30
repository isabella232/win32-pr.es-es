---
description: Guarda un volumen en un búfer. El método crea un búfer ID3DXBuffer para almacenar los datos y devuelve ese objeto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Función D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280303"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="d1f76-104">D3DXSaveVolumeToFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="d1f76-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="d1f76-105">Guarda un volumen en un búfer.</span><span class="sxs-lookup"><span data-stu-id="d1f76-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="d1f76-106">El método crea un búfer [**ID3DXBuffer**](id3dxbuffer.md) para almacenar los datos y devuelve ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d1f76-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f76-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1f76-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="d1f76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1f76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f76-109">*ppDestBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d1f76-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f76-110">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1f76-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d1f76-111">Dirección de un puntero a un búfer de [**ID3DXBuffer**](id3dxbuffer.md) que almacenará la imagen.</span><span class="sxs-lookup"><span data-stu-id="d1f76-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="d1f76-112">*DestFormat* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1f76-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f76-113">Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d1f76-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="d1f76-114">[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar.</span><span class="sxs-lookup"><span data-stu-id="d1f76-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="d1f76-115">Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).</span><span class="sxs-lookup"><span data-stu-id="d1f76-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="d1f76-116">*pSrcVolume* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1f76-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f76-117">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="d1f76-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="d1f76-118">Puntero a la interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contiene la imagen que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="d1f76-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="d1f76-119">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1f76-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f76-120">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d1f76-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d1f76-121">Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores.</span><span class="sxs-lookup"><span data-stu-id="d1f76-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="d1f76-122">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1f76-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d1f76-123">*pSrcBox* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1f76-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f76-124">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1f76-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d1f76-125">Puntero a una estructura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d1f76-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d1f76-126">Especifica el cuadro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="d1f76-126">Specifies the source box.</span></span> <span data-ttu-id="d1f76-127">Establezca este parámetro en **null** para especificar el volumen completo.</span><span class="sxs-lookup"><span data-stu-id="d1f76-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f76-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1f76-128">Return value</span></span>

<span data-ttu-id="d1f76-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1f76-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1f76-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1f76-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1f76-131">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d1f76-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f76-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f76-132">Requirements</span></span>



| <span data-ttu-id="d1f76-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1f76-133">Requirement</span></span> | <span data-ttu-id="d1f76-134">Value</span><span class="sxs-lookup"><span data-stu-id="d1f76-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f76-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1f76-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d1f76-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1f76-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d1f76-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1f76-137">Library</span></span><br/> | <dl> <span data-ttu-id="d1f76-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1f76-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d1f76-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1f76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f76-140">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d1f76-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="d1f76-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="d1f76-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
