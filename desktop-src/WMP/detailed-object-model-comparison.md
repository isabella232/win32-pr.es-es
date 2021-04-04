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
# <a name="detailed-object-model-comparison"></a>Comparación detallada del modelo de objetos

En la tabla siguiente se comparan las propiedades del modelo de objetos de Windows Media Player 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad 6,4 de Windows Media Player</th>
<th>Windows Media Player 7 o posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>La presentación de Windows Media Player 7 o posterior cambia automáticamente de tamaño para ajustarse a los medios. Puede establecer las propiedades de alto y ancho en la <OBJECT> etiqueta o en el script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Controles</em>. <strong>fastForward</strong> y <em>controles</em>. <strong>fastReverse</strong> se habilitan automáticamente para los tipos de archivo que admiten estos métodos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AnglesAvailable</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Usar <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Usar <em>controles</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoRewind</strong></td>
<td>Usar <em>controles</em>. <strong>currentPosition</strong> en el script para especificar o recuperar la posición actual. También puede usar marcadores y el <em>reproductor</em>. evento <strong>markerHit</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Ajustar tamaño automáticamente</strong></td>
<td>El ajuste de tamaño automático es el comportamiento predeterminado. Para invalidar el tamaño automático, establezca las propiedades Height y width en la <OBJECT> etiqueta o en el script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Inicio automático</strong></td>
<td>Usar <em>configuración</em>. <strong>Inicio automático</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Usar <em>configuración</em>. <strong>saldo</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ancho de banda</strong></td>
<td>Usar <em>red</em>. <strong>ancho de banda</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Baseurl</strong></td>
<td>Usar <em>configuración</em>. <strong>baseurl</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Usar <em>red.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Usar <em>red</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Usar <em>red</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonsAvailable</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Usar <em>controles</em>. <strong>isavailable</strong>( &quot; Fastforward &quot; ) y <em>controles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Usar <em>controles</em>. <strong>isavailable</strong> para probar si se puede realizar un método de búsqueda concreto.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Usar <em>controles</em>. <strong>isavailable</strong>( &quot; CurrentMarker &quot; ). Usar <em>medios</em>. <strong>markerCount</strong> para recuperar el recuento de marcadores de un elemento multimedia determinado. Usar <em>controles</em>. <strong>currentMarker</strong> para especificar o recuperar el número de marcador actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>No disponible. Consulte <a href="closed-captioning.md">subtítulos (CC</a> ) para obtener información acerca de cómo ha cambiado el subtítulos (CC) en Windows Media Player.</td>
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
<td>No disponible. Debe proporcionar controles en la interfaz de usuario para iniciar la reproducción. Como alternativa, el usuario puede hacer clic con el botón secundario en la imagen de vídeo para abrir un menú emergente que contiene una selección de <strong>reproducción/pausa</strong> si es el <em>jugador</em>. <strong>enableContextMenu</strong> es igual a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>No disponible. Windows Media Player 9 series o posterior permite al usuario seleccionar si se transmite un identificador de reproductor único a los proveedores de contenido.<br/> Si el usuario selecciona esta opción, el reproductor envía un identificador único al servidor de Windows Media. El identificador se registra en el archivo de registro del servidor, que se encuentra en. <em>system32\logfiles</em> de forma predeterminada. El nombre del campo de registro es &quot; c-playerid &quot; . El registro del servidor no está habilitado de forma predeterminada en Windows Media Services.<br/> Si el usuario no selecciona esta opción, el servidor genera un identificador de sesión aleatorio, que es único para cada cliente para una sesión determinada.<br/> Para obtener más información, consulte la documentación de Windows Media Services 9 series.<br/></td>
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
<td>No disponible. Usar <em>red</em>. <strong>velocidad</strong> de bits para determinar la velocidad de bits actual.</td>
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
<td>Use <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar el índice del átomo de fecha de creación. Usar <em>medios</em>. <strong>getItemInfoByAtom</strong> para recuperar los metadatos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Usar <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
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
<td>Recupere la lista de reproducción actual. Si la lista de reproducción actual no es la misma que la lista de reproducción que devuelve el <em>CDROM</em>. <strong>lista de reproducción</strong>, no hay ningún capítulo actual. De lo contrario, el número de capítulo actual es el índice del medio actual de la lista de reproducción actual.</td>
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
<td>Usar <em>controles</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Usar <em>controles</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Usar <em>controles</em>. <strong>currentPositionTimeCode</strong>, <em>controles</em>. <strong>currentPositionString</strong>o <em>Controls</em>. <strong>currentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recupere la lista de reproducción actual. Si la lista de reproducción actual es la misma que la lista de reproducción que devuelve el <em>CDROM</em>. <strong>lista de reproducción</strong>, el número de título es el índice del medio actual de la lista de reproducción actual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>No disponible. En su lugar, use estilos de Internet Explorer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Usar <em>configuración</em>. <strong>defaultFrame</strong>, o use un <PARAM> atributo en el <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
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
<td>La posición actual se puede recuperar en segundos desde el principio como un <strong>número</strong> mediante <em>controles</em>. <strong>currentPosition</strong>, como una <strong>cadena</strong> con formato HH: mm: SS (horas, minutos, segundos) mediante <em>controles</em>. <strong>currentPositionString</strong>, o en formato de código en tiempo mediante <em>controles</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Desdesempeñar</strong></td>
<td>La pantalla predeterminada cambia automáticamente de tamaño para ajustarse a los medios. Puede establecer las propiedades de alto y ancho en la <OBJECT> etiqueta o en el script. Use <em>Player</em>. <strong>pantalla</strong> completa para cambiar al modo de pantalla completa.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Duración</strong> de</td>
<td>Usar <em>medios</em>. <strong>duración</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong> de</td>
<td>Use <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Use <em>Player</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Habilitado</strong></td>
<td>Use <em>Player</em>. <strong>habilitada</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Cuando se usa Windows Media Player 9 series o una versión posterior, los controles de pantalla completa se habilitan automáticamente a menos que el <em>jugador</em>. <strong></strong>  =  uiMode &quot; ninguno &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>No disponible. Puede proporcionar un control personalizado o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Use la <em>lista de reproducción</em>. <strong>recuento</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Use <em>ErrorItem</em>. <strong>ErrorCode</strong>.</td>
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
<td><em>Player6</em>. <strong>Nombre de archivo</strong></td>
<td>Use <em>Player</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>. Usar <em>controles</em>. <strong>CurrentItem</strong> al trabajar en una lista de reproducción.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Use el <em>error</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Usar <em>medios</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Usar <em>medios</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Usar <em>configuración</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Usar <em>red</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>No disponible. <em>Medios</em>. <strong>Duration</strong> contiene un valor válido cuando se usa con el objeto multimedia actual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Idioma</strong> de</td>
<td>Usar <em>controles</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Usar <em>red</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Usar <em>medios</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Silenciar</strong></td>
<td>Usar <em>configuración</em>. <strong>silenciar</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Use <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Usar <em>configuración</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Use <em>Player</em>. <strong>playState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>No disponible. Use una estructura de bucle de script con un temporizador HTML para duplicar esta funcionalidad.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Velocidad</strong> de</td>
<td>Usar <em>configuración</em>. <strong>velocidad</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Use <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Usar <em>red</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Usar <em>red</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Usar <em>red</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Raíz</strong> de</td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Usar <em>medios</em>. <strong>duración</strong> para determinar la longitud de un objeto <strong>multimedia</strong> . Use un marcador con <em>controles</em>. <strong>currentMarker</strong> para especificar una posición final personalizada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Usar <em>controles</em>. <strong>currentPosition</strong> para iniciar la reproducción desde una posición determinada o usar un marcador con <em>controles</em>. <strong>currentMarker</strong> para especificar una posición inicial personalizada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Los errores se ponen en cola. Use el objeto <strong>error</strong> y el objeto <strong>ErrorItem</strong> para recuperar la información de error.</td>
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
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>No disponible. Puede proporcionar una presentación personalizada de subtítulos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>No disponible. Puede proporcionar funcionalidad personalizada mediante el objeto multimedia</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>No disponible. Puede proporcionar controles personalizados o usar el <em>reproductor</em>. <strong>uiMode</strong> para elegir una configuración predeterminada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Usar <em>medios</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Usar <em>red</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>No disponible. Usar <em>controles</em>. <strong>audioLanguageCount</strong> para recuperar el número de secuencias del lenguaje de audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Subimagen</strong> en</td>
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
<td>Use <em>currentMedia</em>. <strong>Duration</strong> o <em>currentMedia</em>. <strong>durationString</strong>.</td>
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
<td><em>Player6</em>. <strong>Volumen</strong> de</td>
<td>Usar <em>configuración</em>. <strong>Volumen</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>No disponible.</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se comparan los métodos del modelo de objetos de Windows Media Player versión 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player método 6,4</th>
<th>Windows Media Player 7 o posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Use <em>Player</em>. <strong>versionInfo</strong> para recuperar la versión de Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Usar <em>configuración</em>. <strong>velocidad</strong>.</td>
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
<td>Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Fastforward</strong></td>
<td>Usar <em>controles</em>. <strong>fastForward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Usar <em>controles</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Usar <em>configuración</em>. <strong>velocidad</strong>.</td>
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
<td>Usar <em>controles</em>. <strong>currentAudioLanguage</strong> para recuperar el LCID del idioma de audio actual.</td>
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
<td>Use el script para recorrer la lista de reproducción actual. Usar <em>medios</em>. <strong>isIdentical</strong> para comparar cada entrada de la lista de reproducción con el <em>reproductor</em>. objeto <strong>currentMedia</strong> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Usar <em>medios</em>. <strong>getMarkerName</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Usar <em>medios</em>. <strong>getMarkerTime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Usar <em>medios</em>. <strong>getItemInfo</strong>, <em>media</em>. <strong>getItemInfoByAtom</strong>y sus métodos asociados para recuperar los metadatos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Use la <em>lista de reproducción</em>. <strong>elemento</strong> para recuperar un elemento multimedia. A continuación, use los <em>medios</em>. <strong>getItemInfo</strong> para recuperar la cadena de parámetro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Use la <em>lista de reproducción</em>. <strong>elemento</strong> para recuperar un elemento multimedia. A continuación, use los <em>medios</em>. <strong>getAttributeName</strong> para recuperar la cadena de parámetro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>No disponible.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Si actualmente se está reproduciendo un título, use <em>currentPlaylist</em>. <strong>recuento</strong>.</td>
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
<td><em>Player6</em>. <strong></strong> De</td>
<td>Use <em>DVD</em>. <strong>atrás</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsSoundCardEnabled</strong></td>
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
<td>Use <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD</em>. <strong>menú de menús</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Siguiente</strong></td>
<td>Usar <em>controles</em>. <strong>siguiente</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Usar <em>controles</em>. <strong>siguiente</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abrir</strong></td>
<td>Use <em>Player</em>. <strong>Dirección URL</strong> o <em>reproductor</em>. <strong>currentMedia</strong>. Los archivos siempre se abren de forma asincrónica.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Pausar</strong></td>
<td>Usar <em>controles</em>. <strong>pausar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Reproducir</strong></td>
<td>Usar <em>controles</em>. <strong>reproducir</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Anterior</strong></td>
<td>Usar <em>controles</em>. <strong>anterior</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Usar <em>controles</em>. <strong>anterior</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Use <em>DVD</em>. <strong>reanudar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recupere un objeto multimedia mediante <em>currentPlaylist</em>. <strong>elemento</strong>(<em>entryNumber</em>). A continuación, especifique el objeto multimedia recuperado mediante <em>controles</em>. <strong>CurrentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>No disponible.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Usar <em>controles</em>. <strong>reproducir</strong>. También puede usar <em>controles</em>. <strong>Siguiente</strong> si actualmente está en modo todavía.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Detener</strong></td>
<td>Usar <em>controles</em>. <strong>detener</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>No disponible. Usar <em>controles</em>. <strong>currentAudioLanguage</strong> para especificar una secuencia de idioma de audio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TimePlay</strong></td>
<td>En la lista de reproducción raíz, use <em>currentPlaylist</em>. <strong>Item</strong>(<em>index</em>) para recuperar un objeto multimedia. A continuación, establezca el objeto multimedia como el actual con <em>los controles</em>. <strong>CurrentItem</strong>. A continuación, especifique <em>controles</em>. <strong>currentPosition</strong> con un valor de tiempo en segundos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TimeSearch</strong></td>
<td>Usar <em>controles</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Si ya se está reproduciendo la lista de reproducción de título especificada, recupere el capítulo deseado como un objeto multimedia con la siguiente sintaxis:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
A continuación, especifique <em>Player</em>. <strong>currentMedia</strong> con el objeto multimedia devuelto.<br/> También puede usar <em>currentPlaylist</em>. <strong>elemento</strong> para recuperar un objeto multimedia y, a continuación, use el objeto multimedia devuelto para especificar <em>controles</em>. <strong>CurrentItem</strong>.<br/></td>
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



 

