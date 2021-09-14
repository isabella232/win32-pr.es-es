---
title: Evento ScriptCommand del objeto AxWindowsMediaPlayer
description: El evento ScriptCommand tiene lugar cuando se recibe un comando o una dirección URL sincronizados. | Evento ScriptCommand del objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243357"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento ScriptCommand del objeto AxWindowsMediaPlayer

El evento ScriptCommand tiene lugar cuando se recibe un comando o una dirección URL sincronizados.

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad | Descripción                                                   |
|----------|---------------------------------------------------------------|
| scType   | System.String Especifica el tipo de comando de script.<br/> |
| param    | System.StringEspecifica el comando de script.<br/>         |



 

## <a name="remarks"></a>Observaciones

Los comandos se pueden incrustar entre los sonidos e imágenes de un Windows o secuencia multimedia. Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia. Cuando la secuencia alcanza el tiempo asociado al comando, el control Reproductor de Windows Media envía un **evento ScriptCommand** con dos parámetros. Un parámetro especifica el tipo de comando que se envía y el otro parámetro especifica el comando . El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando. Cualquier tipo de comando se puede incrustar en un archivo o secuencia para que lo controle el **evento ScriptCommand.**

En la tabla siguiente se enumeran los tipos de comandos de script que los Reproductor de Windows Media.



| Tipo                   | Descripción                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| EVENTO                  | El control ejecuta las instrucciones definidas para el evento especificado.                                                                                                  |
| NOMBRE               | El control restablece su propiedad **URL,** intenta abrir el archivo especificado y comienza a reproducir la nueva secuencia inmediatamente.                                        |
| OPENEVENT              | Almacena en búfer el comando event type asociado para la ejecución a tiempo del script EVENT.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | El *parámetro param* contiene el texto sincronizado. Reproductor de Windows Media muestra el texto del cuadro de texto en el área de título cerrada de la **característica Reproducción** ahora. |
| TEXT                   | El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado si IWMPSettings. **La propiedad invokeURLs** se establece en true.                    |



 

Puede insertar cualquier otro tipo de comando siempre que proporcione código para controlar el comando. Aunque el control Reproductor de Windows Media los comandos desconocidos, se siguen entregando al **evento ScriptCommand.**

No se llama al evento ScriptCommand si el archivo se está analizando en modo de avance rápido o rebobinado.

Los comandos de dirección URL recibidos por Reproductor de Windows Media control se invocan automáticamente en el explorador web predeterminado si IWMPSettings. **La propiedad invokeURLs** se establece en true. Puede usar IWMPSettings. **propiedad defaultFrame** para especificar el marco de destino en el que aparece la página web.

La dirección URL enviada a Reproductor de Windows Media se procesa en relación con la dirección URL base especificada por IWMPSettings. **propiedad baseURL.** La dirección URL base se concatena con la dirección URL relativa, lo que da lugar a una dirección URL totalmente especificada que el evento **ScriptCommand** pasa como parámetro de comando.

El Reproductor de Windows Media control siempre procesa los comandos de dirección URL entrantes de la siguiente manera:

1.  Se recibe un comando de tipo URL.
2.  IWMPSettings. **baseURL** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.
3.  Se llama a **ScriptCommand.**
4.  Después **de que scriptCommand** devuelva, IWMPSettings. **InvokeURLs** está activado.
5.  Si IWMPSettings. **invokeURLs** es true y el comando es un comando de dirección URL, se invoca la dirección URL especificada. Si IWMPSettings. **invokeURLs** es false o si el comando no es un comando de dirección URL, el comando se omite.

Al crear un archivo multimedia Windows, puede especificar en qué marco se muestra la nueva dirección URL mediante la concatenación de dos y comercial y el nombre del marco en el campo de parámetro. En el ejemplo siguiente se muestran los parámetros **scriptCommand** típicos. Especifica que la dirección URL *mypage* debe iniciarse en el *marco myframe.*


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



No se llama al evento ScriptCommand si se está analizando el archivo (reenviado o reenviado rápidamente).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.captioningId (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.baseURL (VB y C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.defaultFrame (VB y C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.invokeURLs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





