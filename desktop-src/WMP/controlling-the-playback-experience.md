---
title: Controlar la experiencia de reproducción
description: Controlar la experiencia de reproducción
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Listas de reproducción de metarchivo de Windows Media, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivos, controlar la reproducción
- Listas de reproducción de metarchivos de Windows Media, problemas de reproducción
- listas de reproducción, problemas de reproducción
- listas de reproducción de metarchivos, problemas de reproducción
- controlar la reproducción
- Windows Media Player, controlar la reproducción
- Windows Media Player, problemas de reproducción
- HTMLView, problemas de reproducción
- HTMLView, controlar la reproducción
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695384"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="269f5-114">Controlar la experiencia de reproducción</span><span class="sxs-lookup"><span data-stu-id="269f5-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="269f5-115">En esta sección se tratan algunos de los problemas de reproducción que se pueden producir al usar la característica HTMLView.</span><span class="sxs-lookup"><span data-stu-id="269f5-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="269f5-116">Solicitar al usuario que vea el contenido basado en Web</span><span class="sxs-lookup"><span data-stu-id="269f5-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="269f5-117">Puede decidir que solo desea que los usuarios puedan disfrutar del contenido multimedia digital cuando también se muestre el contenido basado en Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="269f5-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="269f5-118">Puede incluir código de script en la Página Web de HTMLView que detiene la reproducción del contenido multimedia digital si el usuario cambia de la característica de **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="269f5-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="269f5-119">Para ello, puede especificar un controlador de eventos para el evento **Unload** como parte del elemento **Body** , como se muestra en el siguiente código HTML:</span><span class="sxs-lookup"><span data-stu-id="269f5-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="269f5-120">Después, puede incluir código de script en la función de controlador de eventos para cerrar el archivo en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="269f5-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="269f5-121">En el siguiente código de ejemplo se hace esto:</span><span class="sxs-lookup"><span data-stu-id="269f5-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="269f5-122">Cuando el usuario cambia de la **reproducción** en curso haciendo clic en un botón para abrir otra característica de Windows Media Player, como la biblioteca, el reproductor cierra el explorador incrustado.</span><span class="sxs-lookup"><span data-stu-id="269f5-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="269f5-123">Esto hace que se produzca el evento **OnUnload** , ejecutando el script en la función denominada **UnloadMe**.</span><span class="sxs-lookup"><span data-stu-id="269f5-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="269f5-124">El método [Player. Close](player-close.md) detiene la reproducción y descarga el archivo multimedia digital actual.</span><span class="sxs-lookup"><span data-stu-id="269f5-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="269f5-125">Para volver a ver el contenido, el usuario debe volver a abrir el archivo. ASX original.</span><span class="sxs-lookup"><span data-stu-id="269f5-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="269f5-126">Esta técnica también detiene la reproducción cuando el usuario se desplaza fuera de la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="269f5-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="269f5-127">Tenga en cuenta que esta técnica no puede impedir que el usuario vea el contenido multimedia digital cuando cambia al modo de máscara.</span><span class="sxs-lookup"><span data-stu-id="269f5-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="269f5-128">Recordará que el parámetro HTMLView se puede aplicar a cada elemento de **entrada** en un archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="269f5-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="269f5-129">Puede aprovechar esta característica para asegurarse de que el contenido de HTMLView se muestra cada vez que se inicia un nuevo archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="269f5-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="269f5-130">Para ello, asocie un elemento **param** para HTMLView con cada entrada de la lista de reproducción. ASX.</span><span class="sxs-lookup"><span data-stu-id="269f5-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="269f5-131">Cuando se reproduce cada entrada, el reproductor vuelve al modo completo y muestra el contenido de HTMLView que especificó en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="269f5-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="269f5-132">Los tipos de comandos URL y script de archivo están deshabilitados de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="269f5-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="269f5-133">Windows Media Player 9 series o posterior proporciona opciones de configuración que permiten al usuario especificar si los comandos de script y de tipo de archivo se pueden ejecutar.</span><span class="sxs-lookup"><span data-stu-id="269f5-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="269f5-134">De forma predeterminada, ambos tipos de comando de script no se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="269f5-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="269f5-135">Si usa tipos de comandos de scripts personalizados, se seguirán ejecutando, independientemente de la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="269f5-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="269f5-136">Si debe usar comandos de script y de tipo de archivo, debe pedir al usuario que cambie la configuración.</span><span class="sxs-lookup"><span data-stu-id="269f5-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="269f5-137">Para cambiar la configuración, haga clic en **herramientas**, **Opciones** y, a continuación, en **seguridad**.</span><span class="sxs-lookup"><span data-stu-id="269f5-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="269f5-138">Al volver a abrir un HTMLView, no se recarga la página web</span><span class="sxs-lookup"><span data-stu-id="269f5-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="269f5-139">Cuando el usuario abre un archivo. ASX que incluye un parámetro HTMLView y, posteriormente, vuelve a abrir el mismo archivo, Windows Media Player no actualiza la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="269f5-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="269f5-140">Esto también significa que si ha permitido a los usuarios salir de la Página Web de HTMLView, el reproductor no devuelve el explorador incrustado a la Página Web de HTMLView inicial.</span><span class="sxs-lookup"><span data-stu-id="269f5-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="269f5-141">Ocultar la ubicación del contenido</span><span class="sxs-lookup"><span data-stu-id="269f5-141">Hiding the content location</span></span>

<span data-ttu-id="269f5-142">Puede decidir que no desea que Windows Media Player muestre la ubicación del contenido multimedia digital mientras se está reproduciendo un archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="269f5-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="269f5-143">Normalmente, Windows Media Player solo muestra información sobre la lista de reproducción al transmitir contenido desde Internet.</span><span class="sxs-lookup"><span data-stu-id="269f5-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="269f5-144">Sin embargo, hay pasos adicionales que puede seguir para evitar que los usuarios determinen la ubicación del contenido.</span><span class="sxs-lookup"><span data-stu-id="269f5-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="269f5-145">Por ejemplo, una manera de asegurarse de que el reproductor no muestra la ruta de acceso al contenido es transmitir el contenido mediante listas de reproducción de Windows Media Services del servidor.</span><span class="sxs-lookup"><span data-stu-id="269f5-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="269f5-146">De este modo, cuando el usuario ve las propiedades del contenido, ve la dirección URL del servidor y no la dirección URL de su contenido.</span><span class="sxs-lookup"><span data-stu-id="269f5-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="269f5-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="269f5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269f5-148">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="269f5-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="269f5-149">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="269f5-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




