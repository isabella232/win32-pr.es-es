---
description: La interfaz ITParticipantEvent contiene métodos que recuperan la descripción de los eventos del participante.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaz ITParticipantEvent (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f47e57bf1698a97be6811316409e596c9dfb03181e50b5f487798463c5cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864465"
---
# <a name="itparticipantevent-interface"></a>Interfaz ITParticipantEvent

\[**ITParticipantEvent** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITParticipantEvent contiene** métodos que recuperan la descripción de los eventos del participante. Cuando la implementación de la aplicación del método [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un [**EVENTO \_ TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **TE \_ PRIVATE**, el parámetro *pEvent* del método es un puntero **IDispatch** para la **interfaz ITParticipantEvent.** Los métodos de esta interfaz se pueden usar para recuperar información relacionada con un cambio de participante que se ha producido.

> [!Note]  
> Debe llamar al método [**ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) y establecer una máscara de filtro de eventos que incluya el evento **TE \_ PRIVATE** para habilitar la recepción de eventos de participante. Si no llama a **ITTAPI::p ut \_ EventFilter**, la aplicación no recibirá ningún evento. Para obtener más información, consulte la información [general sobre](events.md) eventos.

 

## <a name="members"></a>Miembros

La **interfaz ITParticipantEvent** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantEvent** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITParticipantEvent** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ Event**](itparticipantevent-get-event.md)             | Obtiene el descriptor [**\_ PARTICIPANT EVENT**](participant-event.md) del evento.<br/>                                                    |
| [**obtener \_ participante**](itparticipantevent-get-participant.md) | Obtiene un puntero a una matriz de interfaces [**ITParticipant**](itparticipant.md) que representan a los participantes implicados en el evento.<br/> |
| [**get \_ SubStream**](itparticipantevent-get-substream.md)     | Obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las subrecciones implicadas en el evento.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**EVENTO \_ DE PARTICIPANTE**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**EVENTO \_ TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Fragmento de código de Registro de eventos](register-events.md)
</dt> </dl>

 

