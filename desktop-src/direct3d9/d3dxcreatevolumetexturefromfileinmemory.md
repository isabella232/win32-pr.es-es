---
description: Crea una textura de volumen a partir de un archivo en memoria.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: Función D3DXCreateVolumeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821103"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a><span data-ttu-id="55ad4-103">D3DXCreateVolumeTextureFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="55ad4-103">D3DXCreateVolumeTextureFromFileInMemory function</span></span>

<span data-ttu-id="55ad4-104">Crea una textura de volumen a partir de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="55ad4-104">Creates a volume texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ad4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55ad4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="55ad4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55ad4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ad4-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55ad4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ad4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="55ad4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="55ad4-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="55ad4-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="55ad4-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55ad4-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ad4-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55ad4-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55ad4-112">Puntero al archivo en la memoria desde el que se va a crear la textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="55ad4-112">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="55ad4-113">*SrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55ad4-113">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ad4-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55ad4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55ad4-115">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="55ad4-115">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="55ad4-116">*ppVolumeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55ad4-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55ad4-117">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="55ad4-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="55ad4-118">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="55ad4-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ad4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55ad4-119">Return value</span></span>

<span data-ttu-id="55ad4-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55ad4-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55ad4-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55ad4-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="55ad4-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="55ad4-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ad4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55ad4-123">Remarks</span></span>

<span data-ttu-id="55ad4-124">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="55ad4-124">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="55ad4-125">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="55ad4-125">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="55ad4-126">La función es equivalente a D3DXCreateVolumeTextureFromFileInMemoryEx (pDevice, pSrcFile, SrcData, D3DX \_ default, valor predeterminado de d3dx, valor predeterminado de d3dx \_ , default \_ \_ , 0, D3DFMT \_ Unknown, D3DPOOL \_ MANaged, d3dx \_ default, d3dx default \_ , 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="55ad4-126">The function is equivalent to D3DXCreateVolumeTextureFromFileInMemoryEx(pDevice, pSrcFile, SrcData, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="55ad4-127">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="55ad4-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="55ad4-128">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="55ad4-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="55ad4-129">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="55ad4-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="55ad4-130">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="55ad4-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55ad4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55ad4-131">Requirements</span></span>



| <span data-ttu-id="55ad4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ad4-132">Requirement</span></span> | <span data-ttu-id="55ad4-133">Value</span><span class="sxs-lookup"><span data-stu-id="55ad4-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55ad4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55ad4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="55ad4-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ad4-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="55ad4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55ad4-136">Library</span></span><br/> | <dl> <span data-ttu-id="55ad4-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55ad4-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="55ad4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="55ad4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ad4-139">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="55ad4-139">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="55ad4-140">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="55ad4-140">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="55ad4-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="55ad4-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="55ad4-142">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="55ad4-142">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="55ad4-143">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="55ad4-143">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="55ad4-144">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="55ad4-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
