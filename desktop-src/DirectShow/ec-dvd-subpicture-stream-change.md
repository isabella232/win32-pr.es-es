---
description: Indica que el número de secuencia de la subimagen actual ha cambiado para el título principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679344"
---
# <a name="ec_dvd_subpicture_stream_change"></a>\_cambio de \_ secuencia de subimagen de DVD de \_ EC \_

Indica que el número de secuencia de la subimagen actual ha cambiado para el título principal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica el nuevo número de secuencia de la subimagen del usuario. Los números de secuencia de la subimagen oscilan entre 0 y 31. El flujo 0xFFFFFFFF indica que no hay ninguna secuencia seleccionada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor booleano que indica el estado de encendido o apagado de la subimagen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La subimagen puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).

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

 

 




