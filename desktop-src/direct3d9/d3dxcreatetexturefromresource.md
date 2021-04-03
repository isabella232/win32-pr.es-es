---
description: Crea una textura a partir de un recurso.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: Función D3DXCreateTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914721"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="9c156-103">D3DXCreateTextureFromResource función)</span><span class="sxs-lookup"><span data-stu-id="9c156-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="9c156-104">Crea una textura a partir de un recurso.</span><span class="sxs-lookup"><span data-stu-id="9c156-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c156-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c156-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="9c156-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c156-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c156-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c156-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c156-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9c156-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9c156-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="9c156-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="9c156-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c156-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c156-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c156-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c156-112">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="9c156-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="9c156-113">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c156-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c156-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c156-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c156-115">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="9c156-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="9c156-116">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9c156-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9c156-117">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9c156-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="9c156-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c156-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9c156-119">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c156-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c156-120">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="9c156-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="9c156-121">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="9c156-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c156-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c156-122">Return value</span></span>

<span data-ttu-id="9c156-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c156-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c156-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c156-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9c156-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9c156-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c156-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c156-126">Remarks</span></span>

<span data-ttu-id="9c156-127">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="9c156-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9c156-128">Si se define Unicode, la llamada de función se resuelve como D3DXCreateTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="9c156-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="9c156-129">De lo contrario, la llamada de función se resuelve como D3DXCreateTextureFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="9c156-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="9c156-130">La función es equivalente a D3DXCreateTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, d3dx \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, d3dx default, \_ 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="9c156-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="9c156-131">El recurso que se está cargando debe ser de tipo RT \_ Bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="9c156-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="9c156-132">El tipo de recurso RT \_ RCDATA se usa para cargar formatos distintos de los mapas de bits (como. TGA,. jpg y. DDS).</span><span class="sxs-lookup"><span data-stu-id="9c156-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="9c156-133">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="9c156-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="9c156-134">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="9c156-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="9c156-135">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="9c156-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="9c156-136">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="9c156-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="9c156-137">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="9c156-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="9c156-138">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9c156-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c156-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c156-139">Requirements</span></span>



| <span data-ttu-id="9c156-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c156-140">Requirement</span></span> | <span data-ttu-id="9c156-141">Value</span><span class="sxs-lookup"><span data-stu-id="9c156-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c156-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c156-142">Header</span></span><br/>  | <dl> <span data-ttu-id="9c156-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c156-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9c156-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c156-144">Library</span></span><br/> | <dl> <span data-ttu-id="9c156-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c156-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9c156-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c156-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c156-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="9c156-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="9c156-148">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="9c156-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
