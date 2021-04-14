---
description: Crea una textura a partir de un archivo.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Función D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424396"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="3f511-103">D3DXCreateTextureFromFile función)</span><span class="sxs-lookup"><span data-stu-id="3f511-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="3f511-104">Crea una textura a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="3f511-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f511-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f511-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="3f511-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f511-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f511-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f511-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3f511-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3f511-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="3f511-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="3f511-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f511-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f511-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f511-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f511-112">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3f511-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="3f511-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3f511-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3f511-114">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3f511-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3f511-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3f511-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3f511-116">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f511-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f511-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="3f511-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="3f511-118">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="3f511-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f511-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f511-119">Return value</span></span>

<span data-ttu-id="3f511-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f511-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f511-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f511-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3f511-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3f511-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f511-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f511-123">Remarks</span></span>

<span data-ttu-id="3f511-124">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="3f511-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3f511-125">Si se define Unicode, la llamada de función se resuelve como D3DXCreateTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="3f511-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="3f511-126">De lo contrario, la llamada de función se resuelve como D3DXCreateTextureFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="3f511-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="3f511-127">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="3f511-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="3f511-128">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="3f511-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="3f511-129">La función es equivalente a D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, d3dx \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, d3dx \_ default, 0, **null**, null, ppTexture). </span><span class="sxs-lookup"><span data-stu-id="3f511-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="3f511-130">Las texturas de Mipmapped automáticamente tienen cada nivel rellenado con la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="3f511-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="3f511-131">Al cargar imágenes en texturas de mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="3f511-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="3f511-132">Si esto ocurre, es necesario cargar las imágenes manualmente.</span><span class="sxs-lookup"><span data-stu-id="3f511-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="3f511-133">Tenga en cuenta que un recurso creado con esta función se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="3f511-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="3f511-134">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="3f511-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="3f511-135">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3f511-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="3f511-136">Para obtener el mejor rendimiento cuando se usa **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="3f511-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="3f511-137">El escalado de imágenes y la conversión de formato en tiempo de carga puede ser lento.</span><span class="sxs-lookup"><span data-stu-id="3f511-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="3f511-138">Almacenar imágenes en el formato y la resolución que se usarán.</span><span class="sxs-lookup"><span data-stu-id="3f511-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="3f511-139">Si el hardware de destino requiere la potencia de dos dimensiones, cree y almacene imágenes con la potencia de dos dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3f511-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="3f511-140">Considere la posibilidad de usar archivos de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="3f511-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="3f511-141">Dado que los archivos DDS se pueden usar para representar cualquier formato de textura de Direct3D 9, son muy fáciles de leer en D3DX.</span><span class="sxs-lookup"><span data-stu-id="3f511-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="3f511-142">Además, pueden almacenar mapas MIP, por lo que los algoritmos de generación de mipmap se pueden usar para crear las imágenes.</span><span class="sxs-lookup"><span data-stu-id="3f511-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f511-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f511-143">Requirements</span></span>



| <span data-ttu-id="3f511-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f511-144">Requirement</span></span> | <span data-ttu-id="3f511-145">Value</span><span class="sxs-lookup"><span data-stu-id="3f511-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f511-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f511-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3f511-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f511-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3f511-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f511-148">Library</span></span><br/> | <dl> <span data-ttu-id="3f511-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f511-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3f511-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f511-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f511-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="3f511-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="3f511-152">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="3f511-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
