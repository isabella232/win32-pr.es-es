---
title: Evento DomainChange del objeto AxWindowsMediaPlayer
description: El evento DomainChange tiene lugar cuando cambia el dominio de DVD. | Evento DomainChange del objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37f10679225fb893fad8bcf6fc6687021256e305e8c5a08e6ebe96d16b74e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136128"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange del objeto AxWindowsMediaPlayer

El evento DomainChange tiene lugar cuando cambia el dominio de DVD.

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad  | Descripción                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | System.StringIndica el nuevo dominio. Para los valores posibles, vea la sección Comentarios.<br/> |



 

## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestran los valores posibles para la propiedad strDomain.



| String            | Descripción                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Realizar la inicialización predeterminada de un disco de DVD.                     |
| videoManagerMenu  | Mostrar menús para todo el disco. También se conoce como menú raíz o topMenu. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu.     |
| title             | Mostrar el título actual.                                        |
| stop              | El navegador de DVD está en el dominio DE DEtenerse de DVD.                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





