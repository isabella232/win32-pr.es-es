---
title: Player.uiMode
description: La propiedad uiMode especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Player.uiMode Reproductor de Windows Media
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
ms.openlocfilehash: f082da34ffc3b77869e84ceb576b4e6273ccaff15a5f95e66d98cae93697c251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835376"
---
# <a name="playeruimode"></a>Player.uiMode

La **propiedad uiMode** especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario.

## <a name="syntax"></a>Syntax

*player* . **uiMode**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura **y escritura.**



| Valor     | Descripción                                                                                                                                                                                                           | Ejemplo de audio                                          | Ejemplo de vídeo                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| invisibles | Reproductor de Windows Media se inserta sin ninguna interfaz de usuario visible (controles, vídeo o ventana de visualización).                                                                                                        | (No se muestra nada).                                | (No se muestra nada).                                |
| ninguno      | Reproductor de Windows Media se inserta sin controles y solo se muestra la ventana de vídeo o visualización.                                                                                                         | !["none" con audio](images/uimode-none-audio-v11.png) | !["none" con vídeo](images/uimode-none-video-v11.png) |
| Mini      | Reproductor de Windows Media se inserta con los controles de ventana de estado, reproducir/pausar, detener, silenciar y volumen que se muestran además de la ventana de vídeo o visualización.                                                          | !["mini" con audio](images/uimode-mini-audio-v11.png) | !["mini" con vídeo](images/uimode-mini-video-v11.png) |
| full      | Predeterminada. Reproductor de Windows Media se incrusta con la ventana de estado, buscar barra, reproducir/pausar, detener, silenciar, siguiente, anterior, avance rápido, invertir rápido y controles de volumen además de la ventana de vídeo o visualización. | !["full" con audio](images/uimode-full-audio-v11.png) | !["full" con vídeo](images/uimode-full-video-v11.png) |
| custom    | Reproductor de Windows Media se inserta con una interfaz de usuario personalizada. Solo se puede usar en programas de C++.                                                                                                                      | (Se muestra la interfaz de usuario personalizada).                  | (Se muestra la interfaz de usuario personalizada).                  |



 

## <a name="remarks"></a>Comentarios

Esta propiedad especifica la apariencia del Reproductor de Windows Media. Cuando **uiMode** se establece en "none", "mini" o "full", hay una ventana para mostrar clips de vídeo y visualizaciones de audio. Esta ventana se puede ocultar en modo mini o completo estableciendo el atributo **height** de la etiqueta **OBJECT** en 40, que se mide desde la parte inferior, y deja visible la parte de los controles de la interfaz de usuario. Si no se desea ninguna interfaz incrustada, establezca los atributos **de** ancho y **alto** en cero.

Si **uiMode** está establecido en "invisible", no se muestra ninguna interfaz de usuario, pero el espacio todavía está reservado en la página según lo especificado por **ancho** y **alto.** Esto es útil para conservar el diseño de página cuando **uiMode** puede cambiar. Además, el espacio reservado es transparente, por lo que todos los elementos situados detrás del control serán visibles.

Si **uiMode** está establecido en "full" o "mini", Reproductor de Windows Media controles de transporte en modo de pantalla completa. Si **uiMode** está establecido en "none", no se muestra ningún control en modo de pantalla completa.

Si la ventana está visible y se reproduce el contenido de audio, la visualización mostrada será la que se usó más recientemente en Reproductor de Windows Media.

Si **uiMode** se establece en "custom" en un programa de C++ que implementa **IWMPRemoteMediaServices**, se muestra el archivo de máscara indicado **por IWMPRemoteMediaServices::GetCustomUIMode.**

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento SELECT HTML que permite al usuario cambiar la interfaz de usuario de un objeto **Player** incrustado. El **objeto Player** se creó con id. = "Player".


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



Reproductor de Windows Media 10 Mobile: esta propiedad solo acepta o devuelve valores de "none" o "full". En los dispositivos Smartphone, solo se muestran el estado de reproducción y un contador cuando *uiMode* está establecido en "full".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior. Reproductor de Windows Media serie 9 o posterior para "invisible" o "personalizado".<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPRemoteMediaServices (Interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[**IWMPRemoteMediaServices::GetCustomUIMode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





