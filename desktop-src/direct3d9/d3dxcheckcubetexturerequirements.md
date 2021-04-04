---
description: Comprueba los parámetros de creación de texturas de cubo.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Función D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821490"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="563c8-103">D3DXCheckCubeTextureRequirements función)</span><span class="sxs-lookup"><span data-stu-id="563c8-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="563c8-104">Comprueba los parámetros de creación de texturas de cubo.</span><span class="sxs-lookup"><span data-stu-id="563c8-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="563c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="563c8-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="563c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="563c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563c8-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="563c8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="563c8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="563c8-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="563c8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="563c8-110">*pSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="563c8-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="563c8-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="563c8-112">Puntero al ancho y alto solicitados en píxeles, o **null**.</span><span class="sxs-lookup"><span data-stu-id="563c8-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="563c8-113">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="563c8-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="563c8-114">*pNumMipLevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="563c8-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="563c8-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="563c8-116">Puntero al número de niveles de mipmap solicitados, o **null**.</span><span class="sxs-lookup"><span data-stu-id="563c8-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="563c8-117">Devuelve el número corregido de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="563c8-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="563c8-118">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="563c8-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="563c8-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="563c8-120">0 o D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="563c8-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="563c8-121">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="563c8-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="563c8-122">Después, el recurso se puede pasar al parámetro pNewRenderTarget del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="563c8-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="563c8-123">Si \_ se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="563c8-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="563c8-124">*pFormat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="563c8-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-125">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="563c8-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="563c8-126">Puntero a un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="563c8-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="563c8-127">Especifica el formato de píxel deseado o **null**.</span><span class="sxs-lookup"><span data-stu-id="563c8-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="563c8-128">Devuelve el formato corregido.</span><span class="sxs-lookup"><span data-stu-id="563c8-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="563c8-129">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="563c8-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563c8-130">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="563c8-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="563c8-131">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="563c8-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="563c8-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="563c8-132">Return value</span></span>

<span data-ttu-id="563c8-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="563c8-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="563c8-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="563c8-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="563c8-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="563c8-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="563c8-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="563c8-136">Remarks</span></span>

<span data-ttu-id="563c8-137">Si los parámetros de esta función no son válidos, esta función devuelve los parámetros corregidos.</span><span class="sxs-lookup"><span data-stu-id="563c8-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="563c8-138">Las texturas del cubo se diferencian de otras superficies en que son colecciones de superficies.</span><span class="sxs-lookup"><span data-stu-id="563c8-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="563c8-139">Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="563c8-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="563c8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="563c8-140">Requirements</span></span>



| <span data-ttu-id="563c8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="563c8-141">Requirement</span></span> | <span data-ttu-id="563c8-142">Value</span><span class="sxs-lookup"><span data-stu-id="563c8-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="563c8-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="563c8-143">Header</span></span><br/>  | <dl> <span data-ttu-id="563c8-144"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="563c8-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="563c8-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="563c8-145">Library</span></span><br/> | <dl> <span data-ttu-id="563c8-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="563c8-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="563c8-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="563c8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563c8-148">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="563c8-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
