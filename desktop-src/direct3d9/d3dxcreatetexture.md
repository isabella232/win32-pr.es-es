---
description: Crea una textura vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Función D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547915"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="92cc4-103">D3DXCreateTexture función)</span><span class="sxs-lookup"><span data-stu-id="92cc4-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="92cc4-104">Crea una textura vacía, ajustando los parámetros de llamada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="92cc4-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cc4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92cc4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="92cc4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92cc4-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="92cc4-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="92cc4-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-110">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92cc4-112">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="92cc4-112">Width in pixels.</span></span> <span data-ttu-id="92cc4-113">Si este valor es 0, se utiliza un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="92cc4-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="92cc4-114">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="92cc4-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-115">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92cc4-117">Alto en píxeles.</span><span class="sxs-lookup"><span data-stu-id="92cc4-117">Height in pixels.</span></span> <span data-ttu-id="92cc4-118">Si este valor es 0, se utiliza un valor de 1.</span><span class="sxs-lookup"><span data-stu-id="92cc4-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="92cc4-119">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="92cc4-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-120">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92cc4-122">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="92cc4-122">Number of mip levels requested.</span></span> <span data-ttu-id="92cc4-123">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="92cc4-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-124">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92cc4-126">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="92cc4-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="92cc4-127">Al establecer esta marca en **D3DUSAGE \_ RENDERTARGET** , se indica que la superficie se va a usar como destino de representación llamando al método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="92cc4-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="92cc4-128">Si se especifica **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , la aplicación debe comprobar que el dispositivo admite esta operación mediante una llamada a [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="92cc4-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="92cc4-129">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="92cc4-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-130">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-131">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="92cc4-132">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura.</span><span class="sxs-lookup"><span data-stu-id="92cc4-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="92cc4-133">La textura devuelta puede tener un formato diferente al especificado, si el dispositivo no admite el formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="92cc4-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="92cc4-134">Las aplicaciones deben comprobar el formato de la textura devuelta para ver si coincide con el formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="92cc4-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-135">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-136">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="92cc4-137">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="92cc4-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="92cc4-138">*ppTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92cc4-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92cc4-139">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="92cc4-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="92cc4-140">Dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="92cc4-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92cc4-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92cc4-141">Return value</span></span>

<span data-ttu-id="92cc4-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="92cc4-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="92cc4-143">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="92cc4-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92cc4-144">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="92cc4-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="92cc4-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92cc4-145">Remarks</span></span>

<span data-ttu-id="92cc4-146">Internamente, D3DXCreateTexture usa [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para ajustar los parámetros de llamada.</span><span class="sxs-lookup"><span data-stu-id="92cc4-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="92cc4-147">Por lo tanto, las llamadas a D3DXCreateTexture se realizarán con frecuencia cuando se produzca un error en las llamadas a [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) .</span><span class="sxs-lookup"><span data-stu-id="92cc4-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="92cc4-148">Si el alto y el ancho se establecen en el valor [ \_ predeterminado de D3DX](other-d3dx-constants.md), se usa un valor de 256 para ambos parámetros.</span><span class="sxs-lookup"><span data-stu-id="92cc4-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="92cc4-149">Si el alto o el ancho se establece en \_ el valor predeterminado de D3DX y el otro parámetro se establece en un valor numérico, la textura será cuadrada con el alto y el ancho equivalentes al valor numérico.</span><span class="sxs-lookup"><span data-stu-id="92cc4-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="92cc4-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92cc4-150">Requirements</span></span>



| <span data-ttu-id="92cc4-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="92cc4-151">Requirement</span></span> | <span data-ttu-id="92cc4-152">Value</span><span class="sxs-lookup"><span data-stu-id="92cc4-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92cc4-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92cc4-153">Header</span></span><br/>  | <dl> <span data-ttu-id="92cc4-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="92cc4-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="92cc4-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92cc4-155">Library</span></span><br/> | <dl> <span data-ttu-id="92cc4-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92cc4-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="92cc4-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="92cc4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92cc4-158">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="92cc4-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
