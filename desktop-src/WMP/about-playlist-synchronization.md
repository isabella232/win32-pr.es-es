---
title: Acerca de la sincronización de listas de reproducción
description: Acerca de la sincronización de listas de reproducción
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronización de listas de reproducción
- Modelo de objetos de Windows Media Player, sincronización de listas de reproducción
- modelo de objetos, sincronización de listas de reproducción
- Control ActiveX de Windows Media Player, sincronización de listas de reproducción
- Control ActiveX, sincronización de listas de reproducción
- Control ActiveX móvil de Windows Media Player, sincronización de listas de reproducción
- Windows Media Player Mobile, sincronización de listas de reproducción
- sincronizar dispositivos, listas de reproducción
- sincronización de dispositivos, listas de reproducción
- listas de reproducción, sincronización
- Listas de reproducción de metarchivos de Windows Media, sincronización
- listas de reproducción de metarchivos, sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358676"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="390f1-115">Acerca de la sincronización de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="390f1-115">About Playlist Synchronization</span></span>

<span data-ttu-id="390f1-116">Windows Media Player 10 o posterior está diseñado para sincronizar el contenido multimedia digital con los dispositivos mediante un modelo de sincronización de listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="390f1-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="390f1-117">Esto significa que el contenido destinado a copiarse en un dispositivo debe formar parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="390f1-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="390f1-118">Cuando el usuario elige transferir contenido multimedia digital individual desde su equipo a un dispositivo, Windows Media Player agrega el contenido a una lista de reproducción predeterminada para copiarlo.</span><span class="sxs-lookup"><span data-stu-id="390f1-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="390f1-119">Las API de sincronización de dispositivos de Windows Media Player están diseñadas para funcionar como esto también.</span><span class="sxs-lookup"><span data-stu-id="390f1-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="390f1-120">Al igual que Windows Media Player, el programa puede presentar al usuario una lista de listas de reproducción que ha definido.</span><span class="sxs-lookup"><span data-stu-id="390f1-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="390f1-121">Después, puede permitir que el usuario elija qué listas de reproducción se van a sincronizar con un dispositivo determinado y establecer el orden de prioridad para el proceso de sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="390f1-122">Dado que los dispositivos portátiles tienen una capacidad de almacenamiento limitada, es posible que el usuario elija sincronizar más contenido multimedia digital que el dispositivo que puede almacenar.</span><span class="sxs-lookup"><span data-stu-id="390f1-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="390f1-123">Windows Media Player sincroniza el contenido en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="390f1-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="390f1-124">El usuario puede definir el orden de prioridad mediante el uso de un cuadro de diálogo al que se puede tener acceso desde la característica **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="390f1-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="390f1-125">En respuesta a la entrada del usuario en el programa, puede cambiar el orden de prioridad mediante programación cambiando los valores de determinados atributos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="390f1-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="390f1-126">Colectivamente, estos atributos se denominan atributos de *sincronización* .</span><span class="sxs-lookup"><span data-stu-id="390f1-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="390f1-127">Cada lista de reproducción de una biblioteca tiene 16 atributos de sincronización: **Sync01** a **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="390f1-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="390f1-128">Cada atributo representa el dispositivo que tiene el índice de asociación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="390f1-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="390f1-129">El valor de cada atributo le indica dos cosas:</span><span class="sxs-lookup"><span data-stu-id="390f1-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="390f1-130">Si la lista de reproducción se debe sincronizar con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="390f1-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="390f1-131">Valor de prioridad para la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="390f1-131">The priority value for the playlist.</span></span>

<span data-ttu-id="390f1-132">Un valor de cero indica que Windows Media Player no debe intentar sincronizar la lista de reproducción con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="390f1-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="390f1-133">Cualquier otro valor es un número de prioridad.</span><span class="sxs-lookup"><span data-stu-id="390f1-133">Any other value is a priority number.</span></span> <span data-ttu-id="390f1-134">Los valores inferiores reciben mayor prioridad en el momento de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="390f1-135">Las listas de reproducción también tienen un atributo **SyncOnly** que indica si la lista de reproducción solo está disponible para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="390f1-136">Los elementos individuales de contenido multimedia digital contienen metadatos sobre la sincronización también.</span><span class="sxs-lookup"><span data-stu-id="390f1-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="390f1-137">Al recuperar un objeto **multimedia** de la biblioteca, puede inspeccionar el valor del atributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="390f1-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="390f1-138">Este atributo proporciona información ampliada sobre si el contenido se ha copiado correctamente en el dispositivo o si se ha producido un error en la copia del contenido porque no cabe.</span><span class="sxs-lookup"><span data-stu-id="390f1-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="390f1-139">Debe evitar proporcionar elementos de la interfaz de usuario que permitan al usuario crear listas de reproducción a partir de todo el contenido de la biblioteca para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="390f1-140">Para optimizar el rendimiento, Windows Media Player aplica un conjunto de reglas para crear listas de reproducción de sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="390f1-141">El programa solo debe crear listas de reproducción de sincronización para el contenido proporcionado.</span><span class="sxs-lookup"><span data-stu-id="390f1-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="390f1-142">Esta opción permite a Windows Media Player crear listas de reproducción de sincronización para el contenido que el usuario agregó a la biblioteca desde otros orígenes.</span><span class="sxs-lookup"><span data-stu-id="390f1-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="390f1-143">Como alternativa a la creación de su propia interfaz de usuario de lista de reproducción, puede presentar a los usuarios un cuadro de diálogo predeterminado para elegir listas de reproducción y administrar la Asociación de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="390f1-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="390f1-144">Para ello, llame a [IWMPSyncDevice:: showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="390f1-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="390f1-145">Al invocar este método, Windows Media Player muestra el cuadro de diálogo Configuración de sincronización.</span><span class="sxs-lookup"><span data-stu-id="390f1-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="390f1-146">Cuando el usuario cierra el cuadro de diálogo, Windows Media Player vuelve automáticamente a su estado de acoplamiento anterior y vuelve a pasar el control al programa remoto.</span><span class="sxs-lookup"><span data-stu-id="390f1-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="390f1-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="390f1-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="390f1-148">**Acerca de la sincronización de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="390f1-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="390f1-149">**Administrar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="390f1-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="390f1-150">**Atributos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="390f1-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




