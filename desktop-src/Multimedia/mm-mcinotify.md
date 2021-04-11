---
title: Mensaje de MM_MCINOTIFY (mmsystem. h)
description: El \_ mensaje mm MCINOTIFY notifica a una aplicación que un dispositivo MCI ha completado una operación. Los dispositivos MCI envían este mensaje solo cuando \_ se usa la marca de notificación de MCI.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Mensaje de MM_MCINOTIFY de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150629"
---
# <a name="mm_mcinotify-message"></a>\_Mensaje MCINOTIFY mm

El mensaje **mm \_ MCINOTIFY** notifica a una aplicación que un dispositivo MCI ha completado una operación. Los dispositivos MCI envían este mensaje solo cuando \_ se usa la marca de notificación de MCI.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Motivo de la notificación. Se definen los valores siguientes:



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| la notificación de MCI se \_ \_ anuló    | El dispositivo recibió un comando que impidió que se cumplieran las condiciones actuales para iniciar la función de devolución de llamada. Si un comando nuevo interrumpe el comando actual y también solicita la notificación, el dispositivo solo envía este mensaje y no \_ la notificación de MCI. \_ |
| \_error de notificación de MCI \_    | Se produjo un error de dispositivo mientras el dispositivo estaba ejecutando el comando.                                                                                                                                                                                                            |
| la notificación de MCI se \_ \_ realizó correctamente | Se han cumplido las condiciones que inician la función de devolución de llamada.                                                                                                                                                                                                                 |
| notificación de MCI \_ \_ sustituida | El dispositivo ha recibido otro comando con el indicador "Notify" establecido y se han reemplazado las condiciones actuales para iniciar la función de devolución de llamada.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificador del dispositivo que inicia la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de la marca de notificación de MCI \_ , vea [la marca de notificación](the-notify-flag.md).

Un dispositivo devuelve la \_ marca MCI Notify \_ Successful with **mm \_ MCINOTIFY** cuando finaliza la acción de un comando. Por ejemplo, un dispositivo de audio de CD usa esta marca para la notificación del comando [**Play**](play.md) ( [**MCI \_ Play**](mci-play.md)) cuando el dispositivo finaliza la reproducción. El comando **Play** solo se ejecuta correctamente cuando llega a la posición final especificada o alcanza el final del medio. Del mismo modo, los comandos [**Buscar**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) y [**registro**](record.md) ( [**\_ registro de MCI**](mci-record.md)) no devuelven la \_ notificación de MCI \_ correctamente hasta que llegan a la posición final especificada o alcanzan el final del medio.

Un dispositivo devuelve la \_ marca MCI Notify \_ Aborted con **mm \_ MCINOTIFY** solo cuando recibe un comando que le impide cumplir las condiciones de notificación. Por ejemplo, el comando [**Play**](play.md) no anulará la notificación de un comando **Play** anterior siempre que el comando nuevo no cambie la dirección de reproducción ni cambie la posición final. Los comandos de [**búsqueda**](seek.md) y [**registro**](record.md) se comportan de forma similar. MCI tampoco envía una notificación de \_ MCI \_ anulada cuando la reproducción o grabación se detiene con el comando [**pausar**](pause.md) ( [**MCI \_ PAUSE**](mci-pause.md)). El envío del comando de [**reanudación**](resume.md) ( [**\_ reanudación de MCI**](mci-resume.md)) permite que sigan cumpliendo las condiciones de devolución de llamada.

Cuando la aplicación solicite una notificación para un comando, compruebe el error devuelto por las funciones [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Si estas funciones encuentran un error y devuelven un valor distinto de cero, MCI no establecerá la notificación para el comando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensajes de MCI](mci-messages.md)
</dt> <dt>

[**temporalmente**](pause.md)
</dt> <dt>

[**reproducción**](play.md)
</dt> <dt>

[**registro**](record.md)
</dt> <dt>

[**Recuper**](resume.md)
</dt> <dt>

[**desean**](seek.md)
</dt> </dl>

 

