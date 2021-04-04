---
title: Comparación detallada del modelo de objetos
description: Comparación detallada del modelo de objetos
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, diferencias de versión
- modelo de objetos, diferencias de versión
- Control ActiveX de Windows Media Player, diferencias de versión
- Control ActiveX, diferencias de versión
- Control ActiveX móvil de Windows Media Player, diferencias de versión
- Windows Media Player Mobile, modelo de objetos
- Guía de migración, diferencias de versión
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104077261"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="d596c-112">Comparación detallada del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="d596c-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="d596c-113">En la tabla siguiente se comparan las propiedades del modelo de objetos de Windows Media Player 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d596c-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d596c-114">Propiedad 6,4 de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d596c-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="d596c-115">Windows Media Player 7 o posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="d596c-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d596c-116"><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="d596c-117">La presentación de Windows Media Player 7 o posterior cambia automáticamente de tamaño para ajustarse a los medios.</span><span class="sxs-lookup"><span data-stu-id="d596c-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="d596c-118">Puede establecer las propiedades de alto y ancho en la <OBJECT> etiqueta o en el script.</span><span class="sxs-lookup"><span data-stu-id="d596c-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-119"><em>Player6</em>. <strong>AllowScan</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="d596c-120"><em>Controles</em>.</span><span class="sxs-lookup"><span data-stu-id="d596c-120"><em>Controls</em>.</span></span> <span data-ttu-id="d596c-121"><strong>fastForward</strong> y <em>controles</em>. <strong>fastReverse</strong> se habilitan automáticamente para los tipos de archivo que admiten estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d596c-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-122"><em>Player6</em>. <strong>AnglesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-123">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-124"><em>Player6</em>. <strong>AnimationAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="d596c-125">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-126"><em>Player6</em>. <strong>AudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="d596c-127">Usar <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-128"><em>Player6</em>. <strong>AudioStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-129">Usar <em>controles</em>. <strong>audioLanguageCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-130"><em>Player6</em>. <strong>AutoRewind</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="d596c-131">Usar <em>controles</em>. <strong>currentPosition</strong> en el script para especificar o recuperar la posición actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="d596c-132">También puede usar marcadores y el <em>reproductor</em>. evento <strong>markerHit</strong> .</span><span class="sxs-lookup"><span data-stu-id="d596c-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-133"><em>Player6</em>. <strong>Ajustar tamaño automáticamente</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="d596c-134">El ajuste de tamaño automático es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d596c-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="d596c-135">Para invalidar el tamaño automático, establezca las propiedades Height y width en la <OBJECT> etiqueta o en el script.</span><span class="sxs-lookup"><span data-stu-id="d596c-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-136"><em>Player6</em>. <strong>Inicio automático</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="d596c-137">Usar <em>configuración</em>. <strong>Inicio automático</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-138"><em>Player6</em>. <strong>Saldo</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="d596c-139">Usar <em>configuración</em>. <strong>saldo</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-140"><em>Player6</em>. <strong>Ancho de banda</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="d596c-141">Usar <em>red</em>. <strong>ancho de banda</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-142"><em>Player6</em>. <strong>Baseurl</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="d596c-143">Usar <em>configuración</em>. <strong>baseurl</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-144"><em>Player6</em>. <strong>BufferingCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="d596c-145">Usar <em>red.</em> <strong>bufferingCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-146"><em>Player6</em>. <strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="d596c-147">Usar <em>red</em>. <strong>bufferingProgress</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-148"><em>Player6</em>. <strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="d596c-149">Usar <em>red</em>. <strong>bufferingTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-150"><em>Player6</em>. <strong>ButtonsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-151">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-152"><em>Player6</em>. <strong>CanPreview</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="d596c-153">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-154"><em>Player6</em>. <strong>CanScan</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="d596c-155">Usar <em>controles</em>. <strong>isavailable</strong>( &quot; Fastforward &quot; ) y <em>controles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</span><span class="sxs-lookup"><span data-stu-id="d596c-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="d596c-157">Usar <em>controles</em>. <strong>isavailable</strong> para probar si se puede realizar un método de búsqueda concreto.</span><span class="sxs-lookup"><span data-stu-id="d596c-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-158"><em>Player6</em>. <strong>CanSeekToMarkers</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="d596c-159">Usar <em>controles</em>. <strong>isavailable</strong>( &quot; CurrentMarker &quot; ).</span><span class="sxs-lookup"><span data-stu-id="d596c-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="d596c-160">Usar <em>medios</em>. <strong>markerCount</strong> para recuperar el recuento de marcadores de un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="d596c-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="d596c-161">Usar <em>controles</em>. <strong>currentMarker</strong> para especificar o recuperar el número de marcador actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-162"><em>Player6</em>. <strong>CaptioningID</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="d596c-163">Use <em>ClosedCaption</em>. <strong>captioningID</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-164"><em>Player6</em>. <strong>CCActive</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="d596c-165">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-165">Not available.</span></span> <span data-ttu-id="d596c-166">Consulte <a href="closed-captioning.md">subtítulos (CC</a> ) para obtener información acerca de cómo ha cambiado el subtítulos (CC) en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d596c-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-167"><em>Player6</em>. <strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="d596c-168">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-169"><em>Player6</em>. <strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="d596c-170">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-171"><em>Player6</em>. <strong>ChannelURL</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="d596c-172">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-173"><em>Player6</em>. <strong>ClickToPlay</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="d596c-174">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-174">Not available.</span></span> <span data-ttu-id="d596c-175">Debe proporcionar controles en la interfaz de usuario para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="d596c-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="d596c-176">Como alternativa, el usuario puede hacer clic con el botón secundario en la imagen de vídeo para abrir un menú emergente que contiene una selección de <strong>reproducción/pausa</strong> si es el <em>jugador</em>. <strong>enableContextMenu</strong> es igual a true.</span><span class="sxs-lookup"><span data-stu-id="d596c-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="d596c-178">No disponible. Windows Media Player 9 series o posterior permite al usuario seleccionar si se transmite un identificador de reproductor único a los proveedores de contenido.</span><span class="sxs-lookup"><span data-stu-id="d596c-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="d596c-179">Si el usuario selecciona esta opción, el reproductor envía un identificador único al servidor de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d596c-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="d596c-180">El identificador se registra en el archivo de registro del servidor, que se encuentra en. <em>system32\logfiles</em> de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="d596c-181">El nombre del campo de registro es &quot; c-playerid &quot; .</span><span class="sxs-lookup"><span data-stu-id="d596c-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="d596c-182">El registro del servidor no está habilitado de forma predeterminada en Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="d596c-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="d596c-183">Si el usuario no selecciona esta opción, el servidor genera un identificador de sesión aleatorio, que es único para cada cliente para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="d596c-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="d596c-184">Para obtener más información, consulte la documentación de Windows Media Services 9 series.</span><span class="sxs-lookup"><span data-stu-id="d596c-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-185"><em>Player6</em>. <strong>CodecCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="d596c-186">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-187"><em>Player6</em>. <strong>ColorKey</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="d596c-188">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-189"><em>Player6</em>. <strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="d596c-190">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-190">Not available.</span></span> <span data-ttu-id="d596c-191">Usar <em>red</em>. <strong>velocidad</strong> de bits para determinar la velocidad de bits actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-192"><em>Player6</em>. <strong>ContactAddress</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="d596c-193">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-194"><em>Player6</em>. <strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="d596c-195">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-196"><em>Player6</em>. <strong>ContactPhone</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="d596c-197">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-198"><em>Player6</em>. <strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="d596c-199">Use <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar el índice del átomo de fecha de creación.</span><span class="sxs-lookup"><span data-stu-id="d596c-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="d596c-200">Usar <em>medios</em>. <strong>getItemInfoByAtom</strong> para recuperar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="d596c-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-201"><em>Player6</em>. <strong>CurrentAngle</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="d596c-202">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-203"><em>Player6</em>. <strong>CurrentAudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="d596c-204">Usar <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-205"><em>Player6</em>. <strong>CurrentButton</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="d596c-206">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-207"><em>Player6</em>. <strong>CurrentCCService</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="d596c-208">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-209"><em>Player6</em>. <strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="d596c-210">Recupere la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-210">Retrieve the current playlist.</span></span> <span data-ttu-id="d596c-211">Si la lista de reproducción actual no es la misma que la lista de reproducción que devuelve el <em>CDROM</em>. <strong>lista de reproducción</strong>, no hay ningún capítulo actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="d596c-212">De lo contrario, el número de capítulo actual es el índice del medio actual de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-213"><em>Player6</em>. <strong>CurrentDiscSide</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="d596c-214">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="d596c-216">Use <em>DVD</em>. <strong>dominio</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-217"><em>Player6</em>. <strong>CurrentMarker</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="d596c-218">Usar <em>controles</em>. <strong>currentMarker</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="d596c-220">Usar <em>controles</em>. <strong>currentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-221"><em>Player6</em>. <strong>CurrentSubpictureStream</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="d596c-222">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="d596c-224">Usar <em>controles</em>. <strong>currentPositionTimeCode</strong>, <em>controles</em>. <strong>currentPositionString</strong>o <em>Controls</em>. <strong>currentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-225"><em>Player6</em>. <strong>CurrentTitle</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="d596c-226">Recupere la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-226">Retrieve the current playlist.</span></span> <span data-ttu-id="d596c-227">Si la lista de reproducción actual es la misma que la lista de reproducción que devuelve el <em>CDROM</em>. <strong>lista de reproducción</strong>, el número de título es el índice del medio actual de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-228"><em>Player6</em>. <strong>CurrentVolume</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="d596c-229">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-230"><em>Player6</em>. <strong>CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="d596c-231">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-231">Not available.</span></span> <span data-ttu-id="d596c-232">En su lugar, use estilos de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d596c-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-233"><em>Player6</em>. <strong>DefaultFrame</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="d596c-234">Usar <em>configuración</em>. <strong>defaultFrame</strong>, o use un</span><span class="sxs-lookup"><span data-stu-id="d596c-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="d596c-235">atributo en el <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="d596c-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-236"><em>Player6</em>. <strong>DisplayBackColor</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="d596c-237">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-238"><em>Player6</em>. <strong>DisplayForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="d596c-239">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="d596c-241">La posición actual se puede recuperar en segundos desde el principio como un <strong>número</strong> mediante <em>controles</em>. <strong>currentPosition</strong>, como una <strong>cadena</strong> con formato HH: mm: SS (horas, minutos, segundos) mediante <em>controles</em>. <strong>currentPositionString</strong>, o en formato de código en tiempo mediante <em>controles</em>. <strong>currentPositionTimeCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-242"><em>Player6</em>. <strong>Desdesempeñar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="d596c-243">La pantalla predeterminada cambia automáticamente de tamaño para ajustarse a los medios.</span><span class="sxs-lookup"><span data-stu-id="d596c-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="d596c-244">Puede establecer las propiedades de alto y ancho en la <OBJECT> etiqueta o en el script.</span><span class="sxs-lookup"><span data-stu-id="d596c-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="d596c-245">Use <em>Player</em>. <strong>pantalla</strong> completa para cambiar al modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="d596c-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-246"><em>Player6</em>. <strong>Duración</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="d596c-247">Usar <em>medios</em>. <strong>duración</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-248"><em>Player6</em>. <strong>DVD</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="d596c-249">Use <em>Player</em>. <strong>DVD</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-250"><em>Player6</em>. <strong>EnableContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="d596c-251">Use <em>Player</em>. <strong>enableContextMenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-252"><em>Player6</em>. <strong>Habilitado</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="d596c-253">Use <em>Player</em>. <strong>habilitada</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-254"><em>Player6</em>. <strong>EnableFullScreenControls</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="d596c-255">Cuando se usa Windows Media Player 9 series o una versión posterior, los controles de pantalla completa se habilitan automáticamente a menos que el <em>jugador</em>. <strong></strong>  =  uiMode &quot; ninguno &quot; .</span><span class="sxs-lookup"><span data-stu-id="d596c-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-256"><em>Player6</em>. <strong>EnablePositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="d596c-257">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-257">Not available.</span></span> <span data-ttu-id="d596c-258">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-259"><em>Player6</em>. <strong>EnableTracker</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="d596c-260">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-260">Not available.</span></span> <span data-ttu-id="d596c-261">Puede proporcionar un control personalizado o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-262"><em>Player6</em>. <strong>EntryCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="d596c-263">Use la <em>lista de reproducción</em>. <strong>recuento</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-264"><em>Player6</em>. <strong>ErrorCode</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="d596c-265">Use <em>ErrorItem</em>. <strong>ErrorCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-266"><em>Player6</em>. <strong>ErrorCorrection</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="d596c-267">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="d596c-269">Use <em>ErrorItem</em>. <strong>errorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-270"><em>Player6</em>. <strong>Nombre de archivo</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="d596c-271">Use <em>Player</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="d596c-272">Usar <em>controles</em>. <strong>CurrentItem</strong> al trabajar en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d596c-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-273"><em>Player6</em>. <strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="d596c-274">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="d596c-276">Use el <em>error</em>. <strong>errorCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-277"><em>Player6</em>. <strong>HasMultipleItems</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="d596c-278">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-279"><em>Player6</em>. <strong>ImageSourceHeight</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="d596c-280">Usar <em>medios</em>. <strong>imageSourceHeight</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-281"><em>Player6</em>. <strong>ImageSourceWidth</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="d596c-282">Usar <em>medios</em>. <strong>imageSourceWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-283"><em>Player6</em>. <strong>InvokeURLs</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="d596c-284">Usar <em>configuración</em>. <strong>invokeURLs</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-285"><em>Player6</em>. <strong>IsBroadcast</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="d596c-286">Usar <em>red</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-287"><em>Player6</em>. <strong>IsDurationValid</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="d596c-288">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-288">Not available.</span></span> <span data-ttu-id="d596c-289"><em>Medios</em>. <strong>Duration</strong> contiene un valor válido cuando se usa con el objeto multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-290"><em>Player6</em>. <strong>Idioma</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="d596c-291">Usar <em>controles</em>. <strong>currentAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-292"><em>Player6</em>. <strong>LostPackets</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="d596c-293">Usar <em>red</em>. <strong>lostPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-294"><em>Player6</em>. <strong>MarkerCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="d596c-295">Usar <em>medios</em>. <strong>markerCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-296"><em>Player6</em>. <strong>Silenciar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="d596c-297">Usar <em>configuración</em>. <strong>silenciar</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-298"><em>Player6</em>. <strong>OpenState</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="d596c-299">Use <em>Player</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-300"><em>Player6</em>. <strong>PlayCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="d596c-301">Usar <em>configuración</em>. <strong>playCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-302"><em>Player6</em>. <strong>PlayState</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="d596c-303">Use <em>Player</em>. <strong>playState</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-304"><em>Player6</em>. <strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="d596c-305">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-305">Not available.</span></span> <span data-ttu-id="d596c-306">Use una estructura de bucle de script con un temporizador HTML para duplicar esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="d596c-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-307"><em>Player6</em>. <strong>Velocidad</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="d596c-308">Usar <em>configuración</em>. <strong>velocidad</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-309"><em>Player6</em>. <strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="d596c-310">Use <em>Player</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-311"><em>Player6</em>. <strong>ReceivedPackets</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="d596c-312">Usar <em>red</em>. <strong>receivedPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-313"><em>Player6</em>. <strong>ReceptionQuality</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="d596c-314">Usar <em>red</em>. <strong>receptionQuality</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-315"><em>Player6</em>. <strong>RecoveredPackets</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="d596c-316">Usar <em>red</em>. <strong>recoveredPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-317"><em>Player6</em>. <strong>Raíz</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="d596c-318">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-319"><em>Player6</em>. <strong>SAMIFileName</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="d596c-320">Use <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-321"><em>Player6</em>. <strong>SAMILang</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="d596c-322">Use <em>ClosedCaption</em>. <strong>SAMILang</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-323"><em>Player6</em>. <strong>SAMIStyle</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="d596c-324">Use <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-325"><em>Player6</em>. <strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="d596c-326">Usar <em>medios</em>. <strong>duración</strong> para determinar la longitud de un objeto <strong>multimedia</strong> .</span><span class="sxs-lookup"><span data-stu-id="d596c-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="d596c-327">Use un marcador con <em>controles</em>. <strong>currentMarker</strong> para especificar una posición final personalizada.</span><span class="sxs-lookup"><span data-stu-id="d596c-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-328"><em>Player6</em>. <strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="d596c-329">Usar <em>controles</em>. <strong>currentPosition</strong> para iniciar la reproducción desde una posición determinada o usar un marcador con <em>controles</em>. <strong>currentMarker</strong> para especificar una posición inicial personalizada.</span><span class="sxs-lookup"><span data-stu-id="d596c-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-330"><em>Player6</em>. <strong>SendErrorEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-331">Los errores se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="d596c-331">Errors are queued.</span></span> <span data-ttu-id="d596c-332">Use el objeto <strong>error</strong> y el objeto <strong>ErrorItem</strong> para recuperar la información de error.</span><span class="sxs-lookup"><span data-stu-id="d596c-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-333"><em>Player6</em>. <strong>SendKeyboardEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-334">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-335"><em>Player6</em>. <strong>SendMouseClickEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-336">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-337"><em>Player6</em>. <strong>SendMouseMoveEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-338">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-339"><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-340">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-341"><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-342">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-343"><em>Player6</em>. <strong>SendWarningEvents</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="d596c-344">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-345"><em>Player6</em>. <strong>ShowAudioControls</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="d596c-346">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-346">Not available.</span></span> <span data-ttu-id="d596c-347">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-348"><em>Player6</em>. <strong>ShowCaptioning</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="d596c-349">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-349">Not available.</span></span> <span data-ttu-id="d596c-350">Puede proporcionar una presentación personalizada de subtítulos.</span><span class="sxs-lookup"><span data-stu-id="d596c-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-351"><em>Player6</em>. <strong>ShowControls</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="d596c-352">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-352">Not available.</span></span> <span data-ttu-id="d596c-353">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-354"><em>Player6</em>. <strong>ShowDisplay</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="d596c-355">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-356"><em>Player6</em>. <strong>ShowGotoBar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="d596c-357">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-357">Not available.</span></span> <span data-ttu-id="d596c-358">Puede proporcionar funcionalidad personalizada mediante el objeto multimedia</span><span class="sxs-lookup"><span data-stu-id="d596c-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-359"><em>Player6</em>. <strong>ShowPositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="d596c-360">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-360">Not available.</span></span> <span data-ttu-id="d596c-361">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-362"><em>Player6</em>. <strong>ShowStatusBar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="d596c-363">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-363">Not available.</span></span> <span data-ttu-id="d596c-364">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-365"><em>Player6</em>. <strong>ShowTracker</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="d596c-366">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-366">Not available.</span></span> <span data-ttu-id="d596c-367">Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d596c-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-368"><em>Player6</em>. <strong>SourceLink</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="d596c-369">Usar <em>medios</em>. <strong>sourceURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-370"><em>Player6</em>. <strong>SourceProtocol</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="d596c-371">Usar <em>red</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-372"><em>Player6</em>. <strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="d596c-373">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-373">Not available.</span></span> <span data-ttu-id="d596c-374">Usar <em>controles</em>. <strong>audioLanguageCount</strong> para recuperar el número de secuencias del lenguaje de audio.</span><span class="sxs-lookup"><span data-stu-id="d596c-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-375"><em>Player6</em>. <strong>Subimagen</strong> en</span><span class="sxs-lookup"><span data-stu-id="d596c-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="d596c-376">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-377"><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-378">No disponible</span><span class="sxs-lookup"><span data-stu-id="d596c-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-379"><em>Player6</em>. <strong>TitlesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-380">Use lo siguiente:<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="d596c-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-381"><em>Player6</em>. <strong>TotalTitleTime</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="d596c-382">Use <em>currentMedia</em>. <strong>Duration</strong> o <em>currentMedia</em>. <strong>durationString</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-383"><em>Player6</em>. <strong>TransparentAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="d596c-384">Use el script para especificar los valores de alto y ancho para que el reproductor sea visible o invisible.</span><span class="sxs-lookup"><span data-stu-id="d596c-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-385"><em>Player6</em>. <strong>UniqueID</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="d596c-386">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="d596c-388">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-389"><em>Player6</em>. <strong>VideoBorderColor</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="d596c-390">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-391"><em>Player6</em>. <strong>VideoBorderWidth</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="d596c-392">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-393"><em>Player6</em>. <strong>Volumen</strong> de</span><span class="sxs-lookup"><span data-stu-id="d596c-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="d596c-394">Usar <em>configuración</em>. <strong>Volumen</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-395"><em>Player6</em>. <strong>VolumesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="d596c-396">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d596c-397">En la tabla siguiente se comparan los métodos del modelo de objetos de Windows Media Player versión 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d596c-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d596c-398">Windows Media Player método 6,4</span><span class="sxs-lookup"><span data-stu-id="d596c-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="d596c-399">Windows Media Player 7 o posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="d596c-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d596c-400"><em>Player6</em>. <strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="d596c-401">Use <em>Player</em>. <strong>versionInfo</strong> para recuperar la versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d596c-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-402"><em>Player6</em>. <strong>BackwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="d596c-403">Usar <em>configuración</em>. <strong>velocidad</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-404"><em>Player6</em>. <strong>ButtonActivate</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="d596c-405">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-406"><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="d596c-407">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-408"><em>Player6</em>. <strong>Cancelar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="d596c-409">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-410"><em>Player6</em>. <strong>ChapterPlay</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="d596c-411">Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="d596c-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="d596c-412">A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.</span><span class="sxs-lookup"><span data-stu-id="d596c-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-413"><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="d596c-414">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-415"><em>Player6</em>. <strong>ChapterSearch</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="d596c-416">Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="d596c-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="d596c-417">A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.</span><span class="sxs-lookup"><span data-stu-id="d596c-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-418"><em>Player6</em>. <strong>Fastforward</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="d596c-419">Usar <em>controles</em>. <strong>fastForward</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-420"><em>Player6</em>. <strong>FastReverse</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="d596c-421">Usar <em>controles</em>. <strong>fastReverse</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-422"><em>Player6</em>. <strong>ForwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="d596c-423">Usar <em>configuración</em>. <strong>velocidad</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-424"><em>Player6</em>. <strong>GetAllGPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="d596c-425">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-426"><em>Player6</em>. <strong>GetAllSPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="d596c-427">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-428"><em>Player6</em>. <strong>GetAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="d596c-429">Usar <em>controles</em>. <strong>currentAudioLanguage</strong> para recuperar el LCID del idioma de audio actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-430"><em>Player6</em>. <strong>GetCodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="d596c-431">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-432"><em>Player6</em>. <strong>GetCodecInstalled</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="d596c-433">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-434"><em>Player6</em>. <strong>GetCodecURL</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="d596c-435">Use <em>ErrorItem</em>. <strong>customUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-436"><em>Player6</em>. <strong>GetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="d596c-437">Use el script para recorrer la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="d596c-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="d596c-438">Usar <em>medios</em>. <strong>isIdentical</strong> para comparar cada entrada de la lista de reproducción con el <em>reproductor</em>. objeto <strong>currentMedia</strong> .</span><span class="sxs-lookup"><span data-stu-id="d596c-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-439"><em>Player6</em>. <strong>GetMarkerName</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="d596c-440">Usar <em>medios</em>. <strong>getMarkerName</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-441"><em>Player6</em>. <strong>GetMarkerTime</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="d596c-442">Usar <em>medios</em>. <strong>getMarkerTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-443"><em>Player6</em>. <strong>GetMediaInfoString</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="d596c-444">Usar <em>medios</em>. <strong>getItemInfo</strong>, <em>media</em>. <strong>getItemInfoByAtom</strong>y sus métodos asociados para recuperar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="d596c-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-445"><em>Player6</em>. <strong>GetMediaParameter</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="d596c-446">Use la <em>lista de reproducción</em>. <strong>elemento</strong> para recuperar un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="d596c-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="d596c-447">A continuación, use los <em>medios</em>. <strong>getItemInfo</strong> para recuperar la cadena de parámetro.</span><span class="sxs-lookup"><span data-stu-id="d596c-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-448"><em>Player6</em>. <strong>GetMediaParameterName</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="d596c-449">Use la <em>lista de reproducción</em>. <strong>elemento</strong> para recuperar un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="d596c-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="d596c-450">A continuación, use los <em>medios</em>. <strong>getAttributeName</strong> para recuperar la cadena de parámetro.</span><span class="sxs-lookup"><span data-stu-id="d596c-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-451"><em>Player6</em>. <strong>GetMoreInfoURL</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="d596c-452">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-453"><em>Player6</em>. <strong>GetNumberOfChapters</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="d596c-454">Si actualmente se está reproduciendo un título, use <em>currentPlaylist</em>. <strong>recuento</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-455"><em>Player6</em>. <strong>GetStreamGroup</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="d596c-456">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-457"><em>Player6</em>. <strong>GetStreamName</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="d596c-458">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-459"><em>Player6</em>. <strong>GetStreamSelected</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="d596c-460">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-461"><em>Player6</em>. <strong>GetSubpictureLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="d596c-462">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-463"><em>Player6</em>. <strong></strong> De</span><span class="sxs-lookup"><span data-stu-id="d596c-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="d596c-464">Use <em>DVD</em>. <strong>atrás</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-465"><em>Player6</em>. <strong>IsSoundCardEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="d596c-466">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-467"><em>Player6</em>. <strong>LeftButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="d596c-468">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-469"><em>Player6</em>. <strong>LowerButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="d596c-470">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-471"><em>Player6</em>. <strong>MenuCall</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="d596c-472">Use <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD</em>. <strong>menú de menús</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-473"><em>Player6</em>. <strong>Siguiente</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="d596c-474">Usar <em>controles</em>. <strong>siguiente</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-475"><em>Player6</em>. <strong>NextPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="d596c-476">Usar <em>controles</em>. <strong>siguiente</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-477"><em>Player6</em>. <strong>Abrir</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="d596c-478">Use <em>Player</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="d596c-479">Los archivos siempre se abren de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d596c-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-480"><em>Player6</em>. <strong>Pausar</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="d596c-481">Usar <em>controles</em>. <strong>pausar</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-482"><em>Player6</em>. <strong>Reproducir</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="d596c-483">Usar <em>controles</em>. <strong>reproducir</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-484"><em>Player6</em>. <strong>Anterior</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="d596c-485">Usar <em>controles</em>. <strong>anterior</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-486"><em>Player6</em>. <strong>PrevPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="d596c-487">Usar <em>controles</em>. <strong>anterior</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-488"><em>Player6</em>. <strong>ResumeFromMenu</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="d596c-489">Use <em>DVD</em>. <strong>reanudar</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-490"><em>Player6</em>. <strong>RightButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="d596c-491">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-492"><em>Player6</em>. <strong>SetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="d596c-493">Recupere un objeto multimedia mediante <em>currentPlaylist</em>. <strong>elemento</strong>(<em>entryNumber</em>).</span><span class="sxs-lookup"><span data-stu-id="d596c-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="d596c-494">A continuación, especifique el objeto multimedia recuperado mediante <em>controles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-495"><em>Player6</em>. <strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="d596c-496">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-497"><em>Player6</em>. <strong>StillOff</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="d596c-498">Usar <em>controles</em>. <strong>reproducir</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="d596c-499">También puede usar <em>controles</em>. <strong>Siguiente</strong> si actualmente está en modo todavía.</span><span class="sxs-lookup"><span data-stu-id="d596c-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-500"><em>Player6</em>. <strong>Detener</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="d596c-501">Usar <em>controles</em>. <strong>detener</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-502"><em>Player6</em>. <strong>StreamSelect</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="d596c-503">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-503">Not available.</span></span> <span data-ttu-id="d596c-504">Usar <em>controles</em>. <strong>currentAudioLanguage</strong> para especificar una secuencia de idioma de audio.</span><span class="sxs-lookup"><span data-stu-id="d596c-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-505"><em>Player6</em>. <strong>TimePlay</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="d596c-506">En la lista de reproducción raíz, use <em>currentPlaylist</em>. <strong>Item</strong>(<em>index</em>) para recuperar un objeto multimedia.</span><span class="sxs-lookup"><span data-stu-id="d596c-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="d596c-507">A continuación, establezca el objeto multimedia como el actual con <em>los controles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="d596c-508">A continuación, especifique <em>controles</em>. <strong>currentPosition</strong> con un valor de tiempo en segundos.</span><span class="sxs-lookup"><span data-stu-id="d596c-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-509"><em>Player6</em>. <strong>TimeSearch</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="d596c-510">Usar <em>controles</em>. <strong>currentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-511"><em>Player6</em>. <strong>TitlePlay</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="d596c-512">Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="d596c-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="d596c-513">A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.</span><span class="sxs-lookup"><span data-stu-id="d596c-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="d596c-514">También puede usar <em>currentPlaylist</em>. <strong>elemento</strong> para recuperar un objeto multimedia y, a continuación, use el objeto multimedia devuelto para especificar <em>controles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="d596c-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-515"><em>Player6</em>. <strong>TopPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="d596c-516">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d596c-517"><em>Player6</em>. <strong>UOPValid</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="d596c-518">No disponible</span><span class="sxs-lookup"><span data-stu-id="d596c-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d596c-519"><em>Player6</em>. <strong>UpperButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="d596c-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="d596c-520">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d596c-521">En la tabla siguiente se comparan los eventos del modelo de objetos de Windows Media Player versión 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d596c-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="d596c-522">Evento 6,4 de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d596c-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="d596c-523">Windows Media Player 7 o posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="d596c-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d596c-524">*Player6*. **Almacenamiento en búfer**</span><span class="sxs-lookup"><span data-stu-id="d596c-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="d596c-525">Use *Player*. **Almacenar en búfer**.</span><span class="sxs-lookup"><span data-stu-id="d596c-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="d596c-526">*Player6*. **Haga clic en**</span><span class="sxs-lookup"><span data-stu-id="d596c-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="d596c-527">Use *Player*. **Haga clic en**</span><span class="sxs-lookup"><span data-stu-id="d596c-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="d596c-528">*Player6*. **DblClick**</span><span class="sxs-lookup"><span data-stu-id="d596c-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="d596c-529">Use *Player*. **DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="d596c-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="d596c-530">*Player6*. **Desconectar**</span><span class="sxs-lookup"><span data-stu-id="d596c-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="d596c-531">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="d596c-532">*Player6*. **DisplayModeChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="d596c-533">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="d596c-534">*Player6*. **DVDNotify**</span><span class="sxs-lookup"><span data-stu-id="d596c-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="d596c-535">*Reproductor*. **DomainChange** y *Player*. **OpenPlaylistSwitch** son eventos específicos del DVD.</span><span class="sxs-lookup"><span data-stu-id="d596c-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="d596c-536">También pueden aplicarse otros eventos relacionados con las listas de reproducción, los medios y los medios de CD-ROM, dependiendo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d596c-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="d596c-537">*Player6*. **EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="d596c-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="d596c-538">Use *Player*. **PlayState**.</span><span class="sxs-lookup"><span data-stu-id="d596c-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="d596c-539">*Player6*. **Error** de</span><span class="sxs-lookup"><span data-stu-id="d596c-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="d596c-540">El evento no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="d596c-540">The event is unchanged.</span></span> <span data-ttu-id="d596c-541">Sin embargo, los errores se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="d596c-541">Errors, however, are queued.</span></span> <span data-ttu-id="d596c-542">Utilice el objeto **error** con el objeto **ErrorItem** para recuperar la información de error de la cola.</span><span class="sxs-lookup"><span data-stu-id="d596c-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="d596c-543">Vea el código de ejemplo de la sección anterior, control de errores.</span><span class="sxs-lookup"><span data-stu-id="d596c-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="d596c-544">*Player6*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="d596c-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="d596c-545">Use *Player*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="d596c-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="d596c-546">*Player6*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="d596c-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="d596c-547">Use *Player*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="d596c-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="d596c-548">*Player6*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="d596c-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="d596c-549">Use *Player*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="d596c-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="d596c-550">*Player6*. **MarkerHit**</span><span class="sxs-lookup"><span data-stu-id="d596c-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="d596c-551">Use *Player*. **MarkerHit**.</span><span class="sxs-lookup"><span data-stu-id="d596c-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="d596c-552">*Player6*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="d596c-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="d596c-553">Use *Player*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="d596c-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="d596c-554">*Player6*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="d596c-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="d596c-555">Use *Player*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="d596c-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="d596c-556">*Player6*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="d596c-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="d596c-557">Use *Player*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="d596c-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="d596c-558">*Player6*. **NewStream**</span><span class="sxs-lookup"><span data-stu-id="d596c-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="d596c-559">Use *Player*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="d596c-560">*Player6*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="d596c-561">Use *Player*. **OpenStateChange**.</span><span class="sxs-lookup"><span data-stu-id="d596c-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="d596c-562">*Player6*. **PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="d596c-563">Use *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="d596c-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="d596c-564">*Player6*. **PositionChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="d596c-565">Use *Player*. **PositionChange**.</span><span class="sxs-lookup"><span data-stu-id="d596c-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="d596c-566">*Player6*. **ReadyStateChange**</span><span class="sxs-lookup"><span data-stu-id="d596c-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="d596c-567">Use *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="d596c-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="d596c-568">*Player6*. **Comando**</span><span class="sxs-lookup"><span data-stu-id="d596c-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="d596c-569">Use *Player*. **Comando**.</span><span class="sxs-lookup"><span data-stu-id="d596c-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="d596c-570">*Player6*. **ADVERTENCIA** de</span><span class="sxs-lookup"><span data-stu-id="d596c-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="d596c-571">No disponible.</span><span class="sxs-lookup"><span data-stu-id="d596c-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d596c-572">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d596c-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d596c-573">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="d596c-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="d596c-574">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="d596c-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





