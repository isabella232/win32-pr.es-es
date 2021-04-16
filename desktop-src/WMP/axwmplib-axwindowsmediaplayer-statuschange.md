---
title: Evento StatusChange del objeto AxWindowsMediaPlayer
description: El evento StatusChange se produce cuando cambia el valor de la propiedad status. | Evento StatusChange del objeto AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Evento StatusChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699702"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a>Evento StatusChange del objeto AxWindowsMediaPlayer

El evento **StatusChange** se produce cuando cambia el valor de la propiedad **status** .

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a>Datos del evento

Este evento no contiene datos.

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

[**AxWindowsMediaPlayer. status (VB y C#)**](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