En la tabla siguiente se comparan los eventos del modelo de objetos de Windows Media Player versión 6,4 con el modelo de objetos de Windows Media Player 7 o posterior.



| Evento 6,4 de Windows Media Player  | Windows Media Player 7 o posterior equivalente                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Almacenamiento en búfer**         | Use *Player*. **Almacenar en búfer**.                                                                                                                                                                                              |
| *Player6*. **Haga clic en**             | Use *Player*. **Haga clic en**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Use *Player*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Desconectar**        | No disponible.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | No disponible.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Reproductor*. **DomainChange** y *Player*. **OpenPlaylistSwitch** son eventos específicos del DVD. También pueden aplicarse otros eventos relacionados con las listas de reproducción, los medios y los medios de CD-ROM, dependiendo de la aplicación.                        |
| *Player6*. **EndOfStream**       | Use *Player*. **PlayState**.                                                                                                                                                                                              |
| *Player6*. **Error** de             | El evento no se ha modificado. Sin embargo, los errores se ponen en cola. Utilice el objeto **error** con el objeto **ErrorItem** para recuperar la información de error de la cola. Vea el código de ejemplo de la sección anterior, control de errores. |
| *Player6*. **KeyDown**           | Use *Player*. **KeyDown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Use *Player*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Use *Player*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Use *Player*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Use *Player*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Use *Player*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Use *Player*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Use *Player*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Use *Player*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Use *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Use *Player*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Use *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **Comando**     | Use *Player*. **Comando**.                                                                                                                                                                                          |
| *Player6*. **ADVERTENCIA** de           | No disponible.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





