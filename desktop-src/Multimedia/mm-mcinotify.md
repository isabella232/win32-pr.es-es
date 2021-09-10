---
title: MM_MCINOTIFY mensaje (Mmsystem.h)
description: El mensaje MM \_ MCIDETIFY notifica a una aplicación que un dispositivo MCI ha completado una operación. Los dispositivos MCI envían este mensaje solo cuando se usa la \_ marca MCI NOTIFY.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369864"
---
# <a name="mm_mcinotify-message"></a>Mensaje \_ MM MTIFTIFY

El **mensaje MM \_ MCIDETIFY** notifica a una aplicación que un dispositivo MCI ha completado una operación. Los dispositivos MCI envían este mensaje solo cuando se usa la \_ marca MCI NOTIFY.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Motivo de la notificación. Se definen los siguientes valores:



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI \_ NOTIFY \_ ABORTED    | El dispositivo recibió un comando que impedía que se cumpliesan las condiciones actuales para iniciar la función de devolución de llamada. Si un nuevo comando interrumpe el comando actual y también solicita una notificación, el dispositivo solo envía este mensaje y no MCI \_ NOTIFY \_ SUPERSEDED |
| ERROR DE NOTIFICACIÓN DE MCI \_ \_    | Se produjo un error de dispositivo mientras el dispositivo estaba ejecutando el comando.                                                                                                                                                                                                            |
| NOTIFICACIÓN CORRECTA DE MCI \_ \_ | Se han cumplido las condiciones que inician la función de devolución de llamada.                                                                                                                                                                                                                 |
| MCI \_ NOTIFY \_ SUSTITUIDO | El dispositivo recibió otro comando con la marca "notify" establecida y se han reemplazado las condiciones actuales para iniciar la función de devolución de llamada.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificador del dispositivo que inicia la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre la marca MCI \_ NOTIFY, vea [La marca de notificación](the-notify-flag.md).

Un dispositivo devuelve la marca MCI \_ NOTIFY SUCCESSFUL con MM \_ **\_ MCIDETIFY** cuando finaliza la acción de un comando. Por ejemplo, un dispositivo de audio de CD usa esta marca para la notificación del comando [**play**](play.md) [**(MCI \_ PLAY)**](mci-play.md)cuando el dispositivo termina de reproducirse. El **comando de** reproducción solo se realiza correctamente cuando alcanza la posición final especificada o llega al final del medio. De forma similar, los comandos [**seek**](seek.md) ( [**MCI \_ SEEK**](mci-seek.md)) y [**record**](record.md) ( [**MCI \_ RECORD**](mci-record.md)) no devuelven MCI NOTIFY SUCCESSFUL hasta que llegan a la posición final especificada o llegan al final del \_ \_ medio.

Un dispositivo devuelve la marca MCI NOTIFY ABORTED con \_ \_ MM **\_ MTIFTIFY** solo cuando recibe un comando que impide que se cumplen las condiciones de notificación. Por ejemplo, el [**comando play**](play.md) no  anularía la notificación de un comando de reproducción anterior siempre que el nuevo comando no cambie la dirección de reproducción ni cambie la posición final. Los [**comandos de**](seek.md) búsqueda [**y**](record.md) registro se comportan de forma similar. MCI tampoco envía MCI NOTIFY ABORTED cuando se pausa la reproducción o la grabación con el comando \_ \_ [**pause**](pause.md) ( [**MCI \_ PAUSE**](mci-pause.md)). El envío [**del comando resume**](resume.md) [**(MCI \_ RESUME)**](mci-resume.md)les permite seguir cumple las condiciones de devolución de llamada.

Cuando la aplicación solicite la notificación de un comando, compruebe la devolución de errores de las funciones [**mciSendString**](/previous-versions//dd757161(v=vs.85)) [**o mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Si estas funciones encuentran un error y devuelven un valor distinto de cero, MCI no establecerá la notificación para el comando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensajes de MCI](mci-messages.md)
</dt> <dt>

[**Pausa**](pause.md)
</dt> <dt>

[**Jugar**](play.md)
</dt> <dt>

[**grabar**](record.md)
</dt> <dt>

[**Reanudar**](resume.md)
</dt> <dt>

[**Buscar**](seek.md)
</dt> </dl>

 

