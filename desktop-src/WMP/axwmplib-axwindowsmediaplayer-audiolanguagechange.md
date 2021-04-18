---
title: Evento AudioLanguageChange del objeto AxWindowsMediaPlayer
description: El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual. | Evento AudioLanguageChange del objeto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698487"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Evento AudioLanguageChange del objeto AxWindowsMediaPlayer

El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad   | Descripción                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **ididioma** | **System. Int32** Identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.<br/> |



 

## <a name="remarks"></a>Observaciones

Un identificador de configuración regional (LCID) identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

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

[**IWMPControls3. currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





