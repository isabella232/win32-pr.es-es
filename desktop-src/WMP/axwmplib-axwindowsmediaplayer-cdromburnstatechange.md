---
title: Evento CdromChangeStateChange del objeto AxWindowsMediaPlayer
description: El evento CdromStateChange tiene lugar cuando una operación de grabación de CD cambia de estado.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromChangeStateChange del objeto AxWindowsMediaPlayer Reproductor de Windows Media
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476270"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromChangeStateChange del objeto AxWindowsMediaPlayer

El evento CdromStateChange tiene lugar cuando una operación de grabación de CD cambia de estado.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Datos del evento

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromChangeStateChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromChangeStateChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad.   | Descripción                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromRom (pCdrom ) | WMPLib.IWMPCdromRomThe interfaz que representa la operación de grabación que produjo el error.<br/> |
| wmpbs      | WMPLib.WMPStateEl valor de enumeración que indica el nuevo estado.<br/>                         |



 

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

[**Interfaz IWMPCdromRomRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





