---
title: Propiedad EventTrigger. ValueQueries
description: En el caso de scripting, obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de suscripción.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Programador de tareas de la propiedad ValueQueries
- Propiedad ValueQueries Programador de tareas, objeto EventTrigger
- Objeto EventTrigger Programador de tareas, propiedad ValueQueries
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534894"
---
# <a name="eventtriggervaluequeries-property"></a>Propiedad EventTrigger. ValueQueries

En el caso de scripting, obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de [**suscripción**](eventtrigger-subscription.md) .

## <a name="syntax"></a>Sintaxis


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valor de propiedad

Colección de de pares nombre-valor. Cada par nombre-valor de la colección define un nombre único para un valor de propiedad del evento que desencadena el desencadenador de eventos. El valor de propiedad del evento se define como una consulta de evento XPath. Para obtener más información acerca de las consultas de eventos XPath, consulte [selección de eventos](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Observaciones

El nombre de la consulta se puede usar como una variable en las siguientes propiedades de acción:

-   [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction. title**](showmessageaction-title.md)
-   [**ExecAction. arguments**](execaction-arguments.md)
-   [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction. Server**](emailaction-server.md)
-   [**EmailAction. Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction. BCC**](emailaction-bcc.md)
-   [**EmailAction. ReplyTo**](emailaction-replyto.md)
-   [**EmailAction. from**](emailaction-from.md)
-   [**EmailAction. Body**](emailaction-body.md)
-   [**ComHandlerAction. Data**](comhandleraction-data.md)

Las cadenas de ejemplo de código siguientes muestran dos pares de nombre y valor que se pueden usar en una colección de nombre y valor. Los valores devueltos por las consultas XPath pueden reemplazar las variables en la propiedad de una acción. Se hace referencia a los valores por nombre, con `$(user)` y `$(machine)` , en la propiedad Action. Por ejemplo, si `$(user)` `$(machine)` se usan las variables y en la cadena [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , el valor de las consultas XPath reemplazará las variables de la cadena.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Para obtener más información sobre cómo escribir una cadena de consulta para determinados eventos, vea [selección de eventos](/previous-versions//aa385231(v=vs.85)) y [suscripción a eventos](../wes/subscribing-to-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

