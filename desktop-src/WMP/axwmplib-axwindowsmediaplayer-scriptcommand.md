---
title: Evento comando del objeto AxWindowsMediaPlayer
description: El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados. | Evento comando del objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento comando del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699706"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>Evento comando del objeto AxWindowsMediaPlayer

El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados.

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
| scType   | System. StringSpecifies el tipo de comando de script.<br/> |
| param    | System. StringSpecifies el comando de script.<br/>         |



 

## <a name="remarks"></a>Observaciones

Los comandos se pueden insertar entre los sonidos e imágenes de un archivo o una secuencia de Windows Media. Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia. Cuando el flujo alcanza el tiempo asociado con el comando, el control Media Player de Windows envía un evento **comando** con dos parámetros. Un parámetro especifica el tipo de comando que se va a enviar y el otro parámetro especifica el comando. El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando. Cualquier tipo de comando se puede incrustar en un archivo o una secuencia para que lo controle el evento **comando** .

En la tabla siguiente se enumeran los tipos de comando de script que Windows Media Player procesa automáticamente.



| Tipo                   | Descripción                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| CESO                  | El control ejecuta instrucciones definidas para el evento especificado.                                                                                                  |
| EXTENSIÓN               | El control restablece su propiedad de **dirección URL** , intenta abrir el archivo especificado y comienza a reproducir el nuevo flujo inmediatamente.                                        |
| OPENEVENT              | Almacena en búfer el comando de tipo de evento asociado para la ejecución oportuna del script de eventos.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | El parámetro *param* contiene el texto de letra sincronizado. Windows Media Player muestra el texto de letra en el área de subtítulos (CC) de la característica de **reproducción en curso** . |
| TEXT                   | El control muestra el texto asociado en el elemento HTML especificado por IWMPClosedCaption. **captioningId**.                                                       |
| URL                    | El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado si IWMPSettings. la propiedad **invokeURLs** está establecida en true.                    |



 

Puede incrustar cualquier otro tipo de comando siempre que proporcione código para controlar el comando. Aunque el control de Windows Media Player omite los comandos desconocidos, se siguen entregando al evento **comando** .

No se llama al evento comando si el archivo se está examinando en modo de avance rápido o de rebobinado.

Los comandos de dirección URL recibidos por el control Media Player de Windows se invocan automáticamente en el explorador Web predeterminado si IWMPSettings. la propiedad **invokeURLs** está establecida en true. Puede usar IWMPSettings. propiedad **defaultFrame** para especificar el marco de destino en el que aparece la Página Web.

La dirección URL enviada a Windows Media Player se procesa con respecto a la dirección URL base especificada por IWMPSettings. propiedad **baseurl** . La dirección URL base se concatena con la dirección URL relativa, lo que da como resultado una dirección URL completa que se pasa como parámetro de comando por el evento **comando** .

El control de Windows Media Player siempre procesa los comandos de dirección URL de entrada de la siguiente manera:

1.  Se recibe un comando de tipo URL.
2.  IWMPSettings. **baseurl** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.
3.  Se llama a **comando** .
4.  Después de que **comando** devuelve, IWMPSettings. **invokeURLs** está activada.
5.  Si IWMPSettings. **invokeURLs** es true y el comando es un comando de dirección URL, se invoca la dirección URL especificada. Si IWMPSettings. **invokeURLs** es false o si el comando no es un comando de dirección URL, se omite el comando.

Al crear un archivo de Windows Media, puede especificar el marco en el que se muestra la nueva dirección URL mediante la concatenación de dos símbolos de y comercial y el nombre del marco en el campo de parámetro. En el ejemplo siguiente se muestran los parámetros de **comando** típicos. Especifica que se debe iniciar la dirección URL de la *Página* en *el marco frame.*


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



No se llama al evento comando si se está examinando el archivo (reenvío rápido o rebobinado).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. captioningId (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB y C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB y C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





