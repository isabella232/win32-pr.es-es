---
description: Las \_ constantes de marcador de bits LINEDISCONNECTMODE describen diferentes razones para una solicitud de desconexión remota. Un modo de desconexión está disponible como estado de la llamada a la aplicación después de que el estado de la llamada pase a desconectado.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes de LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690804"
---
# <a name="linedisconnectmode_-constants"></a>Constantes de LINEDISCONNECTMODE \_

Las constantes de marcador de bits **LINEDISCONNECTMODE \_** describen diferentes razones para una solicitud de desconexión remota. Un modo de desconexión está disponible como estado de la llamada a la aplicación después de que el estado de la llamada pase a desconectado.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



La dirección de destino no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqueado**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque no se aceptan llamadas de la dirección de origen en la dirección de destino. Esto difiere del rechazo de LINEDISCONNECTMODE \_ en que el bloqueo se implementa en la red (un rechazo pasivo) mientras se implementa un rechazo en el equipo de destino (un rechazo activo). El bloqueo puede deberse a una exclusión específica de la dirección de origen o a que el destino acepta llamadas solo de un conjunto seleccionado de dirección de origen (grupo de usuarios cerrado). (Versiones de TAPI 2,0 y posteriores)

LINEDISCONNECTMODE \_ blocked es adecuado como respuesta bloqueo. Por ejemplo, un módem ha recibido una respuesta, ha pasado más de seis segundos sin detectar un timbre, no pudo conectarse un número definido de veces, determina que el número de teléfono no es válido para llamar a y emite una respuesta "bloqueo".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ ocupado**
</dt> <dd> <dl> <dt>



La estación del usuario remoto está ocupada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ cancelado**
</dt> <dd> <dl> <dt>



Se canceló la llamada. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestión de LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La red está congestionada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque el destino ha invocado la característica no molestar. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ reenviado**
</dt> <dd> <dl> <dt>



El modificador reenvió la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatible**
</dt> <dd> <dl> <dt>



El equipo de estación del usuario remoto no es compatible con el tipo de llamada solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**
</dt> <dd> <dl> <dt>



La estación del usuario remoto no responde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



No se detectó un tono de marcado dentro de un tiempo de espera definido por el proveedor de servicios, en un momento del marcado cuando se esperaba uno (por ejemplo, en una "W" en la cadena de marcado). Esto también puede producirse sin un período de tiempo de espera definido por el proveedor del servicio o sin un valor especificado en el miembro **dwWaitForDialTone** de la estructura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) . (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**
</dt> <dd> <dl> <dt>



Esta es una solicitud de desconexión normal de la parte remota. La llamada finalizó con normalidad.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque se ha cambiado el número de destino, pero no se ha proporcionado la redirección automática al nuevo número. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



La llamada no se pudo conectar o se desconectó porque el dispositivo de destino no está en el orden (error de hardware). (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**recogida de LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La llamada se tomó desde cualquier lugar.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



La llamada no se pudo conectar o se desconectó porque no se pudo obtener o mantener la calidad de servicio mínima. Esto difiere de LINEDISCONNECTMODE \_ incompatible en que la falta de recursos puede ser una condición temporal en el destino. (Versiones de TAPI 2,0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rechazo**
</dt> <dd> <dl> <dt>



El usuario remoto ha rechazado la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



La llamada no se pudo conectar o se desconectó debido a un error temporal en la red. la llamada se puede volver a intentar más tarde y se espera que finalice finalmente. (Versiones de TAPI 2,0 y posteriores)

LINEDISCONNECTMODE \_ TEMPFAILURE es adecuado como respuesta diferida. Por ejemplo, un módem que obtiene una señal de ocupado o que es equivalente demasiadas veces en un período de tiempo determinado concluye que el número no se debe volver a llamar hasta que haya transcurrido un tiempo definido y emita una respuesta ' retrasada '.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE no \_ disponible**
</dt> <dd> <dl> <dt>



La razón de la desconexión no está disponible y no se volverá a conocer más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ desconocido**
</dt> <dd> <dl> <dt>



El motivo de la solicitud de desconexión es desconocido, pero puede ser conocido más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INaccesible**
</dt> <dd> <dl> <dt>



No se pudo establecer contacto con el usuario remoto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Una solicitud de desconexión remota para una llamada determinada provoca el cambio de estado de la llamada al estado desconectado y se envía un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) a la aplicación. La información de LINEDISCONNECTMODE \_ proporciona detalles sobre la solicitud de desconexión remota. Está disponible en la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) de la llamada cuando la llamada está en el estado disconnected. Mientras una llamada se encuentra en este estado, la aplicación sigue teniendo permiso para consultar la información y el estado de la llamada. Por ejemplo, la información de usuario que se recibe como parte de la desconexión remota está disponible. La aplicación puede borrar una llamada desconectada quitando la llamada.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar este \_ valor de LINEDISCONNECTMODE si no se admite en la versión negociada ( \_ \_ se podría usar LINEDISCONNECTMODE normal o Unknown en su lugar).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




