---
description: Las constantes de marca de bits LINEDISCONNECTMODE \_ describen diferentes razones para una solicitud de desconexión remota. Un modo de desconexión está disponible como estado de llamada a la aplicación después de que el estado de la llamada pasa a desconectado.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: LINEDISCONNECTMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ad56f993d746e5d09e33e4dcfb74d29766dd359fa47302053e0af13513a7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060673"
---
# <a name="linedisconnectmode_-constants"></a>Constantes LINEDISCONNECTMODE \_

Las constantes de marca de bits **LINEDISCONNECTMODE \_** describen diferentes razones para una solicitud de desconexión remota. Un modo de desconexión está disponible como estado de llamada a la aplicación después de que el estado de la llamada pasa a desconectado.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



La dirección de destino no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ BLOQUEADO**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque las llamadas desde la dirección de origen no se aceptan en la dirección de destino. Esto difiere de LINEDISCONNECTMODE REJECT en que el bloqueo se implementa en la red (un rechazo pasivo) mientras se implementa un rechazo en el equipo de destino (un rechazo \_ activo). El bloqueo puede deberse a una exclusión específica de la dirección de origen o porque el destino acepta llamadas solo desde un conjunto seleccionado de direcciones de origen (grupo de usuarios cerrado). (TAPI versiones 2.0 y posteriores)

LINEDISCONNECTMODE \_ BLOCKED es adecuado como respuesta en la lista de bloqueos. Por ejemplo, un módem ha recibido una respuesta, ha pasado más de seis segundos sin detectar ringback, no ha podido conectar un número definido de veces, determina que el número de teléfono no es válido para llamar a y emite una respuesta "bloqueado".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ BUSY**
</dt> <dd> <dl> <dt>



La estación del usuario remoto está ocupada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ CANCELLED**
</dt> <dd> <dl> <dt>



Se canceló la llamada. (TAPI versiones 2.0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**CONGESTIÓN DE LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La red se ingiere.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque el destino ha invocado la característica No alterar. (TAPI versiones 2.0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ REENVIADO**
</dt> <dd> <dl> <dt>



El modificador reenvía la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INCOMPATIBLE**
</dt> <dd> <dl> <dt>



El equipo de la estación del usuario remoto no es compatible con el tipo de llamada solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOANSWER**
</dt> <dd> <dl> <dt>



La estación del usuario remoto no responde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



No se detectó un tono de marcado dentro de un tiempo de espera definido por el proveedor de servicios, en un punto durante la marcación cuando se esperaba uno (por ejemplo, en una "W" en la cadena que se puede marcar). Esto también puede ocurrir sin un período de tiempo de espera definido por el proveedor de servicios o sin un valor especificado en el **miembro dwWaitForDialTone** de la [**estructura LINEDIALPARAMS.**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) (TAPI versiones 1.4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Se trata de una solicitud de desconexión normal por parte de la parte remota. La llamada se finalizó con normalidad.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada porque se ha cambiado el número de destino, pero no se proporciona el redireccionamiento automático al nuevo número. (TAPI versiones 2.0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



No se pudo conectar la llamada o se desconectó porque el dispositivo de destino está fuera de servicio (error de hardware). (TAPI versiones 2.0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**RECOGIDA LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La llamada se ha seleccionado desde otro lugar.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



La llamada no se pudo conectar o se desconectó porque no se pudo obtener ni mantener la calidad mínima del servicio. Esto difiere de LINEDISCONNECTMODE INCOMPATIBLE en que la falta de \_ recursos puede ser una condición temporal en el destino. (TAPI versiones 2.0 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ REJECT**
</dt> <dd> <dl> <dt>



El usuario remoto ha rechazado la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



La llamada no se pudo conectar o se desconectó debido a un error temporal en la red. La llamada se puede volver a tentar más adelante y se espera que se complete finalmente. (TAPI versiones 2.0 y posteriores)

LINEDISCONNECTMODE \_ TEMPFAILURE es adecuado como respuesta retrasada. Por ejemplo, un módem que recibe una señal ocupada o un equivalente demasiadas veces en un período de tiempo determinado concluye que no se debe volver a llamar al número hasta que haya transcurrido un tiempo definido y emite una respuesta "retrasada".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



El motivo de la desconexión no está disponible y no se conocerá más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



El motivo de la solicitud de desconexión es desconocido, pero puede conocerse más adelante.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INACCESIBLE**
</dt> <dd> <dl> <dt>



No se pudo alcanzar al usuario remoto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden alto se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Una solicitud de desconexión remota para una llamada determinada da como resultado la transición del estado de llamada al estado desconectado y se envía un [**mensaje LINE \_ CALLSTATE**](line-callstate.md) a la aplicación. La información LINEDISCONNECTMODE \_ proporciona detalles sobre la solicitud de desconexión remota. Está disponible en la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) de la llamada cuando la llamada está en estado desconectado. Mientras una llamada está en este estado, la aplicación todavía puede consultar la información y el estado de la llamada. Por ejemplo, la información de usuario-usuario que se recibe como parte de la desconexión remota está disponible a continuación. La aplicación puede borrar una llamada desconectada quitando la llamada.

Por motivos de compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión negociada de la API en la línea y no usar este valor LINEDISCONNECTMODE si no se admite en la versión negociada (en su lugar se podría usar \_ LINEDISCONNECTMODE NORMAL o \_ \_ UNKNOWN).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**DELINEIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




