---
title: Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer
description: El evento CurrentMediaItemAvailable tiene lugar cuando está disponible un elemento de metadatos gráfico en el elemento multimedia actual. | Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5bbac6f27dfa7c9de1115eb3c2f5eea85096e0868ac17e0f8b11d81385f344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582354"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentMediaItemAvailable del objeto AxWindowsMediaPlayer

El evento CurrentMediaItemAvailable tiene lugar cuando está disponible un elemento de metadatos gráfico en el elemento multimedia actual.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad     | Descripción                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System.StringEl nombre del elemento multimedia actual.<br/> |



 

## <a name="remarks"></a>Comentarios

Dado que la reproducción puede comenzar antes de que un elemento multimedia se descargue por completo, es posible que los gráficos de metadatos contenidos en el elemento multimedia (por ejemplo, la portada del álbum) no estén disponibles cuando empiece a reproducirse. Este evento le avisa cuando finaliza la descarga de un elemento gráfico de metadatos. A continuación, puede recuperar **la interfaz IWMPMedia** pasando el valor **de bstrItemName** a *IWMPMediaCollection*. **Método getByName,** después del cual puede acceder al elemento gráfico de metadatos mediante *IWMPMedia3*. **getItemInfoByType y** especifica **WM/Picture** para el nombre del atributo.

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getByName (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





