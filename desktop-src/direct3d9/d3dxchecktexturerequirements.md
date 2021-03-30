---
description: Comprueba los parámetros de creación de textura.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Función D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280364"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="0f986-103">D3DXCheckTextureRequirements función)</span><span class="sxs-lookup"><span data-stu-id="0f986-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="0f986-104">Comprueba los parámetros de creación de textura.</span><span class="sxs-lookup"><span data-stu-id="0f986-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f986-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f986-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="0f986-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f986-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f986-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0f986-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0f986-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.</span><span class="sxs-lookup"><span data-stu-id="0f986-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="0f986-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f986-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f986-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0f986-112">Puntero al ancho solicitado en píxeles o **null**.</span><span class="sxs-lookup"><span data-stu-id="0f986-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="0f986-113">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="0f986-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="0f986-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f986-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f986-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0f986-116">Puntero al alto solicitado en píxeles o **null**.</span><span class="sxs-lookup"><span data-stu-id="0f986-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="0f986-117">Devuelve el tamaño corregido.</span><span class="sxs-lookup"><span data-stu-id="0f986-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="0f986-118">*pNumMipLevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f986-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f986-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0f986-120">Puntero al número de niveles de mipmap solicitados o **null**.</span><span class="sxs-lookup"><span data-stu-id="0f986-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="0f986-121">Devuelve el número corregido de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0f986-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="0f986-122">*Uso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f986-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f986-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f986-124">0 o [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="0f986-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="0f986-125">Al establecer esta marca en D3DUSAGE \_ RENDERTARGET, se indica que la superficie se va a usar como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0f986-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="0f986-126">Después, el recurso se puede pasar al parámetro pNewRenderTarget del método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0f986-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0f986-127">Si se especifica **D3DUSAGE \_ RENDERTARGET** , la aplicación debe comprobar que el dispositivo admite esta operación llamando a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="0f986-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="0f986-128">*pFormat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f986-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-129">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f986-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="0f986-130">Puntero a un miembro del tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0f986-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="0f986-131">Especifica el formato de píxel deseado o **null**.</span><span class="sxs-lookup"><span data-stu-id="0f986-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="0f986-132">Devuelve el formato corregido.</span><span class="sxs-lookup"><span data-stu-id="0f986-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="0f986-133">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f986-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f986-134">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="0f986-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="0f986-135">Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que describe la clase de memoria en la que se debe colocar la textura.</span><span class="sxs-lookup"><span data-stu-id="0f986-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f986-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f986-136">Return value</span></span>

<span data-ttu-id="0f986-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f986-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f986-138">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f986-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f986-139">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0f986-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f986-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f986-140">Remarks</span></span>

<span data-ttu-id="0f986-141">Si los parámetros de esta función no son válidos, esta función devuelve los parámetros corregidos.</span><span class="sxs-lookup"><span data-stu-id="0f986-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="0f986-142">Esta función usa la heurística siguiente al comparar los requisitos solicitados con los formatos disponibles:</span><span class="sxs-lookup"><span data-stu-id="0f986-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="0f986-143">No elija un formato que tenga menos canales.</span><span class="sxs-lookup"><span data-stu-id="0f986-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="0f986-144">Evite los formatos [FourCC](d3dformat.md) y de 24 bits a menos que se solicite explícitamente.</span><span class="sxs-lookup"><span data-stu-id="0f986-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="0f986-145">Intente no agregar nuevos canales.</span><span class="sxs-lookup"><span data-stu-id="0f986-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="0f986-146">Intente no cambiar el número de bits por canal.</span><span class="sxs-lookup"><span data-stu-id="0f986-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="0f986-147">Intente evitar la conversión entre tipos de formatos.</span><span class="sxs-lookup"><span data-stu-id="0f986-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="0f986-148">Por ejemplo, evite convertir un formato ARGB a un formato de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0f986-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f986-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f986-149">Requirements</span></span>



| <span data-ttu-id="0f986-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f986-150">Requirement</span></span> | <span data-ttu-id="0f986-151">Value</span><span class="sxs-lookup"><span data-stu-id="0f986-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f986-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f986-152">Header</span></span><br/>  | <dl> <span data-ttu-id="0f986-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f986-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0f986-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f986-154">Library</span></span><br/> | <dl> <span data-ttu-id="0f986-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f986-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0f986-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f986-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f986-157">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0f986-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
