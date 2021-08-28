---
title: Comparación detallada del modelo de objetos
description: Comparación detallada del modelo de objetos
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Reproductor de Windows Media,modelo de objetos
- Reproductor de Windows Media modelo de objetos, diferencias de versión
- modelo de objetos, diferencias de versión
- Reproductor de Windows Media ActiveX control de versiones, diferencias de versión
- ActiveX control de versiones, diferencias de versión
- Reproductor de Windows Media Control de ActiveX móvil, diferencias de versión
- Reproductor de Windows Media Móvil, modelo de objetos
- guía de migración, diferencias de versión
- versiones de Reproductor de Windows Media,modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f2e092f7e32b889056841b5802dffa141c0be4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884771"
---
# <a name="detailed-object-model-comparison"></a>Comparación detallada del modelo de objetos

En la tabla siguiente se comparan las Reproductor de Windows Media del modelo de objetos 6.4 con Reproductor de Windows Media modelo de objetos 7 o posterior.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Reproductor de Windows Media 6.4</th>
<th>Reproductor de Windows Media 7 o versiones posteriores equivalentes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>La presentación de Reproductor de Windows Media 7 o posterior cambia automáticamente de tamaño para ajustarse a los medios. Puede establecer las propiedades de alto y ancho en la &lt; etiqueta OBJECT o en el &gt; script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Controla</em>. <strong>fastForward y</strong> <em>Controla</em>. <strong>fastReverse se</strong> habilita automáticamente para los tipos de archivo que admiten estos métodos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ángulos disponibles</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Use <em>controles</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoRewind</strong></td>
<td>Use <em>controles</em>. <strong>currentPosition</strong> en el script para especificar o recuperar la posición actual. Como alternativa, use marcadores y <em>player</em>. <strong>evento markerHit.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AutoSize</strong></td>
<td>El ajuste de tamaño automático es el comportamiento predeterminado. Para invalidar el tamaño automático, establezca las propiedades de alto y ancho en la &lt; etiqueta OBJECT o en el &gt; script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Inicio automático</strong></td>
<td>Use <em>Configuración</em>. <strong>autoStart</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Equilibrio</strong></td>
<td>Use <em>Configuración</em>. <strong>equilibra</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ancho de banda</strong></td>
<td>Use <em>Red</em>. <strong>bandWidth</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Use <em>Configuración</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Use <em>Red.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Use <em>Red</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Use <em>Red</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Botones Disponibles</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Use <em>controles</em>. <strong>isAvailable</strong>( &quot; FastForward &quot; ) y <em>controles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Use <em>controles</em>. <strong>isAvailable</strong> para probar si se puede realizar un método de búsqueda determinado.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Use <em>controles</em>. <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ). Use <em>media</em>. <strong>markerCount</strong> para recuperar el recuento de marcadores en un elemento multimedia determinado. Use <em>controles</em>. <strong>currentMarker para</strong> especificar o recuperar el número de marcador actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Use <em>ClosedCaption.</em> <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>No disponible. Consulte <a href="closed-captioning.md">Subtítulos para obtener</a> información sobre cómo han cambiado los subtítulos en Reproductor de Windows Media.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>No disponible. Debe proporcionar controles en la interfaz de usuario para iniciar la reproducción. Como alternativa, el usuario puede hacer clic con el botón derecho en la imagen de vídeo para abrir un menú emergente que contiene una <strong>selección reproducir/pausar</strong> si el <em>reproductor .</em> <strong>enableContextMenu</strong> es igual a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>No disponible. Reproductor de Windows Media serie 9 o posterior permite al usuario seleccionar si se transmite un identificador de reproductor único a los proveedores de contenido.<br/> Si el usuario selecciona esta opción, el Reproductor envía un identificador único al Windows Multimedia. El identificador se registra en el archivo de registro del servidor, ubicado en . <em>Carpeta system32\logfiles</em> de forma predeterminada. El nombre del campo de registro &quot; es c-playerid. &quot; El registro del servidor no está habilitado de forma predeterminada en Servicios de Windows Media.<br/> Si el usuario no selecciona esta opción, el servidor genera un identificador de sesión aleatorio, que es único para cada cliente para una sesión determinada.<br/> Para más información, consulte la documentación Servicios de Windows Media serie 9.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>No disponible. Use <em>Red</em>. <strong>bitRate</strong> para determinar la velocidad de bits actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactAddress</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactPhone</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Use <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar el índice del átomo de fecha de creación. Use <em>media</em>. <strong>getItemInfoByAtom para</strong> recuperar los metadatos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentButton</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentCCService</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Recupere la lista de reproducción actual. Si la lista de reproducción actual no es la misma que la lista de reproducción devuelta por <em>Cdrom</em>. <strong>lista de</strong>reproducción , no hay ningún capítulo actual. De lo contrario, el número de capítulo actual es el índice del medio actual en la lista de reproducción actual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Use <em>DVD</em>. <strong>dominio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Use <em>controles</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Use <em>controles</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Use <em>controles</em>. <strong>currentPositionTimeCode</strong>, <em>Controla</em>. <strong>currentPositionString</strong>o <em>Controles</em>. <strong>currentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recupere la lista de reproducción actual. Si la lista de reproducción actual es la misma que la lista de reproducción devuelta por <em>Cdrom</em>. <strong>playlist</strong>, a continuación, el número de título es el índice del medio actual en la lista de reproducción actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>No disponible. Use Internet Explorer en su lugar.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Use <em>Configuración</em>. <strong>defaultFrame</strong>o use un <PARAM> atributo en el &lt; elemento &gt; OBJECT:
<pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayBackColor</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplayForeColor</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>La posición actual se puede recuperar en segundos desde el principio como <strong>un número</strong> mediante <em>controles</em>. <strong>currentPosition</strong>, como una <strong>cadena</strong> con formato HH:MM:SS (horas, minutos, segundos) mediante <em>controles</em>. <strong>currentPositionString</strong>o en formato de código de tiempo mediante <em>controles</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplaySize</strong></td>
<td>La pantalla predeterminada cambia automáticamente de tamaño para ajustarse al medio. Puede establecer las propiedades de alto y ancho en la &lt; etiqueta OBJECT o en el &gt; script. Use <em>el reproductor</em>. <strong>fullScreen</strong> para cambiar al modo de pantalla completa.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Duración</strong></td>
<td>Use <em>Media</em>. <strong>duration</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Use <em>el reproductor</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Use <em>el reproductor</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Habilitado</strong></td>
<td>Use <em>el reproductor</em>. <strong>habilitado.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Al usar Reproductor de Windows Media serie 9 o posterior, los controles de pantalla completa se habilitan automáticamente a menos que el <em>Reproductor de</em>. <strong>uiMode</strong>  =  &quot; &quot;ninguno.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>Reproductor de</em>. <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>No disponible. Puede proporcionar un control personalizado o usar el <em>Reproductor de</em>. <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Use lista <em>de reproducción</em>. <strong>count</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Código de error</strong></td>
<td>Use <em>ErrorItem</em>. <strong>errorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Use <em>ErrorItem</em>. <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FileName</strong></td>
<td>Use <em>el reproductor</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>. Use <em>controles</em>. <strong>currentItem cuando</strong> se trabaja dentro de una lista de reproducción.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Use <em>el error</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Use <em>Media</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Use <em>Media</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Use <em>Configuración</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Use <em>Red</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>No disponible. <em>Multimedia</em>. <strong>duration</strong> contiene un valor válido cuando se usa con el objeto multimedia actual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Idioma</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Use <em>Red</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Use <em>Media</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Exclusión mutua</strong></td>
<td>Use <em>Configuración</em>. <strong>mute</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Use <em>el reproductor</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Use <em>Configuración</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Use <em>player</em>. <strong>playState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>No disponible. Use una estructura de bucle de script con un temporizador HTML para duplicar esta funcionalidad.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Velocidad</strong></td>
<td>Use <em>Configuración</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Use <em>player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Use <em>Red</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Use <em>Red</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Use <em>Red</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Raíz</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Use <em>ClosedCaption.</em> <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Use <em>ClosedCaption.</em> <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Use <em>ClosedCaption.</em> <strong>SAMIStyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Use <em>media</em>. <strong>duración</strong> para determinar la longitud de un <strong>objeto</strong> Multimedia. Use un marcador con <em>Controles</em>. <strong>currentMarker para</strong> especificar una posición final personalizada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Use <em>controles</em>. <strong>currentPosition</strong> para iniciar la reproducción desde una posición determinada o usar un marcador con <em>Controles</em>. <strong>currentMarker para</strong> especificar una posición inicial personalizada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Los errores se ponen en cola. Use el <strong>objeto Error</strong> y el <strong>objeto ErrorItem</strong> para recuperar información de error.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendKeyboardEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendMouseClickEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendMouseMoveEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendWarningEvents</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowAudioControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o <em>usar</em>player . <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>No disponible. Puede proporcionar una presentación personalizada de subtítulos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o <em>usar</em>player . <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>No disponible. Puede proporcionar funcionalidad personalizada mediante el objeto Multimedia.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o <em>usar</em>player . <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o <em>usar</em>player . <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o <em>usar</em>player . <strong>uimode para</strong> elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Use <em>media</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Use <em>Red</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>No disponible. Use <em>controles</em>. <strong>audioLanguageCount para</strong> recuperar el número de secuencias de idioma de audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SubpictureOn</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>No disponible</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Use lo siguiente:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Use <em>currentMedia.</em> <strong>duration</strong> o <em>currentMedia.</em> <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Use el script para especificar los valores de alto y ancho para que el reproductor sea visible o invisible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>VideoBorderColor</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorderWidth</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volumen</strong></td>
<td>Use <em>Configuración</em>. <strong>Volumen</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Volúmenes disponibles</strong></td>
<td>No disponible.</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se comparan los Reproductor de Windows Media modelo de objetos de la versión 6.4 con el modelo de objetos Reproductor de Windows Media 7 o posterior.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Reproductor de Windows Media método 6.4</th>
<th>Reproductor de Windows Media 7 o versiones posteriores equivalentes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Use <em>el reproductor</em>. <strong>versionInfo</strong> para recuperar la versión de Reproductor de Windows Media.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Use <em>Configuración</em>. <strong>rate</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ButtonActivate</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Cancelar</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterPlay</strong></td>
<td>Si ya está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia mediante la sintaxis siguiente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> mediante el objeto multimedia devuelto.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Si ya está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia mediante la sintaxis siguiente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> mediante el objeto multimedia devuelto.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Use <em>controles</em>. <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Use <em>controles</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Use <em>Configuración</em>. <strong>rate</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAllGPRMs</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetAllSPRMs</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAudioLanguage</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguage para</strong> recuperar el LCID del idioma de audio actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecDescription</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCodecInstalled</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecURL</strong></td>
<td>Use <em>ErrorItem</em>. <strong>customUrl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Use el script para recorrer en bucle la lista de reproducción actual. Use <em>Media</em>. <strong>isIdentical para</strong> comparar cada entrada de la lista de reproducción con el <em>reproductor</em>. <strong>objeto currentMedia.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Use <em>Media</em>. <strong>getMarkerName</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Use <em>Media</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Use <em>Media</em>. <strong>getItemInfo</strong>, <em>Media</em>. <strong>getItemInfoByAtom</strong>y sus métodos asociados para recuperar metadatos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Use lista <em>de reproducción</em>. <strong>elemento para</strong> recuperar un elemento multimedia. A continuación, use <em>Media</em>. <strong>getItemInfo para</strong> recuperar la cadena de parámetro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Use lista <em>de reproducción</em>. <strong>elemento para</strong> recuperar un elemento multimedia. A continuación, use <em>Media</em>. <strong>getAttributeName para</strong> recuperar la cadena de parámetro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Si un título se está reproduciendo actualmente, use <em>currentPlaylist</em>. <strong>count</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamGroup</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamSelected</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetSubpictureLanguage</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GoUp</strong></td>
<td>Use <em>DVD</em>. <strong>back</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Is SoundCardEnabled</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>LeftButtonSelect</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LowerButtonSelect</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MenuCall</strong></td>
<td>Use <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD</em>. <strong>topMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Siguiente</strong></td>
<td>Use <em>controles</em>. <strong>a continuación,</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Use <em>controles</em>. <strong>a continuación,</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abrir</strong></td>
<td>Use <em>el reproductor</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>. Los archivos siempre se abren de forma asincrónica.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Pausar</strong></td>
<td>Use <em>controles</em>. <strong>pause</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Reproducir</strong></td>
<td>Use <em>controles</em>. <strong>reproducir</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Anterior</strong></td>
<td>Use <em>controles</em>. <strong>anterior.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Use <em>controles</em>. <strong>anterior.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Use <em>DVD</em>. <strong>resume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recupere un objeto multimedia mediante <em>currentPlaylist</em>. <strong>item</strong>(<em>entryNumber</em>). A continuación, especifique el objeto multimedia recuperado mediante <em>Controles</em>. <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Use <em>controles</em>. <strong>reproducir</strong>. Como alternativa, use <em>Controles</em>. <strong>A continuación,</strong> si actualmente está en modo de mantenimiento.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Detener</strong></td>
<td>Use <em>controles</em>. <strong>detenga</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>No disponible. Use <em>controles</em>. <strong>currentAudioLanguage para</strong> especificar una secuencia de idioma de audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>En la lista de reproducción raíz, use <em>currentPlaylist</em>. <strong>item</strong>(<em>index</em>) para recuperar un objeto multimedia. A continuación, establezca el objeto multimedia como el actual mediante <em>Controles</em>. <strong>currentItem</strong>. A continuación, especifique <em>Controles</em>. <strong>currentPosition</strong> con un valor de tiempo en segundos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Use <em>controles</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Si ya está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia mediante la sintaxis siguiente:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> mediante el objeto multimedia devuelto.<br/> Como alternativa, use <em>currentPlaylist</em>. <strong>elemento</strong> para recuperar un objeto multimedia y, a continuación, usar el objeto multimedia devuelto para especificar <em>Controles</em>. <strong>currentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TopPGSearch</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>UOPValid</strong></td>
<td>No disponible</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UpperButtonSelect</strong></td>
<td>No disponible.</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se comparan los eventos Reproductor de Windows Media modelo de objetos de la versión 6.4 con Reproductor de Windows Media modelo de objetos 7 o posterior.



