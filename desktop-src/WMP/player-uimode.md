---
title: Player. uiMode
description: La propiedad uiMode especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Media Player de Windows Player. uiMode
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708762"
---
# <a name="playeruimode"></a>Player. uiMode

La propiedad **uiMode** especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.

## <a name="syntax"></a>Sintaxis

*reproductor* . **uiMode**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.



| Value     | Descripción                                                                                                                                                                                                           | Ejemplo de audio                                          | Ejemplo de vídeo                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisibles | Windows Media Player está incrustado sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).                                                                                                        | (No se muestra nada).                                | (No se muestra nada).                                |
| ninguno      | Windows Media Player está incrustado sin controles y solo se muestra la ventana de vídeo o visualización.                                                                                                         | !["ninguno" con audio](images/uimode-none-audio-v11.png) | !["ninguno" con vídeo](images/uimode-none-video-v11.png) |
| pequeño      | Windows Media Player está incrustado con los controles ventana de estado, reproducir/pausar, detener, silenciar y volumen mostrados además de la ventana de vídeo o visualización.                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con vídeo](images/uimode-mini-video-v11.png) |
| full      | Predeterminada. Windows Media Player está incrustado con la ventana de estado, la barra de búsqueda, los controles de reproducción/pausa, detención, silencio, siguiente, anterior, avance rápido, retroceso rápido y volumen, además de la ventana de vídeo o visualización. | !["completo" con audio](images/uimode-full-audio-v11.png) | !["completo" con vídeo](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player está incrustado con una interfaz de usuario personalizada. Solo se puede usar en programas de C++.                                                                                                                      | (Se muestra la interfaz de usuario personalizada).                  | (Se muestra la interfaz de usuario personalizada).                  |



 

## <a name="remarks"></a>Observaciones

Esta propiedad especifica la apariencia del Media Player de Windows incrustado. Cuando **uiMode** se establece en "none", "mini" o "Full", hay una ventana para la presentación de clips de vídeo y visualizaciones de audio. Esta ventana se puede ocultar en el modo mini o completo estableciendo el atributo de **alto** de la etiqueta de **objeto** en 40, que se mide desde la parte inferior, y deja visible la parte controles de la interfaz de usuario. Si no se desea ninguna interfaz incrustada, establezca los atributos **ancho** y **alto** en cero.

Si **uiMode** se establece en "invisible", no se muestra ninguna interfaz de usuario, pero el espacio se reserva en la página según lo especificado en **ancho** y **alto**. Esto resulta útil para conservar el diseño de página cuando **uiMode** puede cambiar. Además, el espacio reservado es transparente, por lo que todos los elementos que estén en capas detrás del control serán visibles.

Si **uiMode** se establece en "Full" o "mini", Windows Media Player muestra los controles de transporte en modo de pantalla completa. Si **uiMode** se establece en "none", no se muestra ningún control en el modo de pantalla completa.

Si la ventana está visible y el contenido de audio se está reproduciendo, la visualización que se muestra será la que se usó más recientemente en Windows Media Player.

Si **uiMode** se establece en "Custom" en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado por **IWMPRemoteMediaServices:: GetCustomUIMode** .

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento SELECT de HTML que permite al usuario cambiar la interfaz de usuario para un objeto **reproductor** incrustado. El objeto **Player** se creó con ID = "Player".


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



Windows Media Player 10 Mobile: esta propiedad solo acepta o devuelve los valores "none" o "Full". En dispositivos Smartphone, solo se muestran el estado de reproducción y un contador cuando *uiMode* se establece en "Full".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior. Windows Media Player 9 series o posterior para "invisible" o "personalizado".<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





