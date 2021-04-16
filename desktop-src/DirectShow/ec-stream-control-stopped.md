---
description: Un comando de detención del control de secuencias ha surtido efecto.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690284"
---
# <a name="ec_stream_control_stopped"></a>CONTROL de secuencia de EC \_ \_ \_ detenido

Un comando de detención del control de secuencias ha surtido efecto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN que detuvo la secuencia.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido por el usuario.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Los filtros envían este evento en respuesta al método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . El método **StopAt** especifica un tiempo de referencia para que un código PIN detenga el streaming. Cuando se detiene el streaming, el filtro envía este evento.

El parámetro *pSender* especifica el PIN que ejecuta el comando STOP. Dependiendo de la implementación, es posible que no sea el PIN que recibió la llamada [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

La aplicación especifica el parámetro *dwCookie* en el método [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Este parámetro permite que la aplicación realice el seguimiento de varias llamadas al método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




