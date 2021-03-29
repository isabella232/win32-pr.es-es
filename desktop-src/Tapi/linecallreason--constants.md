---
description: Las \_ constantes de marcador de bits LINECALLREASON describen el motivo de una llamada.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes de LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678989"
---
# <a name="linecallreason_-constants"></a>Constantes de LINECALLREASON \_

Las constantes de marcador de bits **LINECALLREASON \_** describen el motivo de una llamada.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**
</dt> <dd> <dl> <dt>



La llamada fue el resultado de una solicitud de finalización de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**
</dt> <dd> <dl> <dt>



La llamada se realizó en la dirección. Normalmente, aparece inicialmente en estado de suspensión y se puede cambiar a mediante [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Si una llamada activa se vuelve inactiva, la llamada de acampada puede cambiar al estado de la oferta y el dispositivo comienza a sonar.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ directo**
</dt> <dd> <dl> <dt>



Se trata de una llamada directa entrante o saliente.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**
</dt> <dd> <dl> <dt>



Esta llamada se reenvió desde otra extensión que estaba ocupada en el momento de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**
</dt> <dd> <dl> <dt>



La llamada se reenvió desde otra extensión que no ha respondido a la llamada después de un número de anillos.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**
</dt> <dd> <dl> <dt>



La llamada se reenvió incondicionalmente desde otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrusión**
</dt> <dd> <dl> <dt>



La llamada se ha desatacado en la línea, ya sea mediante una acción de finalización de llamada invocada por otra estación o por una acción del operador. Dependiendo de la implementación del conmutador, la llamada puede aparecer en el estado conectado o en la Conferencia con una llamada activa existente en la línea.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ estacionado**
</dt> <dd> <dl> <dt>



La llamada se ha detenido en la dirección. Normalmente, aparece inicialmente en estado de suspensión.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**recogida de LINECALLREASON \_**
</dt> <dd> <dl> <dt>



La llamada se tomó de otra extensión.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**redirección de LINECALLREASON \_**
</dt> <dd> <dl> <dt>



La llamada se redirigió a esta estación.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON \_ recordatorio**
</dt> <dd> <dl> <dt>



La llamada es un recordatorio (o "retirada") de que el usuario tiene una llamada detenida o en espera durante un tiempo prolongado.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**
</dt> <dd> <dl> <dt>



La llamada aparece en la dirección porque el conmutador necesita instrucciones de enrutamiento de la aplicación. La aplicación debe examinar el miembro **CalledID** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)y usar la función [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) para proporcionar una nueva dirección de marcado para la llamada. Si se va a bloquear la llamada en su lugar, la aplicación puede llamar a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Si la aplicación no puede realizar una acción dentro de un período de tiempo de espera definido por el conmutador, se realizará una acción predeterminada. Un proveedor de servicios puede utilizar esta constante solo si la versión negociada en la línea es 2,0 o superior. En caso contrario, el proveedor de servicios debe sustituir LINECALLREASON no \_ disponible.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**transferencia de LINECALLREASON \_**
</dt> <dd> <dl> <dt>



La llamada se ha transferido desde otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON no \_ disponible**
</dt> <dd> <dl> <dt>



La razón de la llamada no está disponible y no se volverá a conocer más adelante.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ desconocido**
</dt> <dd> <dl> <dt>



Actualmente, el motivo de la llamada es desconocido, pero puede ser conocido más adelante.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**Desactivación \_ de LINECALLREASON**
</dt> <dd> <dl> <dt>



La llamada se recuperó como una llamada estacionada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Las \_ constantes LINECALLREASON se usan en el miembro **dwReason** de la estructura de datos [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




