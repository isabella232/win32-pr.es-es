---
description: Se trata de una interfaz implementada por el usuario que permite a un usuario establecer el estado del dispositivo de un efecto.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interfaz ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362645"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="0ccb6-103">Interfaz ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0ccb6-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="0ccb6-104">Se trata de una interfaz implementada por el usuario que permite a un usuario establecer el estado del dispositivo de un efecto.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="0ccb6-105">El usuario debe implementar cada uno de los métodos de esta interfaz y, a continuación, se usarán como devoluciones de llamada a la aplicación cuando se produzca cualquiera de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="0ccb6-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="0ccb6-106">Un efecto llama a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="0ccb6-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0ccb6-107">El estado del efecto se actualiza dinámicamente mediante una llamada a la API de cambio de estado adecuada.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="0ccb6-108">Consulte páginas de método individuales para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-108">See individual method pages for details.</span></span>

<span data-ttu-id="0ccb6-109">Cuando una aplicación utiliza el administrador de estado para implementar devoluciones de llamada personalizadas, un efecto ya no guarda y restaura el estado automáticamente al llamar a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="0ccb6-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="0ccb6-110">Dado que la aplicación ha implementado un comportamiento personalizado de guardar y restaurar en las devoluciones de llamada, se omite este comportamiento automático.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="0ccb6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ccb6-111">Members</span></span>

<span data-ttu-id="0ccb6-112">La interfaz **ID3DXEffectStateManager** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0ccb6-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0ccb6-113">**ID3DXEffectStateManager** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0ccb6-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="0ccb6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ccb6-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ccb6-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0ccb6-115">Methods</span></span>

<span data-ttu-id="0ccb6-116">La interfaz **ID3DXEffectStateManager** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="0ccb6-117">Método</span><span class="sxs-lookup"><span data-stu-id="0ccb6-117">Method</span></span>                                                                                | <span data-ttu-id="0ccb6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ccb6-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ccb6-119">**LightEnable**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="0ccb6-120">Función de devolución de llamada que debe ser implementada por un usuario para habilitar o deshabilitar una luz.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="0ccb6-121">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="0ccb6-122">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un código FVF.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="0ccb6-123">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="0ccb6-124">Función de devolución de llamada que debe ser implementada por un usuario para establecer una luz.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="0ccb6-125">**SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="0ccb6-126">Una función de devolución de llamada que debe ser implementada por un usuario para establecer el estado del material.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="0ccb6-127">**SetNPatchMode**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="0ccb6-128">Una función de devolución de llamada que debe ser implementada por un usuario para establecer el número de segmentos de subdivisión para N-patches.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="0ccb6-129">**SetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="0ccb6-130">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="0ccb6-131">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="0ccb6-132">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="0ccb6-133">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="0ccb6-134">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="0ccb6-135">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="0ccb6-136">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="0ccb6-137">**SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="0ccb6-138">Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="0ccb6-139">**SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="0ccb6-140">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una muestra.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="0ccb6-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="0ccb6-142">Función de devolución de llamada que debe ser implementada por un usuario para establecer una textura.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="0ccb6-143">**SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="0ccb6-144">Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="0ccb6-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="0ccb6-146">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una transformación.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="0ccb6-147">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="0ccb6-148">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="0ccb6-149">**SetVertexShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="0ccb6-150">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="0ccb6-151">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="0ccb6-152">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="0ccb6-153">**SetVertexShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="0ccb6-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="0ccb6-154">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0ccb6-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ccb6-155">Remarks</span></span>

<span data-ttu-id="0ccb6-156">Un usuario crea una interfaz ID3DXEffectStateManager implementando una clase que deriva de esta interfaz e implementando todos los métodos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="0ccb6-157">Una vez creada la interfaz, puede obtener o establecer el administrador de estado dentro de un efecto mediante [**ID3DXEffect:: GetStateManager**](id3dxeffect--getstatemanager.md) y [**ID3DXEffect:: SetStateManager**](id3dxeffect--setstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="0ccb6-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="0ccb6-158">El tipo LPD3DXEFFECTSTATEMANAGER se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0ccb6-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="0ccb6-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ccb6-159">Requirements</span></span>



| <span data-ttu-id="0ccb6-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ccb6-160">Requirement</span></span> | <span data-ttu-id="0ccb6-161">Value</span><span class="sxs-lookup"><span data-stu-id="0ccb6-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ccb6-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ccb6-162">Header</span></span><br/>  | <dl> <span data-ttu-id="0ccb6-163"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ccb6-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0ccb6-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ccb6-164">Library</span></span><br/> | <dl> <span data-ttu-id="0ccb6-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ccb6-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ccb6-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ccb6-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ccb6-167">Interfaces de efectos</span><span class="sxs-lookup"><span data-stu-id="0ccb6-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
