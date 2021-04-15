---
title: Acerca de la sincronización de dispositivos
description: Acerca de la sincronización de dispositivos
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizar dispositivos
- Modelo de objetos de Windows Media Player, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Control ActiveX de Windows Media Player, sincronizar dispositivos
- Control ActiveX, sincronizar dispositivos
- Control ActiveX móvil de Windows Media Player, sincronizar dispositivos
- Windows Media Player Mobile, sincronizar dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
- sincronización de dispositivos, transferencia manual
- sincronización de dispositivos, transferencia manual
- sincronizar dispositivos, sincronización automática
- sincronización de dispositivos, sincronización automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695294"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="fe986-116">Acerca de la sincronización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="fe986-116">About Device Synchronization</span></span>

<span data-ttu-id="fe986-117">Windows Media Player 10 presentó un nuevo modelo para sincronizar contenido multimedia digital con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="fe986-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="fe986-118">Desde la perspectiva del usuario, esto significa que puede especificar qué listas de reproducción (incluidas las listas de reproducción automáticas) se sincronizan automáticamente con los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fe986-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="fe986-119">También puede transferir manualmente contenido multimedia digital a los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fe986-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="fe986-120">Desde la perspectiva del desarrollador, esto significa que hay nuevas funcionalidades expuestas que puede aprovechar en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fe986-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="fe986-121">Para ello, debe crear una instancia remota del control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="fe986-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="fe986-122">Hay dos maneras en que un usuario puede copiar contenido multimedia digital en un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="fe986-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="fe986-123">**Transferencia manual.**</span><span class="sxs-lookup"><span data-stu-id="fe986-123">**Manual transfer.**</span></span> <span data-ttu-id="fe986-124">El usuario selecciona el contenido multimedia digital en la biblioteca y, a continuación, inicia una transferencia del contenido al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe986-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="fe986-125">Esto es similar a la funcionalidad proporcionada por las versiones anteriores de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe986-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="fe986-126">El SDK de Windows Media Player no proporciona métodos para transferir medios digitales a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe986-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="fe986-127">**Sincronización automática.**</span><span class="sxs-lookup"><span data-stu-id="fe986-127">**Automatic synchronization.**</span></span> <span data-ttu-id="fe986-128">El usuario especifica las listas de reproducción que se sincronizan automáticamente con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe986-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="fe986-129">Esta es una característica de Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fe986-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="fe986-130">El SDK de Windows Media Player proporciona funcionalidad para administrar la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="fe986-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="fe986-131">Esta funcionalidad está diseñada para permitirle crear una interfaz de usuario personalizada para la aplicación con el fin de especificar cómo se produce la sincronización de dispositivos y proporcionar información de estado a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fe986-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="fe986-132">Para que la sincronización automática funcione, debe establecerse una relación especial entre Windows Media Player y el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe986-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="fe986-133">Esta relación se denomina *Asociación*.</span><span class="sxs-lookup"><span data-stu-id="fe986-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="fe986-134">En las secciones siguientes se proporciona más información sobre la sincronización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fe986-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="fe986-135">Acerca de los dispositivos</span><span class="sxs-lookup"><span data-stu-id="fe986-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="fe986-136">Acerca de las asociaciones</span><span class="sxs-lookup"><span data-stu-id="fe986-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="fe986-137">Acerca del motor de sincronización</span><span class="sxs-lookup"><span data-stu-id="fe986-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="fe986-138">Acerca de la sincronización de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="fe986-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="fe986-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe986-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe986-140">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="fe986-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="fe986-141">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fe986-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="fe986-142">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="fe986-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




