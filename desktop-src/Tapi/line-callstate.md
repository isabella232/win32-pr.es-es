---
description: El \_ mensaje de línea de CALLSTATE TAPI se envía cuando cambia el estado de la llamada especificada.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Mensaje de LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679491"
---
# <a name="line_callstate-message"></a>Mensaje de línea \_ CALLSTATE

El mensaje de **línea de \_ CALLSTATE** TAPI se envía cuando cambia el estado de la llamada especificada. Normalmente, se reciben varios mensajes de este tipo durante la duración de una llamada. Se notifica a las aplicaciones las nuevas llamadas entrantes con este mensaje; la nueva llamada está en el estado de la *oferta* . La aplicación puede utilizar [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) para recuperar información más detallada sobre el estado actual de la llamada.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la llamada.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Nuevo estado de la llamada. Este parámetro debe ser una y solo una de las siguientes [**\_ constantes LINECALLSTATE**](linecallstate--constants.md).



| dwParam1                                                                                                                                                                                             | Significado                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ ocupado**</dt> </dl>                         | *dwParam2* contiene detalles sobre el modo ocupado. Este parámetro utiliza una de las [**\_ constantes de LINEBUSYMODE**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ conectado**</dt> </dl>          | *dwParam2* contiene detalles sobre el modo conectado. Este parámetro utiliza una de las [**\_ constantes de LINECONNECTEDMODE**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ DItono**</dt> </dl>             | *dwParam2* contiene detalles sobre el modo de tono de marcado. Este parámetro utiliza una de las [**\_ constantes de LINEDIALTONEMODE**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**oferta de LINECALLSTATE \_**</dt> </dl>             | *dwParam2* contiene detalles sobre el modo conectado. Este parámetro utiliza una de las [**\_ constantes de LINEOFFERINGMODE**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* contiene los detalles sobre el modo de información especial. Este parámetro utiliza una de las [**\_ constantes de LINESPECIALINFO**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ DESconectado**</dt> </dl> | *dwParam2* contiene detalles sobre el modo de desconexión. Este parámetro utiliza una de las [**\_ constantes de LINEDISCONNECTMODE**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Información dependiente del estado de la llamada. Vea *dwParam1*.

> [!Note]  
> En los casos en los que una respuesta *diferida* sea adecuada, use LINEDISCONNECTMODE \_ TEMPFAILURE. Si una respuesta *bloqueo* es adecuada, use LINEDISCONNECT \_ blocked. Para obtener más información, [**vea \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).

 

Si *dwParam1* es LINECALLSTATE \_ Conference, *DwParam2* contiene el parámetro *hConfCall* de la llamada primaria de la Conferencia de la que el sujeto *hCall* es miembro. Si la llamada especificada en *dwParam2* no se consideró anteriormente en la aplicación para que fuera una llamada de conferencia primaria (*hConfCall*, la aplicación debe hacerlo como resultado de este mensaje. Si la aplicación no tiene un identificador a la llamada primaria de la Conferencia (porque ha llamado previamente a [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) en ese identificador) *dwParam2* se establece en **null**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si es cero, este parámetro indica que no ha habido ningún cambio en el privilegio de la aplicación para la llamada.

Si es distinto de cero, especifica el privilegio de la aplicación para la llamada. Esto sucede en las siguientes situaciones: (1) la primera vez que se asigna a la aplicación un identificador a esta llamada; (2) cuando la aplicación es el destino de una entrega de llamada (incluso si la aplicación ya era propietaria de la llamada). Este parámetro utiliza una de las [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)siguientes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje se envía a cualquier aplicación que tenga un identificador para la llamada. El mensaje **line \_ CALLSTATE** también notifica a las aplicaciones que supervisan las llamadas en una línea sobre la existencia y el estado de las llamadas salientes establecidas por otras aplicaciones o manualmente por el usuario (por ejemplo, en un dispositivo telefónico conectado). El estado de la llamada de estas llamadas refleja el estado real de la llamada, que no es *ofrecer*. Al examinar el estado de la llamada, la aplicación puede determinar si la llamada es una llamada entrante que debe responderse o no.

Un mensaje de **línea \_ CALLSTATE** con un estado de llamada desconocido se puede enviar a una aplicación de supervisión como resultado de un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) correctos solicitados por otra aplicación. Al mismo tiempo que se envía a la aplicación que realiza la solicitud una [**\_ respuesta de línea**](line-reply.md) (Success) para la operación solicitada, se envía a todas las aplicaciones de supervisión de la línea el mensaje **\_ CALLSTATE** (Unknown) de la línea. Un mensaje de **\_ CALLSTATE de línea** que indica que el estado de la llamada "real" de la llamada recién generada se envía (utilizando la información proporcionada por el proveedor de servicios) a las aplicaciones que se solicitan y supervisan poco después.

Se envía un mensaje de **\_ CALLSTATE de línea** (desconocido) a las aplicaciones de supervisión solo si [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) hace que las llamadas se resuelvan en una conferencia de tres vías.

Por compatibilidad con versiones anteriores, las aplicaciones antiguas no esperan ningún valor determinado en *dwParam2* de un mensaje de LINECALLSTATE \_ Conference. Por tanto, TAPI pasa la llamada primaria *hConfCall* en *dwParam2* independientemente de la versión de la API de la aplicación que recibe el mensaje. En el caso de una llamada de conferencia iniciada por el proveedor de servicios, la aplicación anterior no es consciente de que la llamada primaria se ha convertido en una llamada de conferencia, a menos que se trate de examinar espontáneamente otra información (por ejemplo, llamar a [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).

Este mensaje no se puede deshabilitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**respuesta de línea \_**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




