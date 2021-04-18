---
description: Se utiliza para establecer y consultar los efectos, y para elegir técnicas. Un objeto Effect puede contener varias técnicas para representar el mismo efecto.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interfaz ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707790"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="1addb-104">Interfaz ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="1addb-104">ID3DXEffect interface</span></span>

<span data-ttu-id="1addb-105">Se utiliza para establecer y consultar los efectos, y para elegir técnicas.</span><span class="sxs-lookup"><span data-stu-id="1addb-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="1addb-106">Un objeto Effect puede contener varias técnicas para representar el mismo efecto.</span><span class="sxs-lookup"><span data-stu-id="1addb-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="1addb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1addb-107">Members</span></span>

<span data-ttu-id="1addb-108">La interfaz **ID3DXEffect** hereda de [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="1addb-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="1addb-109">**ID3DXEffect** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1addb-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="1addb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1addb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1addb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1addb-111">Methods</span></span>

<span data-ttu-id="1addb-112">La interfaz **ID3DXEffect** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1addb-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="1addb-113">Método</span><span class="sxs-lookup"><span data-stu-id="1addb-113">Method</span></span>                                                                | <span data-ttu-id="1addb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1addb-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1addb-115">**ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="1addb-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="1addb-116">Aplique los valores de un bloque de estado al estado del sistema de efecto actual.</span><span class="sxs-lookup"><span data-stu-id="1addb-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="1addb-117">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="1addb-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="1addb-118">Inicia una técnica activa.</span><span class="sxs-lookup"><span data-stu-id="1addb-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="1addb-119">**BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="1addb-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="1addb-120">Iniciar captura de cambios de estado en un bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="1addb-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1addb-121">**BeginPass**</span><span class="sxs-lookup"><span data-stu-id="1addb-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="1addb-122">Comienza un paso, dentro de la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="1addb-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="1addb-123">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="1addb-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="1addb-124">Crea una copia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="1addb-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="1addb-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="1addb-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="1addb-126">Propaga los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="1addb-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1addb-127">**DeleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="1addb-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="1addb-128">Elimine un bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="1addb-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="1addb-129">**Fin**</span><span class="sxs-lookup"><span data-stu-id="1addb-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="1addb-130">Finaliza una técnica activa.</span><span class="sxs-lookup"><span data-stu-id="1addb-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="1addb-131">**EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="1addb-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="1addb-132">Detiene la captura de cambios de estado de parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="1addb-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="1addb-133">**EndPass**</span><span class="sxs-lookup"><span data-stu-id="1addb-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="1addb-134">Finaliza un paso activo.</span><span class="sxs-lookup"><span data-stu-id="1addb-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="1addb-135">**FindNextValidTechnique**</span><span class="sxs-lookup"><span data-stu-id="1addb-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="1addb-136">Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.</span><span class="sxs-lookup"><span data-stu-id="1addb-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="1addb-137">**GetCurrentTechnique**</span><span class="sxs-lookup"><span data-stu-id="1addb-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="1addb-138">Obtiene la técnica actual.</span><span class="sxs-lookup"><span data-stu-id="1addb-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="1addb-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="1addb-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="1addb-140">Recupera el dispositivo asociado al efecto.</span><span class="sxs-lookup"><span data-stu-id="1addb-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1addb-141">**GetPool**</span><span class="sxs-lookup"><span data-stu-id="1addb-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="1addb-142">Obtiene un puntero al grupo de parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="1addb-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="1addb-143">**GetStateManager**</span><span class="sxs-lookup"><span data-stu-id="1addb-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="1addb-144">Obtiene el efecto administrador de estado.</span><span class="sxs-lookup"><span data-stu-id="1addb-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="1addb-145">**IsParameterUsed**</span><span class="sxs-lookup"><span data-stu-id="1addb-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="1addb-146">Determina si la técnica utiliza un parámetro.</span><span class="sxs-lookup"><span data-stu-id="1addb-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1addb-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="1addb-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="1addb-148">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="1addb-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="1addb-149">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1addb-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="1addb-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="1addb-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="1addb-151">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="1addb-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="1addb-152">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="1addb-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="1addb-153">Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.</span><span class="sxs-lookup"><span data-stu-id="1addb-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1addb-154">**SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="1addb-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="1addb-155">Establezca el efecto administrador de estado.</span><span class="sxs-lookup"><span data-stu-id="1addb-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="1addb-156">**SetTechnique**</span><span class="sxs-lookup"><span data-stu-id="1addb-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="1addb-157">Establece la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="1addb-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="1addb-158">**ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="1addb-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="1addb-159">Validar una técnica.</span><span class="sxs-lookup"><span data-stu-id="1addb-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="1addb-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1addb-160">Remarks</span></span>

<span data-ttu-id="1addb-161">La interfaz ID3DXEffect se obtiene llamando a [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)o [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="1addb-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="1addb-162">El tipo LPD3DXEFFECT se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="1addb-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="1addb-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1addb-163">Requirements</span></span>



| <span data-ttu-id="1addb-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="1addb-164">Requirement</span></span> | <span data-ttu-id="1addb-165">Value</span><span class="sxs-lookup"><span data-stu-id="1addb-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1addb-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1addb-166">Header</span></span><br/>  | <dl> <span data-ttu-id="1addb-167"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1addb-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1addb-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1addb-168">Library</span></span><br/> | <dl> <span data-ttu-id="1addb-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1addb-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1addb-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="1addb-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1addb-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="1addb-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1addb-172">Interfaces de efectos</span><span class="sxs-lookup"><span data-stu-id="1addb-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1addb-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="1addb-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="1addb-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="1addb-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="1addb-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="1addb-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




