---
description: Crea una textura de cubo a partir de un recurso.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: Función D3DXCreateCubeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721474"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="2ca7f-103">D3DXCreateCubeTextureFromResource función)</span><span class="sxs-lookup"><span data-stu-id="2ca7f-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="2ca7f-104">Crea una textura de cubo a partir de un recurso.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ca7f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2ca7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ca7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca7f-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ca7f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca7f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ca7f-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="2ca7f-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ca7f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca7f-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ca7f-112">Identificador del módulo en el que se encuentra el recurso, o **null** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="2ca7f-113">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ca7f-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca7f-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ca7f-115">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="2ca7f-116">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2ca7f-117">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2ca7f-118">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2ca7f-119">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ca7f-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca7f-120">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2ca7f-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="2ca7f-121">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca7f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ca7f-122">Return value</span></span>

<span data-ttu-id="2ca7f-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ca7f-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ca7f-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca7f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ca7f-126">Remarks</span></span>

<span data-ttu-id="2ca7f-127">La configuración del compilador determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="2ca7f-128">Si se define Unicode, la llamada de función se resuelve como **D3DXCreateCubeTextureFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="2ca7f-129">De lo contrario, la llamada de función se resuelve como **D3DXCreateCubeTextureFromResourceA** porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="2ca7f-130">La función es equivalente a D3DXCreateCubeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="2ca7f-131">Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2ca7f-132">Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2ca7f-133">Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="2ca7f-134">Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="2ca7f-135">El filtrado se aplica automáticamente a una textura creada con este método.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="2ca7f-136">El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="2ca7f-137">**D3DXCreateCubeTextureFromResource** usa el formato de archivo de DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2ca7f-138">El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="2ca7f-139">Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="2ca7f-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="2ca7f-140">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="2ca7f-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca7f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca7f-141">Requirements</span></span>



| <span data-ttu-id="2ca7f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca7f-142">Requirement</span></span> | <span data-ttu-id="2ca7f-143">Value</span><span class="sxs-lookup"><span data-stu-id="2ca7f-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca7f-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ca7f-144">Header</span></span><br/>  | <dl> <span data-ttu-id="2ca7f-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca7f-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2ca7f-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ca7f-146">Library</span></span><br/> | <dl> <span data-ttu-id="2ca7f-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ca7f-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2ca7f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ca7f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca7f-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="2ca7f-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="2ca7f-150">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2ca7f-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
