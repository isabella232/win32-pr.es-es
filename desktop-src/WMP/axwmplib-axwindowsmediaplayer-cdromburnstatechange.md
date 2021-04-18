---
title: Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer
description: El evento CdromBurnStateChange se produce cuando cambia el estado de una operación de grabación de CD.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698483"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnStateChange del objeto AxWindowsMediaPlayer

El evento CdromBurnStateChange se produce cuando cambia el estado de una operación de grabación de CD.

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

El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**. Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, que contiene las siguientes propiedades relacionadas con este evento.



| Propiedad   | Descripción                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromBurn | Interfaz WMPLib. IWMPCdromBurnThe que representa la operación de grabación que provocó el error.<br/> |
| wmpbs      | Valor de enumeración WMPLib. WMPBurnStateThe que indica el nuevo estado.<br/>                         |



 

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

[**Interfaz IWMPCdromBurn (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





