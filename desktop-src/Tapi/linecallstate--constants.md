---
description: Las constantes de marca de bits LINECALLSTATE describen los estados de llamada en los que \_ puede estar una llamada.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: LINECALLSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb16daf5875db637a255b626a6f90303ed7c7af69566b0b7db71695af4bc8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140108"
---
# <a name="linecallstate_-constants"></a>Constantes \_ LINECALLSTATE

Las constantes de marca de bits **LINECALLSTATE \_** describen los estados de llamada en los que puede estar una llamada.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ ACEPTADO**
</dt> <dd> <dl> <dt>



La llamada estaba en estado de oferta y se ha aceptado. Esto indica a otras aplicaciones (de supervisión) que la aplicación propietaria actual ha reclamado la responsabilidad de responder a la llamada. En ISDN, el estado aceptado se introduce cuando el equipo llamado envía un mensaje al conmutador que indica que está dispuesto a presentar la llamada a la persona llamada. Esto tiene el efecto secundario de alertar (llamar) a los usuarios en ambos extremos de la llamada. Una llamada entrante siempre se puede responder inmediatamente sin que primero se acepte por separado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ BUSY**
</dt> <dd> <dl> <dt>



La llamada recibe un tono ocupado. Un tono ocupado indica que la llamada no se puede completar ya sea un circuito (tronco) o la estación de la entidad remota está en uso. Vea [**LINEBUSYMODE \_ Constants**](linebusymode--constants.md)( Constantes LINEBUSYMODE ).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ CONFERENCED**
</dt> <dd> <dl> <dt>



La llamada es miembro de una llamada de conferencia y está lógicamente en el estado conectado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ CONECTADO**
</dt> <dd> <dl> <dt>



Se ha establecido la llamada y se realiza la conexión. La información puede fluir a través de la llamada entre la dirección de origen y la dirección de destino.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE \_ DIALING**
</dt> <dd> <dl> <dt>



El originador marca dígitos en la llamada. El conmutador recopila los dígitos marcados. Tenga en cuenta [**que ni lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ni [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) colocarán la línea en el estado de marcado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ DIALTONE**
</dt> <dd> <dl> <dt>



La llamada recibe un tono de marcado del conmutador, lo que significa que el conmutador está listo para recibir un número marcado. Consulte [**CONSTANTIALTONEMODE \_ Constants (Constantes DELINEIALTONEMODE)**](linedialtonemode--constants.md) para obtener identificadores de los tonos de marcación especiales, como un tono de atonía del correo de voz normal.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ DISCONNECTED**
</dt> <dd> <dl> <dt>



La entidad remota se ha desconectado de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ IDLE**
</dt> <dd> <dl> <dt>



La llamada existe pero no se ha conectado. No existe ninguna actividad en la llamada, lo que significa que ninguna llamada está activa actualmente. Una llamada nunca puede salir del estado de inactividad.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**OFERTA \_ LINECALLSTATE**
</dt> <dd> <dl> <dt>



La llamada se ofrece a la estación, lo que indica la llegada de una nueva llamada. El estado de la oferta no es el mismo que el de hacer que un teléfono o equipo suene. En algunos entornos, una llamada en el estado de la oferta no llama al usuario hasta que el modificador indica a la línea que se llame. Un ejemplo de uso podría ser cuando aparece una llamada entrante en varios conjuntos de estaciones, pero solo los anillos de dirección principal. La instrucción de anillo no afecta a ningún estado de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONHOLD**
</dt> <dd> <dl> <dt>



El modificador mantiene la llamada. Esto libera la línea física, lo que permite que otra llamada use la línea.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**
</dt> <dd> <dl> <dt>



La llamada está actualmente en espera mientras se agrega a una conferencia.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**
</dt> <dd> <dl> <dt>



La llamada está actualmente en espera de transferirse a otro número.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ PROCEEDING**
</dt> <dd> <dl> <dt>



La marcación se ha completado y la llamada se está completando a través de la red de conmutador o teléfono. Esto ocurre después de que se complete la marcación y antes de que la llamada llegue a la entidad de acceso telefónico, como se indica mediante la llamada, ocupado o respuesta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE \_ RINGBACK**
</dt> <dd> <dl> <dt>



Se ha alcanzado la estación a la que se va a llamar y el conmutador del destino está generando un tono de anillo al originador. Un *anillo de* retorno significa que se está alertando a la dirección de destino de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**
</dt> <dd> <dl> <dt>



La llamada recibe una señal de información especial, que precede a un anuncio pregrabado que indica por qué no se puede completar una llamada. Vea [**LINESPECIALINFO \_ Constants**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



La llamada existe, pero su estado es desconocido actualmente. Esto puede ser el resultado de una detección de progreso de llamada deficiente por parte del proveedor de servicios. También se puede generar un mensaje de estado de llamada con el estado de llamada establecido en desconocido para informar al archivo DLL de TAPI sobre una nueva llamada en un momento en el que el estado real de la llamada no se conoce exactamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 8 bits de orden superior pueden definir un subestado específico del dispositivo de cualquiera de los estados predefinidos, siempre que también se establezca uno de los bits LINECALLSTATE \_ definidos anteriormente. Los 24 bits de orden inferior están reservados para estados predefinidos.

El mensaje LINE CALLSTATE enviado a la aplicación usa las constantes [**\_ LINECALLSTATE**](line-callstate.md) como parámetros. **\_** El mensaje lleva el nuevo estado de llamada al que la llamada ha pasado. Estas constantes también se usan como miembros en la [**estructura LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) devuelta por la [**función lineGetCallStatus.**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)

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

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

