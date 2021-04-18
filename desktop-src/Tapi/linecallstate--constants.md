---
description: Las \_ constantes de marcador de bits LINECALLSTATE describen los Estados de llamada en los que puede estar una llamada.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes de LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680362"
---
# <a name="linecallstate_-constants"></a>Constantes de LINECALLSTATE \_

Las constantes de marcador de bits **LINECALLSTATE \_** describen los Estados de llamada en los que puede estar una llamada.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ aceptado**
</dt> <dd> <dl> <dt>



La llamada se encontraba en el estado de la oferta y se aceptó. Esto indica a otras aplicaciones (de supervisión) que la aplicación propietaria actual ha reclamado la responsabilidad de responder a la llamada. En ISDN, el estado aceptado se especifica cuando el equipo de la entidad que llama envía un mensaje al conmutador que indica que está dispuesto a presentar la llamada a la persona llamada. Esto tiene el efecto secundario de las alertas (timbres) de los usuarios en ambos extremos de la llamada. Una llamada entrante siempre se puede responder inmediatamente sin aceptarse primero por separado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ ocupado**
</dt> <dd> <dl> <dt>



La llamada recibe un tono ocupado. Un tono ocupado indica que la llamada no se puede completar porque un circuito (tronco) o la estación de la entidad remota están en uso. Vea [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ Conference**
</dt> <dd> <dl> <dt>



La llamada es un miembro de una llamada de conferencia y está lógicamente en estado conectado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ conectado**
</dt> <dd> <dl> <dt>



Se ha establecido la llamada y se ha realizado la conexión. La información puede fluir a través de la llamada entre la dirección de origen y la dirección de destino.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_marcado LINECALLSTATE**
</dt> <dd> <dl> <dt>



El originador está marcando dígitos en la llamada. El modificador recopila los dígitos marcados. Tenga en cuenta que ni [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ni [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) colocarán la línea en el estado de marcado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ DItono**
</dt> <dd> <dl> <dt>



La llamada está recibiendo un tono de marcado del conmutador, lo que significa que el conmutador está listo para recibir un número marcado. Vea [**\_ constantes de LINEDIALTONEMODE**](linedialtonemode--constants.md) para identificadores de tonos de marcado especiales, como un tono de intermitencia del correo de voz normal.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ DESconectado**
</dt> <dd> <dl> <dt>



La parte remota se ha desconectado de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inactivo**
</dt> <dd> <dl> <dt>



La llamada existe pero no se ha conectado. No existe ninguna actividad en la llamada, lo que significa que no hay ninguna llamada actualmente activa. Una llamada nunca puede salir del estado de inactividad.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**oferta de LINECALLSTATE \_**
</dt> <dd> <dl> <dt>



La llamada se ofrece a la estación, señalando la llegada de una nueva llamada. El estado de la oferta no es el mismo que ocasionar que un teléfono o equipo suene. En algunos entornos, una llamada en el estado de la oferta no hace sonar al usuario hasta que el modificador indica a la línea que se ponga en anillo. Un uso de ejemplo podría ser el lugar en el que aparece una llamada entrante en varios conjuntos de estaciones, pero solo los anillos de la dirección principal. La instrucción para el anillo no afecta a ningún estado de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE en \_ suspensión**
</dt> <dd> <dl> <dt>



La llamada está en espera por el modificador. Esto libera la línea física, lo que permite que otra llamada use la línea.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**
</dt> <dd> <dl> <dt>



La llamada está actualmente en espera mientras se agrega a una conferencia.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**
</dt> <dd> <dl> <dt>



La llamada está en espera en el momento de la transferencia a otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ continuar**
</dt> <dd> <dl> <dt>



El marcado se ha completado y la llamada se realiza a través del conmutador o la red telefónica. Esto se produce después de que el marcado finalice y antes de que la llamada llegue a la entidad marcada, como se indica por timbre, ocupado o respuesta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**\_timbre LINECALLSTATE**
</dt> <dd> <dl> <dt>



Se ha alcanzado la estación a la que se va a llamar y el conmutador del destino está generando un tono de timbre de vuelta al originador. Un *timbre* significa que la dirección de destino se alerta a la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**
</dt> <dd> <dl> <dt>



La llamada recibe una señal de información especial, que precede a un anuncio pregrabado que indica por qué no se puede completar una llamada. Vea [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ desconocido**
</dt> <dd> <dl> <dt>



La llamada existe, pero su estado es desconocido actualmente. Este puede ser el resultado de una detección deficiente del progreso de la llamada por parte del proveedor de servicios. También se puede generar un mensaje de estado de llamada con el estado de llamada establecido en Unknown para informar a la DLL de TAPI sobre una nueva llamada a la vez cuando no se conoce el estado de llamada real de la llamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 8 bits de orden superior pueden definir un subestado específico del dispositivo de cualquiera de los Estados predefinidos, siempre que \_ se establezca también uno de los bits LINECALLSTATE definidos anteriormente. Los 24 bits de orden inferior están reservados para los Estados predefinidos.

El mensaje de [**línea \_ CALLSTATE**](line-callstate.md) que se envía a la aplicación usa las **\_ constantes LINECALLSTATE** como parámetros. El mensaje lleva el nuevo estado de la llamada al que la llamada ha pasado. Estas constantes también se usan como miembros en la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) devuelta por la función [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .

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

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

