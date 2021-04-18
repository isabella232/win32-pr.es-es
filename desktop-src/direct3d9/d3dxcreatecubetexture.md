---
description: Crea una textura de cubo vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Función D3DXCreateCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721540"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="48dcd-103">D3DXCreateCubeTexture función)</span><span class="sxs-lookup"><span data-stu-id="48dcd-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="48dcd-104">Crea una textura de cubo vacía, ajustando los parámetros de llamada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="48dcd-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="48dcd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48dcd-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="48dcd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48dcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48dcd-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="48dcd-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="48dcd-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-110">*Tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48dcd-112">Ancho y alto de la textura del cubo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="48dcd-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="48dcd-113">Por ejemplo, si la textura del cubo es un cubo de 8 píxeles por 8 píxeles, el valor de este parámetro debe ser 8.</span><span class="sxs-lookup"><span data-stu-id="48dcd-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-114">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48dcd-116">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="48dcd-116">Number of mip levels requested.</span></span> <span data-ttu-id="48dcd-117">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="48dcd-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-118">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48dcd-120">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="48dcd-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="48dcd-121">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="48dcd-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="48dcd-122">Después, el recurso se puede pasar al parámetro *pNewRenderTarget* del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="48dcd-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="48dcd-123">Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="48dcd-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="48dcd-124">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="48dcd-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-125">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-126">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="48dcd-127">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="48dcd-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="48dcd-128">La textura del cubo devuelto puede tener un formato diferente al especificado por *Format*.</span><span class="sxs-lookup"><span data-stu-id="48dcd-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="48dcd-129">Las aplicaciones deben comprobar el formato de la textura del cubo devuelta.</span><span class="sxs-lookup"><span data-stu-id="48dcd-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-130">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-131">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="48dcd-132">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="48dcd-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="48dcd-133">*ppCubeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48dcd-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcd-134">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="48dcd-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="48dcd-135">Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.</span><span class="sxs-lookup"><span data-stu-id="48dcd-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48dcd-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48dcd-136">Return value</span></span>

<span data-ttu-id="48dcd-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48dcd-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48dcd-138">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48dcd-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48dcd-139">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="48dcd-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="48dcd-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48dcd-140">Remarks</span></span>

<span data-ttu-id="48dcd-141">Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.</span><span class="sxs-lookup"><span data-stu-id="48dcd-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="48dcd-142">Internamente, D3DXCreateCubeTexture usa [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) para ajustar los parámetros de llamada.</span><span class="sxs-lookup"><span data-stu-id="48dcd-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="48dcd-143">Por lo tanto, las llamadas a D3DXCreateCubeTexture se realizarán con frecuencia cuando se produzca un error en las llamadas a [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="48dcd-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="48dcd-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48dcd-144">Requirements</span></span>



| <span data-ttu-id="48dcd-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="48dcd-145">Requirement</span></span> | <span data-ttu-id="48dcd-146">Value</span><span class="sxs-lookup"><span data-stu-id="48dcd-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48dcd-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48dcd-147">Header</span></span><br/>  | <dl> <span data-ttu-id="48dcd-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="48dcd-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="48dcd-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48dcd-149">Library</span></span><br/> | <dl> <span data-ttu-id="48dcd-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48dcd-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="48dcd-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="48dcd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dcd-152">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="48dcd-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
