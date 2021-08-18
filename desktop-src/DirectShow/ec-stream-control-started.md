---
description: Un comando stream-control start ha tenido efecto.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73af8d39c3dae0447600a23dcb00483f4e0da6b81bc7ba6ab4a7e8b5f7afa42d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997895"
---
# <a name="ec_stream_control_started"></a>EC \_ STREAM \_ CONTROL \_ STARTED

Un comando stream-control start ha tenido efecto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin que inició la secuencia.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido por el usuario.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Los filtros envían este evento en respuesta al [**método IAMStreamControl::StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) Este método especifica una hora de referencia para que un pin comience el streaming. Cuando se inicia el streaming, el filtro envía este evento.

El *parámetro pSender* especifica el pin que ejecuta el comando start. Dependiendo de la implementación, es posible que no sea el pin el que recibió la [**llamada StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

La aplicación especifica el parámetro *dwCookie* en el [**método StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) Este parámetro permite que la aplicación realice un seguimiento de varias llamadas al método .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




