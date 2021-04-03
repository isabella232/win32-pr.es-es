---
description: Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se va a realizar.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807699"
---
# <a name="d3dlock"></a><span data-ttu-id="7fe26-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="7fe26-103">D3DLOCK</span></span>

<span data-ttu-id="7fe26-104">Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="7fe26-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe26-105">\#define</span><span class="sxs-lookup"><span data-stu-id="7fe26-105">\#define</span></span>                   | <span data-ttu-id="7fe26-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fe26-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7fe26-107">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="7fe26-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="7fe26-108">La aplicación descarta toda la memoria dentro de la región bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7fe26-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="7fe26-109">En el caso de los búferes de vértices y de índices, se descartará todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="7fe26-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="7fe26-110">Esta opción solo es válida cuando el recurso se crea con uso dinámico (vea [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="7fe26-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7fe26-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="7fe26-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="7fe26-112">Permite que una aplicación recupere ciclos de CPU si el controlador no puede bloquear la superficie inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="7fe26-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="7fe26-113">Si se establece esta marca y el controlador no puede bloquear la superficie inmediatamente, la llamada de bloqueo devolverá D3DERR \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="7fe26-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="7fe26-114">Esta marca solo se puede usar cuando se bloquea una superficie creada con [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="7fe26-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="7fe26-115">Esta marca también se puede utilizar con un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="7fe26-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="7fe26-116">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="7fe26-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="7fe26-117">De forma predeterminada, un bloqueo en un recurso agrega una región desfasada a ese recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe26-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="7fe26-118">Esta opción evita cualquier cambio en el estado de modificación del recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe26-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="7fe26-119">Las aplicaciones deben usar esta opción cuando tengan información adicional sobre el conjunto de regiones que han cambiado durante la operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7fe26-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7fe26-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="7fe26-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="7fe26-121">Indica que la memoria a la que se hizo referencia en una llamada de dibujo desde el último bloqueo sin esta marca no se modificará durante el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7fe26-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="7fe26-122">Esto puede habilitar las optimizaciones cuando la aplicación está anexando datos a un recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe26-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="7fe26-123">Si se especifica esta marca, el controlador se devolverá inmediatamente si el recurso está en uso; de lo contrario, el controlador debe terminar de usar el recurso antes de volver del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7fe26-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="7fe26-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="7fe26-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="7fe26-125">El comportamiento predeterminado de un bloqueo de memoria de vídeo es reservar una sección crítica para todo el sistema, lo que garantiza que no se producirán cambios en el modo de presentación mientras dure el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7fe26-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="7fe26-126">Esta opción hace que la sección crítica para todo el sistema no se mantenga mientras dure el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7fe26-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="7fe26-127">La operación de bloqueo lleva mucho tiempo, pero puede permitir que el sistema realice otras tareas, como mover el cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="7fe26-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="7fe26-128">Esta opción es útil para los bloqueos de larga duración, como el bloqueo del búfer de reserva para la representación de software que de otro modo afectaría negativamente a la capacidad de respuesta del sistema.</span><span class="sxs-lookup"><span data-stu-id="7fe26-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="7fe26-129">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7fe26-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="7fe26-130">La aplicación no escribirá en el búfer.</span><span class="sxs-lookup"><span data-stu-id="7fe26-130">The application will not write to the buffer.</span></span> <span data-ttu-id="7fe26-131">Esto permite que los recursos almacenados en formatos no nativos guarden el paso de recompresión al desbloquearse.</span><span class="sxs-lookup"><span data-stu-id="7fe26-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="7fe26-132">Información constante</span><span class="sxs-lookup"><span data-stu-id="7fe26-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="7fe26-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fe26-133">Header</span></span>                   | <span data-ttu-id="7fe26-134">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="7fe26-134">d3d9types.h</span></span> |
| <span data-ttu-id="7fe26-135">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="7fe26-135">Minimum operating system</span></span> | <span data-ttu-id="7fe26-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7fe26-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="7fe26-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe26-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe26-138">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7fe26-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="7fe26-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="7fe26-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="7fe26-140">**Lock**</span><span class="sxs-lookup"><span data-stu-id="7fe26-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="7fe26-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="7fe26-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="7fe26-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="7fe26-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="7fe26-143">**Lock**</span><span class="sxs-lookup"><span data-stu-id="7fe26-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="7fe26-144">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="7fe26-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="7fe26-145">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="7fe26-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="7fe26-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="7fe26-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="7fe26-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="7fe26-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="7fe26-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="7fe26-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="7fe26-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="7fe26-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
