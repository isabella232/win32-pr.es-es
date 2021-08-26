---
description: El mensaje TAPI LINE CALLSTATE se envía cuando el estado \_ de la llamada especificada ha cambiado.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: LINE_CALLSTATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d82dfb5f0d5e306085ecd2d7f29270d19c2c9c101e30ac547fe246b7e6fddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012575"
---
# <a name="line_callstate-message"></a>Mensaje \_ LINE CALLSTATE

El mensaje TAPI **LINE \_ CALLSTATE** se envía cuando el estado de la llamada especificada ha cambiado. Normalmente, se reciben varios de estos mensajes durante la vigencia de una llamada. Las aplicaciones son notificadas de nuevas llamadas entrantes con este mensaje; la nueva llamada está en estado *de* oferta. La aplicación puede usar [**lineGetCallStatus para**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) recuperar información más detallada sobre el estado actual de la llamada.


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

Nuevo estado de llamada. Este parámetro debe ser uno y solo una de las siguientes [**constantes LINECALLSTATE \_**](linecallstate--constants.md).



| dwParam1                                                                                                                                                                                             | Significado                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <dt>**LINECALLSTATE \_ BUSY**</dt> </dl>                         | *dwParam2 contiene* detalles sobre el modo ocupado. Este parámetro usa una de las [**constantes LINEBUSYMODE \_**](linebusymode--constants.md).<br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <dt>**LINECALLSTATE \_ CONECTADO**</dt> </dl>          | *dwParam2 contiene* detalles sobre el modo conectado. Este parámetro usa una de las [**constantes LINECONNECTEDMODE \_**](lineconnectedmode--constants.md).<br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <dt>**LINECALLSTATE \_ DIALTONE**</dt> </dl>             | *dwParam2 contiene* detalles sobre el modo de tono de marcado. Este parámetro usa una de las [**constantes DELINEIALTONEMODE \_**](linedialtonemode--constants.md).<br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <dt>**OFERTA \_ LINECALLSTATE**</dt> </dl>             | *dwParam2 contiene* detalles sobre el modo conectado. Este parámetro usa una de las [**constantes LINEOFFERINGMODE \_**](lineofferingmode--constants.md).<br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <dt>**LINECALLSTATE \_ SPECIALINFO**</dt> </dl>    | *dwParam2* contiene los detalles sobre el modo de información especial. Este parámetro usa una de las [**constantes LINESPECIALINFO \_**](linespecialinfo--constants.md).<br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <dt>**LINECALLSTATE \_ DISCONNECTED**</dt> </dl> | *dwParam2 contiene* detalles sobre el modo de desconexión. Este parámetro usa una de las [**constantes LINEDISCONNECTMODE \_**](linedisconnectmode--constants.md).<br/>        |



 

</dd> <dt>

*dwParam2* 
</dt> <dd>

Información dependiente del estado de llamada. Vea *dwParam1*.

> [!Note]  
> En circunstancias en las *que una respuesta* retrasada es adecuada, use LINEDISCONNECTMODE \_ TEMPFAILURE. Cuando una *respuesta en la lista de* bloqueos sea adecuada, use LINEDISCONNECT \_ BLOCKED. Para obtener más información, [**vea LINEDISCONNECTMODE \_ Constants**](linedisconnectmode--constants.md).

 

Si *dwParam1* es LINECALLSTATE \_ CONFERENCED, *dwParam2* contiene el parámetro *hConfCall* de la llamada primaria de la conferencia de la que el asunto *hCall* es miembro. Si la aplicación no consideró previamente que la llamada especificada en *dwParam2* era una llamada de conferencia primaria (*hConfCall*), la aplicación debe hacerlo como resultado de este mensaje. Si la aplicación no tiene un identificador para la llamada primaria de la conferencia (porque anteriormente ha llamado a [**lineDeallocateCall en**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ese identificador), *dwParam2* se establece en **NULL.**

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si es cero, este parámetro indica que no ha habido ningún cambio en el privilegio de la aplicación para la llamada.

Si es distinto de cero, especifica el privilegio de la aplicación para la llamada. Esto sucede en las situaciones siguientes: (1) La primera vez que se le da un identificador a la aplicación para esta llamada; (2) Cuando la aplicación es el destino de una entrega de llamada (incluso si la aplicación ya era propietaria de la llamada). Este parámetro usa una de las siguientes [**constantes LINECALLPRIVILEGE \_**](linecallprivilege--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este mensaje se envía a cualquier aplicación que tenga un identificador para la llamada. El **mensaje LINE \_ CALLSTATE** también notifica a las aplicaciones que supervisan las llamadas en una línea sobre la existencia y el estado de las llamadas salientes establecidas por otras aplicaciones o manualmente por el usuario (por ejemplo, en un dispositivo telefónico conectado). El estado de llamada de estas llamadas refleja el estado real de la llamada, que *no* ofrece . Al examinar el estado de la llamada, la aplicación puede determinar si la llamada es una llamada entrante que debe responderse o no.

Se puede enviar un mensaje **LINE \_ CALLSTATE** con un estado de llamada desconocido a una aplicación de supervisión como resultado de un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)correcto, [**lineForward,**](/windows/desktop/api/Tapi/nf-tapi-lineforward) [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer,**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) [**linePickup,**](/windows/desktop/api/Tapi/nf-tapi-linepickup) [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) solicitado por otra aplicación. Al mismo tiempo que se envía a la aplicación solicitante una respuesta LINE [**\_ REPLY**](line-reply.md) (correcta) para la operación solicitada, las aplicaciones de supervisión de la línea se envían al mensaje **LINE \_ CALLSTATE** (desconocido). Un **mensaje \_ LINE CALLSTATE** que indica el estado de llamada "real" de la llamada recién generada se envía (mediante la información proporcionada por el proveedor de servicios) a las aplicaciones que solicitan y supervisan poco después.

Se **envía un mensaje LINE \_ CALLSTATE** (desconocido) a las aplicaciones de supervisión solo si [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) hace que las llamadas se resuelvan en una conferencia triple.

Por compatibilidad con versiones anteriores, las aplicaciones anteriores no esperan ningún valor determinado en *dwParam2* de un mensaje LINECALLSTATE \_ CONFERENCED. TAPI, por tanto, pasa la llamada primaria *hConfCall* en *dwParam2* independientemente de la versión de API de la aplicación que recibe el mensaje. En el caso de una llamada de conferencia iniciada por el proveedor de servicios, la aplicación anterior no es consciente de que la llamada primaria se ha convertido en una llamada de conferencia a menos que se examine de forma desaprobada otra información (por ejemplo, llamar a [**lineGetConfRelatedCalls).**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)

Este mensaje no se puede deshabilitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RESPUESTA \_ DE LÍNEA**](line-reply.md)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**DELINEIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
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

 

 




