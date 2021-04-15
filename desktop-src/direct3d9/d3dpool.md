---
description: Define la clase de memoria que contiene los búferes de un recurso.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumeración D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649417"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="8668a-103">Enumeración D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="8668a-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="8668a-104">Define la clase de memoria que contiene los búferes de un recurso.</span><span class="sxs-lookup"><span data-stu-id="8668a-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="8668a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8668a-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="8668a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8668a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8668a-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**\_Valor predeterminado de D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="8668a-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="8668a-108">Los recursos se colocan en el bloque de memoria más adecuado para el conjunto de usos solicitado para el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="8668a-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="8668a-109">Suele ser la memoria de vídeo, incluida la memoria de vídeo local y la memoria AGP.</span><span class="sxs-lookup"><span data-stu-id="8668a-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="8668a-110">El \_ grupo predeterminado D3DPOOL es independiente de D3DPOOL \_ Managed y D3DPOOL \_ SYSTEMMEM, y especifica que el recurso se coloca en la memoria preferida para el acceso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8668a-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="8668a-111">Tenga en cuenta que el \_ valor predeterminado de D3DPOOL nunca indica que D3DPOOL \_ administrado o D3DPOOL \_ SYSTEMMEM debe elegirse como el tipo de bloque de memoria para este recurso.</span><span class="sxs-lookup"><span data-stu-id="8668a-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="8668a-112">Las texturas colocadas en el \_ grupo predeterminado D3DPOOL no se pueden bloquear a menos que sean texturas dinámicas o son formatos de controlador privados, FourCC.</span><span class="sxs-lookup"><span data-stu-id="8668a-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="8668a-113">Para acceder a las texturas de unlockable, debe usar funciones como [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)y [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="8668a-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="8668a-114">\_La administración de D3DPOOL es probablemente una opción mejor que D3DPOOL \_ predeterminada para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8668a-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="8668a-115">Tenga en cuenta que algunas texturas creadas en formatos de píxeles de propietario del controlador, desconocidos para el tiempo de ejecución de Direct3D, se pueden bloquear.</span><span class="sxs-lookup"><span data-stu-id="8668a-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="8668a-116">Tenga en cuenta también que, a diferencia de las texturas, los búferes de intercambio de cadena, los destinos de representación, los búferes de vértices y los búferes de índice se pueden bloquear.</span><span class="sxs-lookup"><span data-stu-id="8668a-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="8668a-117">Cuando se pierde un dispositivo, los recursos creados con D3DPOOL \_ default se deben liberar antes de llamar a [**IDirect3DDevice9:: RESET**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="8668a-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="8668a-118">Para obtener más información, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="8668a-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="8668a-119">Al crear recursos con el \_ valor predeterminado de D3DPOOL, si ya se ha confirmado la memoria de la tarjeta de vídeo, los recursos administrados se expulsarán para liberar suficiente memoria para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8668a-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="8668a-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**Administrado por D3DPOOL \_**</span><span class="sxs-lookup"><span data-stu-id="8668a-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="8668a-121">Los recursos se copian automáticamente en la memoria accesible para el dispositivo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8668a-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="8668a-122">Los recursos administrados están respaldados por la memoria del sistema y no es necesario volver a crearlos cuando se pierde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8668a-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="8668a-123">Consulte [Administración de recursos (Direct3D 9)](managing-resources.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8668a-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="8668a-124">Se pueden bloquear los recursos administrados.</span><span class="sxs-lookup"><span data-stu-id="8668a-124">Managed resources can be locked.</span></span> <span data-ttu-id="8668a-125">Solo se modifica directamente la copia de la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="8668a-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="8668a-126">Direct3D copia los cambios en la memoria accesible desde el controlador según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8668a-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8668a-127">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="8668a-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="8668a-128">D3DPOOL \_ Managed es válido con [**IDirect3DDevice9**](/windows/desktop/api); sin embargo, no es válido con [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="8668a-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8668a-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="8668a-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="8668a-130">Los recursos se colocan en memoria que normalmente no es accesible para el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8668a-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="8668a-131">Esta asignación de memoria consume RAM del sistema pero no reduce la memoria RAM paginable.</span><span class="sxs-lookup"><span data-stu-id="8668a-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="8668a-132">No es necesario volver a crear estos recursos cuando se pierde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8668a-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="8668a-133">Los recursos de este grupo se pueden bloquear y se pueden usar como origen de una operación [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) o [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) en un recurso de memoria creado con D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="8668a-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="8668a-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**</span><span class="sxs-lookup"><span data-stu-id="8668a-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="8668a-135">Los recursos se colocan en la RAM del sistema y no es necesario volver a crearlos cuando se pierde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8668a-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="8668a-136">Estos recursos no están limitados por el tamaño del dispositivo o las restricciones de formato.</span><span class="sxs-lookup"><span data-stu-id="8668a-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="8668a-137">Por este motivo, no se puede tener acceso a estos recursos mediante el dispositivo Direct3D ni establecerse como texturas o destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="8668a-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="8668a-138">Sin embargo, estos recursos siempre se pueden crear, bloquear y copiar.</span><span class="sxs-lookup"><span data-stu-id="8668a-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="8668a-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8668a-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8668a-140">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="8668a-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8668a-141">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8668a-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8668a-142">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8668a-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8668a-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8668a-143">Remarks</span></span>

<span data-ttu-id="8668a-144">Todos los tipos de grupo son válidos con todos los recursos, incluidos: búferes de vértices, búferes de índice, texturas y superficies.</span><span class="sxs-lookup"><span data-stu-id="8668a-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="8668a-145">En las tablas siguientes se indican las restricciones en los tipos de grupo para destinos de representación, galerías de símbolos de profundidad y usos dinámicos y de mipmap.</span><span class="sxs-lookup"><span data-stu-id="8668a-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="8668a-146">Una x indica una combinación compatible; la falta de una x indica una incompatibilidad.</span><span class="sxs-lookup"><span data-stu-id="8668a-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="8668a-147">grupo</span><span class="sxs-lookup"><span data-stu-id="8668a-147">Pool</span></span>               | <span data-ttu-id="8668a-148">D3DUSAGE \_ RENDERTARGET</span><span class="sxs-lookup"><span data-stu-id="8668a-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="8668a-149">D3DUSAGE \_ DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="8668a-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="8668a-150">\_Valor predeterminado de D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="8668a-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="8668a-151">x</span><span class="sxs-lookup"><span data-stu-id="8668a-151">x</span></span>                      | <span data-ttu-id="8668a-152">x</span><span class="sxs-lookup"><span data-stu-id="8668a-152">x</span></span>                      |
| <span data-ttu-id="8668a-153">Administrado por D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="8668a-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="8668a-154">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="8668a-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="8668a-155">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="8668a-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="8668a-156">grupo</span><span class="sxs-lookup"><span data-stu-id="8668a-156">Pool</span></span>               | <span data-ttu-id="8668a-157">D3DUSAGE \_ dinámico</span><span class="sxs-lookup"><span data-stu-id="8668a-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="8668a-158">D3DUSAGE \_ AUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="8668a-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="8668a-159">\_Valor predeterminado de D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="8668a-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="8668a-160">x</span><span class="sxs-lookup"><span data-stu-id="8668a-160">x</span></span>                 | <span data-ttu-id="8668a-161">x</span><span class="sxs-lookup"><span data-stu-id="8668a-161">x</span></span>                       |
| <span data-ttu-id="8668a-162">Administrado por D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="8668a-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="8668a-163">x</span><span class="sxs-lookup"><span data-stu-id="8668a-163">x</span></span>                       |
| <span data-ttu-id="8668a-164">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="8668a-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="8668a-165">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="8668a-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="8668a-166">x</span><span class="sxs-lookup"><span data-stu-id="8668a-166">x</span></span>                 |                         |



 

<span data-ttu-id="8668a-167">Para obtener más información sobre los tipos de uso, vea [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="8668a-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="8668a-168">Los grupos no se pueden mezclar para los distintos objetos contenidos en un recurso (niveles MIP en un mipmap) y, cuando se elige un grupo, no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="8668a-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="8668a-169">Las aplicaciones deben usar D3DPOOL \_ administradas para la mayoría de los recursos estáticos, ya que esto evita que la aplicación tenga que tratar con los dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="8668a-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="8668a-170">(El tiempo de ejecución restaura los recursos administrados). Esto es especialmente útil para los sistemas de arquitectura de memoria unificada (UMA).</span><span class="sxs-lookup"><span data-stu-id="8668a-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="8668a-171">Otros recursos dinámicos no son una buena coincidencia para D3DPOOL \_ administrado.</span><span class="sxs-lookup"><span data-stu-id="8668a-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="8668a-172">De hecho, los búferes de índice y los búferes de vértices no se pueden crear con D3DPOOL \_ administrados junto con D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="8668a-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="8668a-173">En el caso de las texturas dinámicas, a veces es conveniente usar un par de texturas de memoria de vídeo y de memoria del sistema, asignando la memoria de vídeo mediante D3DPOOL \_ default y la memoria del sistema mediante D3DPOOL \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="8668a-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="8668a-174">Puede bloquear y modificar los bits de la textura de memoria del sistema mediante un método de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8668a-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="8668a-175">Después, puede actualizar la textura de memoria de vídeo mediante [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="8668a-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="8668a-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8668a-176">Requirements</span></span>



| <span data-ttu-id="8668a-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="8668a-177">Requirement</span></span> | <span data-ttu-id="8668a-178">Value</span><span class="sxs-lookup"><span data-stu-id="8668a-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8668a-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8668a-179">Header</span></span><br/> | <dl> <span data-ttu-id="8668a-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8668a-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8668a-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="8668a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8668a-182">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8668a-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8668a-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="8668a-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="8668a-184">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="8668a-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="8668a-185">**IDirect3DDevice9::CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8668a-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="8668a-186">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="8668a-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="8668a-187">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="8668a-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="8668a-188">**IDirect3DDevice9::CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="8668a-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="8668a-189">**D3DINDEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8668a-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="8668a-190">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8668a-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="8668a-191">**D3DVERTEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8668a-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="8668a-192">**D3DVOLUME \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8668a-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
