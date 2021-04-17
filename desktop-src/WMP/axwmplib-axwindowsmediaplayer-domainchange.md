---
title: Evento DomainChange del objeto AxWindowsMediaPlayer
description: El evento DomainChange se produce cuando cambia el dominio del DVD. | Evento DomainChange del objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700060"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DomainChange del objeto AxWindowsMediaPlayer

El evento DomainChange se produce cuando cambia el dominio del DVD.

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
| strDomain | System. StringIndicates el nuevo dominio. Para los valores posibles, vea la sección Comentarios.<br/> |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran los posibles valores para la propiedad strDomain.



| String            | Descripción                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | Realizar la inicialización predeterminada de un disco DVD.                     |
| videoManagerMenu  | Mostrando menús para todo el disco. También se conoce como menú o menú raíz. |
| videoTitleSetMenu | Mostrar menús para el conjunto de títulos actual. También se conoce como titleMenu.     |
| title             | Mostrar el título actual.                                        |
| stop              | El navegador de DVD está en el dominio de detención de DVD.                         |



 

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

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





