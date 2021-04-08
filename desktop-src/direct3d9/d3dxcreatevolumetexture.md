---
description: Crea una textura de volumen vacía, ajustando los parámetros de llamada según sea necesario.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Función D3DXCreateVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003821"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="6d29c-103">D3DXCreateVolumeTexture función)</span><span class="sxs-lookup"><span data-stu-id="6d29c-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="6d29c-104">Crea una textura de volumen vacía, ajustando los parámetros de llamada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6d29c-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d29c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d29c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6d29c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d29c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d29c-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6d29c-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="6d29c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-110">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d29c-112">Ancho en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6d29c-112">Width in pixels.</span></span> <span data-ttu-id="6d29c-113">Este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6d29c-113">This value must be nonzero.</span></span> <span data-ttu-id="6d29c-114">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6d29c-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-115">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d29c-117">Alto en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6d29c-117">Height in pixels.</span></span> <span data-ttu-id="6d29c-118">Este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6d29c-118">This value must be nonzero.</span></span> <span data-ttu-id="6d29c-119">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6d29c-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-120">*Nivel de detalle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d29c-122">Profundidad en píxeles.</span><span class="sxs-lookup"><span data-stu-id="6d29c-122">Depth in pixels.</span></span> <span data-ttu-id="6d29c-123">Este valor debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6d29c-123">This value must be nonzero.</span></span> <span data-ttu-id="6d29c-124">La dimensión máxima que admite un controlador (para ancho, alto y profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6d29c-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-125">*MipLevels* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d29c-127">Número de niveles de MIP solicitados.</span><span class="sxs-lookup"><span data-stu-id="6d29c-127">Number of mip levels requested.</span></span> <span data-ttu-id="6d29c-128">Si este valor es cero o el valor predeterminado de D3DX \_ , se crea una cadena de mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="6d29c-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-129">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d29c-131">0 o D3DUSAGE \_ dinámico.</span><span class="sxs-lookup"><span data-stu-id="6d29c-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="6d29c-132">Para obtener más información sobre el uso de texturas dinámicas, vea [usar texturas dinámicas](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="6d29c-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-133">*Formato* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-134">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6d29c-135">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de píxel solicitado para la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="6d29c-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="6d29c-136">La textura de volumen devuelta puede tener un formato diferente al especificado por Format.</span><span class="sxs-lookup"><span data-stu-id="6d29c-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="6d29c-137">Las aplicaciones deben comprobar el formato de la textura de volumen devuelta.</span><span class="sxs-lookup"><span data-stu-id="6d29c-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-138">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-139">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="6d29c-140">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="6d29c-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="6d29c-141">*ppVolumeTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d29c-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d29c-142">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6d29c-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="6d29c-143">Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura de volumen creado.</span><span class="sxs-lookup"><span data-stu-id="6d29c-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d29c-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d29c-144">Return value</span></span>

<span data-ttu-id="6d29c-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d29c-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d29c-146">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d29c-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d29c-147">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6d29c-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="6d29c-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d29c-148">Remarks</span></span>

<span data-ttu-id="6d29c-149">Internamente, D3DXCreateVolumeTexture usa [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) para ajustar los parámetros de llamada.</span><span class="sxs-lookup"><span data-stu-id="6d29c-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="6d29c-150">Por lo tanto, las llamadas a D3DXCreateVolumeTexture se realizarán con frecuencia cuando se produzca un error en las llamadas a [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) .</span><span class="sxs-lookup"><span data-stu-id="6d29c-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d29c-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d29c-151">Requirements</span></span>



| <span data-ttu-id="6d29c-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d29c-152">Requirement</span></span> | <span data-ttu-id="6d29c-153">Value</span><span class="sxs-lookup"><span data-stu-id="6d29c-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d29c-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d29c-154">Header</span></span><br/>  | <dl> <span data-ttu-id="6d29c-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d29c-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6d29c-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d29c-156">Library</span></span><br/> | <dl> <span data-ttu-id="6d29c-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d29c-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6d29c-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d29c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d29c-159">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6d29c-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
