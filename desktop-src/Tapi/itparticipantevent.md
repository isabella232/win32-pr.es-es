---
description: La interfaz ITParticipantEvent contiene métodos que recuperan la descripción de los eventos de los participantes.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaz ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680320"
---
# <a name="itparticipantevent-interface"></a>Interfaz ITParticipantEvent

\[**ITParticipantEvent** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITParticipantEvent** contiene métodos que recuperan la descripción de los eventos de los participantes. Cuando la implementación de la aplicación del método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **te \_ Private**, el parámetro *pevent* del método es un puntero **IDispatch** para la interfaz **ITParticipantEvent** . Los métodos de esta interfaz se pueden usar para recuperar información relativa a un cambio de participante que se ha producido.

> [!Note]  
> Debe llamar al método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) y establecer una máscara de filtro de eventos que incluya el evento de usuario **\_ privado** para habilitar la recepción de eventos de participantes. Si no llama a **ITTAPI::p UT \_ EventFilter**, la aplicación no recibirá ningún evento. Para obtener más información, vea información general sobre [eventos](events.md) .

 

## <a name="members"></a>Miembros

La interfaz **ITParticipantEvent** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantEvent** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITParticipantEvent** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ evento**](itparticipantevent-get-event.md)             | Obtiene el descriptor de [**\_ eventos del participante**](participant-event.md) del evento.<br/>                                                    |
| [**obtener \_ participante**](itparticipantevent-get-participant.md) | Obtiene un puntero a una matriz de interfaces [**ITParticipant**](itparticipant.md) que representan los participantes implicados en el evento.<br/> |
| [**obtener \_ subflujo**](itparticipantevent-get-substream.md)     | Obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las subsecuencias implicadas en el evento.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**evento de participante \_**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Fragmento de código registrar eventos](register-events.md)
</dt> </dl>

 

