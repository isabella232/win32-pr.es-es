---
description: Indica que el número de secuencia de audio actual cambió para el título principal del DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680855"
---
# <a name="ec_dvd_audio_stream_change"></a>\_cambio de \_ flujo de audio de DVD de EC \_ \_

Indica que el número de secuencia de audio actual cambió para el título principal del DVD.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica el nuevo número de secuencia de audio del usuario. Los números de secuencia de audio oscilan entre 0 y 7. El flujo 0xFFFFFFFF indica que no hay ninguna secuencia seleccionada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La secuencia de audio actual puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante la interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Este evento se desencadena en todos los dominios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




