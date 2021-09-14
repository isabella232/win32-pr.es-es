---
title: EventTrigger.ValueQueries, propiedad
description: Para el scripting, obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento correspondiente que se devuelve de la consulta de suscripción especificada en la propiedad Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- ValueQueries, propiedad Programador de tareas
- Propiedad ValueQueries Programador de tareas , objeto EventTrigger
- Objeto EventTrigger Programador de tareas , propiedad ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068661"
---
# <a name="eventtriggervaluequeries-property"></a>EventTrigger.ValueQueries, propiedad

Para el scripting, obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento correspondiente que se devuelve de la consulta de suscripción especificada en la [**propiedad Subscription.**](eventtrigger-subscription.md)

## <a name="syntax"></a>Sintaxis


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valor de propiedad

Colección de pares nombre-valor. Cada par nombre-valor de la colección define un nombre único para un valor de propiedad del evento que desencadena el desencadenador de eventos. El valor de propiedad del evento se define como una consulta de eventos XPath. Para obtener más información sobre las consultas de eventos XPath, vea [Selección de eventos.](/previous-versions//aa385231(v=vs.85))

## <a name="remarks"></a>Observaciones

El nombre de la consulta se puede usar como variable en las siguientes propiedades de acción:

-   [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction.Title**](showmessageaction-title.md)
-   [**ExecAction.Arguments**](execaction-arguments.md)
-   [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction.Server**](emailaction-server.md)
-   [**EmailAction.Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction.Bcc**](emailaction-bcc.md)
-   [**EmailAction.ReplyTo**](emailaction-replyto.md)
-   [**EmailAction.From**](emailaction-from.md)
-   [**EmailAction.Body**](emailaction-body.md)
-   [**ComHandlerAction.Data**](comhandleraction-data.md)

Las cadenas de ejemplo de código siguientes muestran dos pares de valor de nombre que se pueden usar en una colección nombre-valor. Los valores devueltos por las consultas XPath pueden reemplazar variables en la propiedad de una acción. Se hace referencia a los valores por nombre, con `$(user)` y , en la propiedad `$(machine)` action. Por ejemplo, si las variables y se usan en la cadena `$(user)` `$(machine)` [**ShowMessageAction.MessageBody,**](showmessageaction-messagebody.md) el valor de las consultas XPath reemplazará las variables de la cadena.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Para obtener más información sobre cómo escribir una cadena de consulta para [determinados](../wes/subscribing-to-events.md)eventos, vea [Selección de](/previous-versions//aa385231(v=vs.85)) eventos y Suscripción a eventos .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