| Reproductor de Windows Media evento 6.4  | Reproductor de Windows Media 7 o posterior equivalente                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Almacenamiento en búfer**         | Use *el reproductor*. **Almacenar en búfer**.                                                                                                                                                                                              |
| *Player6*. **Haga clic en**             | Use *el reproductor*. **Haga clic en**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Use *el reproductor*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Desconectar**        | No disponible.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | No disponible.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Player*. **DomainChange** y *Player*. **OpenPlaylistSwitch** son eventos específicos de DVD. También se pueden aplicar otros eventos relacionados con listas de reproducción, medios y medios de CD-ROM en función de la aplicación.                        |
| *Player6*. **EndOfStream**       | Use *el reproductor*. **PlayState**.                                                                                                                                                                                              |
| *Player6*. **Error**             | El evento no se modifica. Sin embargo, los errores se ponen en cola. Use el **objeto Error** con el **objeto ErrorItem** para recuperar información de error de la cola. Vea el código de ejemplo de la sección anterior, Control de errores. |
| *Player6*. **KeyDown**           | Use *el reproductor*. **Keydown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Use *el reproductor*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Use *el reproductor*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Use *el reproductor*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Use *el reproductor*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Use *el reproductor*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Use *el reproductor*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Use *el reproductor*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Use *el reproductor*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Use *el reproductor*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Use *el reproductor*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Use *el reproductor*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **ScriptCommand**     | Use *el reproductor*. **ScriptCommand**.                                                                                                                                                                                          |
| *Player6*. **Advertencia**           | No disponible.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





