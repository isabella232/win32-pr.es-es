---
description: 'Función D3DXCreateVolumeTextureFromFile: crea una textura de volumen a partir de un archivo.'
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: Función D3DXCreateVolumeTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094312"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="ea338-103">Función D3DXCreateVolumeTextureFromFile</span><span class="sxs-lookup"><span data-stu-id="ea338-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="ea338-104">Crea una textura de volumen a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="ea338-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea338-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea338-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ea338-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea338-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea338-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea338-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ea338-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ea338-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="ea338-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ea338-110">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea338-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea338-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea338-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea338-112">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="ea338-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="ea338-113">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea338-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ea338-114">De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ea338-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ea338-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ea338-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea338-116">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea338-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea338-117">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ea338-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ea338-118">Dirección de un puntero a una [**interfaz IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="ea338-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea338-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea338-119">Return value</span></span>

<span data-ttu-id="ea338-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea338-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea338-121">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea338-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea338-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ea338-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea338-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea338-123">Remarks</span></span>

<span data-ttu-id="ea338-124">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="ea338-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ea338-125">Si se define Unicode, la llamada a la función se resuelve en D3DXCreateVolumeTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="ea338-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="ea338-126">De lo contrario, la llamada de función se resuelve en D3DXCreateVolumeTextureFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea338-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="ea338-127">La función es equivalente a D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, \_ D3DX DEFAULT, D3DX \_ DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="ea338-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="ea338-128">Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga.</span><span class="sxs-lookup"><span data-stu-id="ea338-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ea338-129">Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ea338-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ea338-130">Las texturas mipmapped rellenan automáticamente cada nivel con la textura cargada.</span><span class="sxs-lookup"><span data-stu-id="ea338-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="ea338-131">Al cargar imágenes en texturas mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="ea338-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="ea338-132">Si esto sucede, las imágenes deben cargarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="ea338-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="ea338-133">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria que D3DPOOL \_ MANAGED indica.</span><span class="sxs-lookup"><span data-stu-id="ea338-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="ea338-134">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria que indica D3DPOOL \_ DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="ea338-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="ea338-135">El filtrado se aplica automáticamente a una textura creada mediante este método.</span><span class="sxs-lookup"><span data-stu-id="ea338-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="ea338-136">El filtrado es equivalente a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER en [D3DX \_ FILTER](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ea338-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea338-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea338-137">Requirements</span></span>



| <span data-ttu-id="ea338-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea338-138">Requirement</span></span> | <span data-ttu-id="ea338-139">Value</span><span class="sxs-lookup"><span data-stu-id="ea338-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea338-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea338-140">Header</span></span><br/>  | <dl> <span data-ttu-id="ea338-141"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea338-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ea338-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea338-142">Library</span></span><br/> | <dl> <span data-ttu-id="ea338-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea338-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ea338-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea338-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea338-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="ea338-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="ea338-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ea338-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ea338-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ea338-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="ea338-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="ea338-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="ea338-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="ea338-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="ea338-150">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ea338-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
