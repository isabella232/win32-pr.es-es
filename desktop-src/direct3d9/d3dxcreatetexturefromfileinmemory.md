---
description: Crea una textura a partir de un archivo en memoria.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: Función D3DXCreateTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821111"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="00503-103">D3DXCreateTextureFromFileInMemory función)</span><span class="sxs-lookup"><span data-stu-id="00503-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="00503-104">Crea una textura a partir de un archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="00503-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="00503-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00503-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="00503-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00503-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00503-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00503-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="00503-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="00503-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="00503-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="00503-110">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00503-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00503-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00503-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00503-112">Puntero al archivo en la memoria desde el que se va a crear la textura.</span><span class="sxs-lookup"><span data-stu-id="00503-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="00503-113">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00503-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00503-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00503-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00503-115">Tamaño en bytes del archivo en memoria.</span><span class="sxs-lookup"><span data-stu-id="00503-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="00503-116">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00503-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00503-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="00503-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="00503-118">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="00503-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00503-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00503-119">Return value</span></span>

<span data-ttu-id="00503-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00503-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00503-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00503-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="00503-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="00503-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="00503-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00503-123">Remarks</span></span>

<span data-ttu-id="00503-124">La función es equivalente a D3DXCreateTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, d3dx \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, d3dx default, \_ 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="00503-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="00503-125">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="00503-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="00503-126">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="00503-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="00503-127">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="00503-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="00503-128">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="00503-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="00503-129">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="00503-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="00503-130">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="00503-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00503-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00503-131">Requirements</span></span>



| <span data-ttu-id="00503-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="00503-132">Requirement</span></span> | <span data-ttu-id="00503-133">Value</span><span class="sxs-lookup"><span data-stu-id="00503-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00503-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00503-134">Header</span></span><br/>  | <dl> <span data-ttu-id="00503-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="00503-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="00503-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00503-136">Library</span></span><br/> | <dl> <span data-ttu-id="00503-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00503-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="00503-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="00503-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00503-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="00503-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="00503-140">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="00503-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
