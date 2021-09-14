---
title: Evento FolderScanStateChange del objeto AxWindowsMediaPlayer
description: El evento FolderScanStateChange tiene lugar cuando una operación de supervisión de carpetas cambia de estado.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242001"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento FolderScanStateChange del objeto AxWindowsMediaPlayer

El evento FolderScanStateChange tiene lugar cuando una operación de supervisión de carpetas cambia de estado.

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ Carpeta \_ WMPOCXEventsScanStateChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.



| Propiedad | Descripción                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| wmpfss   | WMPLib.WMPFolderScanStateEl valor de enumeración que indica el nuevo estado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                         |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**WMPFolderScanState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





