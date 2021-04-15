---
description: Comprueba los parámetros de creación de texturas por volumen.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: Función D3DXCheckVolumeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424420"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="e4750-103">D3DXCheckVolumeTextureRequirements función)</span><span class="sxs-lookup"><span data-stu-id="e4750-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="e4750-104">Comprueba los parámetros de creación de texturas por volumen.</span><span class="sxs-lookup"><span data-stu-id="e4750-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4750-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4750-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="e4750-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4750-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4750-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e4750-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e4750-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e4750-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.</span><span class="sxs-lookup"><span data-stu-id="e4750-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4750-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4750-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4750-112">Puntero al ancho solicitado en píxeles o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4750-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="e4750-113">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="e4750-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4750-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4750-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4750-116">Puntero al alto solicitado en píxeles o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4750-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="e4750-117">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="e4750-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-118">*pDepth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4750-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4750-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4750-120">Puntero a la profundidad solicitada en píxeles o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4750-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="e4750-121">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="e4750-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-122">*pNumMipLevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4750-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4750-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4750-124">Puntero al número de niveles de mipmap solicitados, o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4750-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="e4750-125">Devuelve el número corregido de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="e4750-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-126">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e4750-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4750-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4750-128">Actualmente no se usa, se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="e4750-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-129">*pFormat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4750-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-130">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4750-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="e4750-131">Puntero a un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="e4750-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="e4750-132">Especifica el formato de píxel deseado o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4750-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="e4750-133">Devuelve el formato corregido.</span><span class="sxs-lookup"><span data-stu-id="e4750-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="e4750-134">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e4750-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4750-135">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e4750-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e4750-136">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="e4750-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4750-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4750-137">Return value</span></span>

<span data-ttu-id="e4750-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4750-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4750-139">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4750-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4750-140">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e4750-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4750-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4750-141">Remarks</span></span>

<span data-ttu-id="e4750-142">Si los parámetros de esta función no son válidos, esta función devuelve los parámetros corregidos.</span><span class="sxs-lookup"><span data-stu-id="e4750-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4750-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4750-143">Requirements</span></span>



| <span data-ttu-id="e4750-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4750-144">Requirement</span></span> | <span data-ttu-id="e4750-145">Value</span><span class="sxs-lookup"><span data-stu-id="e4750-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4750-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4750-146">Header</span></span><br/>  | <dl> <span data-ttu-id="e4750-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4750-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e4750-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4750-148">Library</span></span><br/> | <dl> <span data-ttu-id="e4750-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4750-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e4750-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4750-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4750-151">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e4750-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
