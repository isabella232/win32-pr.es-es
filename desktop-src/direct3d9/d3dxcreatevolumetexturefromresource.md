---
description: Crea una textura de volumen a partir de un recurso.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: Función D3DXCreateVolumeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547902"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="cb3f1-103">D3DXCreateVolumeTextureFromResource función)</span><span class="sxs-lookup"><span data-stu-id="cb3f1-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="cb3f1-104">Crea una textura de volumen a partir de un recurso.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3f1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb3f1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="cb3f1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb3f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3f1-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3f1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f1-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cb3f1-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f1-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3f1-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f1-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f1-112">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f1-113">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3f1-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f1-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3f1-115">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="cb3f1-116">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cb3f1-117">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="cb3f1-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cb3f1-119">*ppVolumeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb3f1-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3f1-120">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="cb3f1-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="cb3f1-121">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3f1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb3f1-122">Return value</span></span>

<span data-ttu-id="cb3f1-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb3f1-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb3f1-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3f1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb3f1-126">Remarks</span></span>

<span data-ttu-id="cb3f1-127">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="cb3f1-128">Si se define Unicode, la llamada de función se resuelve como D3DXCreateVolumeTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="cb3f1-129">De lo contrario, la llamada de función se resuelve como D3DXCreateVolumeTextureFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="cb3f1-130">La función es equivalente a D3DXCreateVolumeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, valor predeterminado de d3dx, valor predeterminado de d3dx \_ , default \_ \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ MANaged, d3dx \_ default, d3dx default \_ , 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="cb3f1-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="cb3f1-131">El recurso que se está cargando debe ser un recurso definido por la aplicación (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="cb3f1-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="cb3f1-132">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="cb3f1-133">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="cb3f1-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="cb3f1-134">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="cb3f1-135">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="cb3f1-136">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="cb3f1-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="cb3f1-137">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cb3f1-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3f1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb3f1-138">Requirements</span></span>



| <span data-ttu-id="cb3f1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3f1-139">Requirement</span></span> | <span data-ttu-id="cb3f1-140">Value</span><span class="sxs-lookup"><span data-stu-id="cb3f1-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3f1-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb3f1-141">Header</span></span><br/>  | <dl> <span data-ttu-id="cb3f1-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f1-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cb3f1-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb3f1-143">Library</span></span><br/> | <dl> <span data-ttu-id="cb3f1-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f1-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cb3f1-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb3f1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3f1-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="cb3f1-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="cb3f1-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="cb3f1-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="cb3f1-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="cb3f1-151">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="cb3f1-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
