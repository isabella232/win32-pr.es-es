---
description: Crea una textura de cubo a partir de un archivo en memoria.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Función D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721476"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="79fe0-103">D3DXCreateCubeTextureFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="79fe0-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="79fe0-104">Crea una textura de cubo a partir de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="79fe0-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fe0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79fe0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="79fe0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79fe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fe0-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fe0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fe0-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="79fe0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="79fe0-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="79fe0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="79fe0-110">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fe0-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fe0-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79fe0-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79fe0-112">Puntero al archivo en la memoria desde el que se va a crear el mapa.</span><span class="sxs-lookup"><span data-stu-id="79fe0-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="79fe0-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="79fe0-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="79fe0-114">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79fe0-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fe0-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79fe0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79fe0-116">Tamaño del archivo en memoria, en bytes.</span><span class="sxs-lookup"><span data-stu-id="79fe0-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79fe0-117">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79fe0-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79fe0-118">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="79fe0-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="79fe0-119">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="79fe0-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fe0-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79fe0-120">Return value</span></span>

<span data-ttu-id="79fe0-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79fe0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79fe0-122">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79fe0-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="79fe0-123">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="79fe0-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="79fe0-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79fe0-124">Remarks</span></span>

<span data-ttu-id="79fe0-125">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="79fe0-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="79fe0-126">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="79fe0-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="79fe0-127">La función es equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="79fe0-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="79fe0-128">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="79fe0-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="79fe0-129">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="79fe0-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="79fe0-130">Este método se ha diseñado para que se use para cargar archivos de imagen almacenados como RT \_ RCDATA, que es un recurso definido por la aplicación (datos sin procesar).</span><span class="sxs-lookup"><span data-stu-id="79fe0-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="79fe0-131">De lo contrario, se producirá un error en este método.</span><span class="sxs-lookup"><span data-stu-id="79fe0-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="79fe0-132">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="79fe0-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="79fe0-133">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="79fe0-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="79fe0-134">**D3DXCreateCubeTextureFromFileInMemory** usa el formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="79fe0-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="79fe0-135">El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="79fe0-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="79fe0-136">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="79fe0-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="79fe0-137">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="79fe0-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79fe0-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79fe0-138">Requirements</span></span>



| <span data-ttu-id="79fe0-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fe0-139">Requirement</span></span> | <span data-ttu-id="79fe0-140">Value</span><span class="sxs-lookup"><span data-stu-id="79fe0-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79fe0-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79fe0-141">Header</span></span><br/>  | <dl> <span data-ttu-id="79fe0-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="79fe0-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="79fe0-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79fe0-143">Library</span></span><br/> | <dl> <span data-ttu-id="79fe0-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79fe0-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="79fe0-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="79fe0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fe0-146">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="79fe0-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
