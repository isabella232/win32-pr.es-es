---
description: Un comando de inicio de control de secuencia ha surtido efecto.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653454"
---
# <a name="ec_stream_control_started"></a>CONTROL de secuencia de EC \_ \_ \_ iniciado

Un comando de inicio de control de secuencia ha surtido efecto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN que inició la secuencia.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valor definido por el usuario.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

Los filtros envían este evento en respuesta al método [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Este método especifica un tiempo de referencia para que un código PIN empiece el streaming. Cuando se inicia la transmisión por secuencias, el filtro envía este evento.

El parámetro *pSender* especifica el PIN que ejecuta el comando START. Dependiendo de la implementación, es posible que no sea el PIN que recibió la llamada [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

La aplicación especifica el parámetro *dwCookie* en el método [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Este parámetro permite que la aplicación realice el seguimiento de varias llamadas al método.

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

 

 




