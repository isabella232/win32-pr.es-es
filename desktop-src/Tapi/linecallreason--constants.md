---
description: Las constantes de marca de bits LINECALLREASON \_ describen el motivo de una llamada.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: LINECALLREASON_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9aa59b2589bc3c737da2feb76b6caeb97905af6871c770d653a2b18f1377b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866945"
---
# <a name="linecallreason_-constants"></a>Constantes LINECALLREASON \_

Las constantes de marca de bits **LINECALLREASON \_** describen el motivo de una llamada.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**
</dt> <dd> <dl> <dt>



La llamada fue el resultado de una solicitud de finalización de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**\_LINECALLREASONCAMPEDON**
</dt> <dd> <dl> <dt>



La llamada se ha acampado en la dirección. Normalmente, aparece inicialmente en el estado onhold y se puede cambiar a mediante [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Si una llamada activa se vuelve inactiva, la llamada de acampada puede cambiar al estado de la oferta y el dispositivo empieza a llamar.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ DIRECT**
</dt> <dd> <dl> <dt>



Se trata de una llamada entrante o saliente directa.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**
</dt> <dd> <dl> <dt>



Esta llamada se reenvía desde otra extensión que estaba ocupada en el momento de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**
</dt> <dd> <dl> <dt>



La llamada se reenvía desde otra extensión que no respondió a la llamada después de un número de anillos.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**
</dt> <dd> <dl> <dt>



La llamada se reenvía incondicionalmente desde otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ INTRUDE**
</dt> <dd> <dl> <dt>



La llamada se intruyó en la línea, ya sea mediante una acción de finalización de llamada invocada por otra estación o por la acción del operador. En función de la implementación del conmutador, la llamada puede aparecer en el estado conectado o con una llamada activa existente en la línea.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ ESTACIONADO**
</dt> <dd> <dl> <dt>



La llamada estaba estacionada en la dirección. Normalmente, aparece inicialmente en el estado onhold.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON \_ PICKUP**
</dt> <dd> <dl> <dt>



La llamada se ha seleccionado de otra extensión.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**REDIRECCIONAMIENTO DE LINECALLREASON \_**
</dt> <dd> <dl> <dt>



La llamada se redirija a esta estación.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON \_ REMINDER**
</dt> <dd> <dl> <dt>



La llamada es un recordatorio (o "recuperación") de que el usuario tiene una llamada estacionada o en espera durante (potencialmente) mucho tiempo.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**
</dt> <dd> <dl> <dt>



La llamada aparece en la dirección porque el modificador necesita instrucciones de enrutamiento de la aplicación. La aplicación debe examinar el **miembro CalledID** en [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)y usar la función [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) para proporcionar una nueva dirección que se puede marcar para la llamada. Si la llamada se va a bloquear en su lugar, la aplicación puede llamar a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Si la aplicación no puede tomar medidas dentro de un período de tiempo de espera definido por el conmutador, se realizará una acción predeterminada. Un proveedor de servicios solo puede usar esta constante si la versión negociada en la línea es 2.0 o superior. De lo contrario, el proveedor de servicios debe sustituir LINECALLREASON \_ UNAVAIL.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON \_ TRANSFER**
</dt> <dd> <dl> <dt>



La llamada se ha transferido desde otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON \_ UNAVAIL**
</dt> <dd> <dl> <dt>



El motivo de la llamada no está disponible y no se conocerá más adelante.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ UNKNOWN**
</dt> <dd> <dl> <dt>



El motivo de la llamada es desconocido actualmente, pero puede que se conozca más adelante.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON \_ UNPARK**
</dt> <dd> <dl> <dt>



La llamada se recuperó como una llamada aparcado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Las constantes LINECALLREASON \_ se usan en el miembro **dwReason** de la estructura de datos [**LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



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

 

 




