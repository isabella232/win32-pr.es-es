---
description: Se ha realizado un comando stream-control stop.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928425"
---
# <a name="ec_stream_control_stopped"></a>EC \_ STREAM \_ CONTROL \_ STOPPED

Se ha realizado un comando stream-control stop.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin que detuvo la secuencia.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido por el usuario.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

Los filtros envían este evento en respuesta al [**método IAMStreamControl::StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) El **método StopAt** especifica un tiempo de referencia para que un pin detenga el streaming. Cuando el streaming se detiene, el filtro envía este evento.

El *parámetro pSender* especifica el pin que ejecuta el comando stop. Dependiendo de la implementación, es posible que no sea el pin el que recibió la [**llamada StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)

La aplicación especifica el parámetro *dwCookie* en el [**método StopAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) Este parámetro permite que la aplicación realice un seguimiento de varias llamadas al método .

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

 

 




