---
title: Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows
description: Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Administrador de dispositivos, reproductores de audio portátiles
- Administrador de dispositivos, reproductores de audio portátiles
- Guía de programación, reproductores de audio portátiles
- proveedores de servicios, reproductores de audio portátiles
- creación de proveedores de servicios, reproductores de audio portátiles
- reproductores de audio portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695336"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="80167-109">Requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="80167-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="80167-110">La extensión de espacio de nombres del shell del reproductor de audio portátil proporciona a los usuarios de Windows una manera coherente de administrar los dispositivos de audio administrados por Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="80167-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="80167-111">Si crea los componentes del proveedor de servicios y del controlador según las siguientes directrices, el dispositivo se mostrará en el espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="80167-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="80167-112">Los usuarios podrán interactuar con el contenido del dispositivo de forma coherente en el explorador de Windows para realizar operaciones básicas, como copiar, eliminar y cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="80167-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="80167-113">Los siguientes requisitos de Shell para el proveedor de servicios y los componentes de controlador están diseñados para complementar las directrices generales de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="80167-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="80167-114">Capacidades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="80167-114">Device Capabilities</span></span>

<span data-ttu-id="80167-115">Los proveedores de servicios de Windows Media Administrador de dispositivos deben ser explícitos en sus capacidades admitidas.</span><span class="sxs-lookup"><span data-stu-id="80167-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="80167-116">Si no se admite una llamada, se debe devolver un código de error.</span><span class="sxs-lookup"><span data-stu-id="80167-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="80167-117">Se deben establecer los campos adecuados para la presencia o ausencia de funcionalidades en la devolución de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="80167-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="80167-118">**IMDSPStorageGlobals::GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="80167-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="80167-119">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="80167-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="80167-120">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="80167-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="80167-121">Los proveedores de servicios deben admitir las siguientes funcionalidades para ser compatibles con el Shell:</span><span class="sxs-lookup"><span data-stu-id="80167-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="80167-122">Copiar en el dispositivo (compatible con las devoluciones de llamada de cancelación y progreso)</span><span class="sxs-lookup"><span data-stu-id="80167-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="80167-123">Eliminar archivo del dispositivo (compatible con las devoluciones de llamada de cancelación y progreso)</span><span class="sxs-lookup"><span data-stu-id="80167-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="80167-124">Cambiar el nombre del archivo en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="80167-124">Rename file on device</span></span>
-   <span data-ttu-id="80167-125">Informes de espacio (espacio total, espacio libre, espacio inutilizable)</span><span class="sxs-lookup"><span data-stu-id="80167-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="80167-126">Plug and Play (consulte [habilitación de PNP para dispositivos](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="80167-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="80167-127">Formato (preferiblemente con compatibilidad con las devoluciones de llamada de cancelación y progreso)</span><span class="sxs-lookup"><span data-stu-id="80167-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="80167-128">Si se admiten metadatos, se deben admitir los siguientes campos para archivos individuales.</span><span class="sxs-lookup"><span data-stu-id="80167-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="80167-129">Si no hay datos disponibles, el campo debe inicializarse como una cadena vacía:</span><span class="sxs-lookup"><span data-stu-id="80167-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="80167-130">Campo</span><span class="sxs-lookup"><span data-stu-id="80167-130">Field</span></span>        | <span data-ttu-id="80167-131">Constante (definida en WMDM. idl)</span><span class="sxs-lookup"><span data-stu-id="80167-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="80167-132">Etiqueta Metadata</span><span class="sxs-lookup"><span data-stu-id="80167-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="80167-133">Título de la canción</span><span class="sxs-lookup"><span data-stu-id="80167-133">Song Title</span></span>   | <span data-ttu-id="80167-134">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="80167-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="80167-135">WMDM/título</span><span class="sxs-lookup"><span data-stu-id="80167-135">WMDM/Title</span></span>      |
| <span data-ttu-id="80167-136">Número de pista</span><span class="sxs-lookup"><span data-stu-id="80167-136">Track Number</span></span> | <span data-ttu-id="80167-137">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="80167-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="80167-138">WMDM/Track</span><span class="sxs-lookup"><span data-stu-id="80167-138">WMDM/Track</span></span>      |
| <span data-ttu-id="80167-139">Artistas</span><span class="sxs-lookup"><span data-stu-id="80167-139">Artist</span></span>       | <span data-ttu-id="80167-140">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="80167-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="80167-141">WMDM/autor</span><span class="sxs-lookup"><span data-stu-id="80167-141">WMDM/Author</span></span>     |
| <span data-ttu-id="80167-142">Álbum</span><span class="sxs-lookup"><span data-stu-id="80167-142">Album</span></span>        | <span data-ttu-id="80167-143">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="80167-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="80167-144">WMDM/álbum</span><span class="sxs-lookup"><span data-stu-id="80167-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="80167-145">Year</span><span class="sxs-lookup"><span data-stu-id="80167-145">Year</span></span>         | <span data-ttu-id="80167-146">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="80167-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="80167-147">WMDM/año</span><span class="sxs-lookup"><span data-stu-id="80167-147">WMDM/Year</span></span>       |
| <span data-ttu-id="80167-148">Género</span><span class="sxs-lookup"><span data-stu-id="80167-148">Genre</span></span>        | <span data-ttu-id="80167-149">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="80167-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="80167-150">WMDM/género</span><span class="sxs-lookup"><span data-stu-id="80167-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="80167-151">Simultaneidad</span><span class="sxs-lookup"><span data-stu-id="80167-151">Concurrency</span></span>

<span data-ttu-id="80167-152">Los controladores de modo kernel para Windows Media Administrador de dispositivos deben ser sólidos para controlar el acceso simultáneo.</span><span class="sxs-lookup"><span data-stu-id="80167-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="80167-153">Por ejemplo, un usuario puede tener acceso simultáneamente al dispositivo a través del shell y el reproductor multimedia, o simplemente a través de varias ventanas en el shell.</span><span class="sxs-lookup"><span data-stu-id="80167-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="80167-154">Como parte del control de la simultaneidad, los controladores no deben asumir, solo porque se ha cargado el proveedor de servicios, que el dispositivo está en uso.</span><span class="sxs-lookup"><span data-stu-id="80167-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="80167-155">En su lugar, deben implementar un mecanismo de bloqueo para serializar el acceso al dispositivo según sea necesario para las operaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="80167-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="80167-156">UI</span><span class="sxs-lookup"><span data-stu-id="80167-156">UI</span></span>

<span data-ttu-id="80167-157">Los proveedores de servicios de Windows Media Administrador de dispositivos no deben mostrar ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="80167-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="80167-158">Siempre que sea posible, se deben devolver todos los errores de las llamadas de método como códigos de error específicos de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="80167-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="80167-159">Habilitar en el shell</span><span class="sxs-lookup"><span data-stu-id="80167-159">Enabling in the Shell</span></span>

<span data-ttu-id="80167-160">Si el paquete cumple todos los requisitos de Shell, puede habilitar el dispositivo para que se muestre en el shell estableciendo el valor de *ShowInShell* en 1 en los parámetros del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80167-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="80167-161">Para obtener más información, vea [parámetros de dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="80167-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80167-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80167-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80167-163">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="80167-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




