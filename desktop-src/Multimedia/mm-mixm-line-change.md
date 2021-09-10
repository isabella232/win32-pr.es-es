---
title: MM_MIXM_LINE_CHANGE mensaje (Mmsystem.h)
description: Un dispositivo mezclador envía el mensaje MM MIXM LINE CHANGE para notificar a una aplicación que el estado de una línea de audio en \_ el dispositivo especificado ha \_ \_ cambiado. La aplicación debe actualizar su pantalla y los valores almacenados en caché para la línea de audio especificada.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371179"
---
# <a name="mm_mixm_line_change-message"></a>MENSAJE DE CAMBIO DE LÍNEA DE MM \_ MIXM \_ \_

Un dispositivo mezclador envía el mensaje **MM \_ MIXM \_ LINE \_ CHANGE** para notificar a una aplicación que el estado de una línea de audio en el dispositivo especificado ha cambiado. La aplicación debe actualizar su pantalla y los valores almacenados en caché para la línea de audio especificada.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador al dispositivo mezclador que envió el mensaje de notificación.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Identificador de línea de la línea de audio que ha cambiado de estado. Este identificador es el mismo que el **miembro dwLineID** de la estructura **MIXERLINE** devuelta por la **función mixerGetLineInfo.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una aplicación debe abrir un dispositivo mezclador y especificar una ventana de devolución de llamada para recibir el **mensaje MM \_ MIXM LINE \_ \_ CHANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mezcladores de audio](audio-mixers.md)
</dt> <dt>

[Mensajes de Mixer audio](audio-mixer-messages.md)
</dt> </dl>

 

 





