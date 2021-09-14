---
title: Elemento Value (namedValues)
description: Contiene el valor asociado a un nombre en un par nombre-valor.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Valor, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968560"
---
# <a name="value-namedvalues-element"></a>Elemento Value (namedValues)

Contiene el valor asociado a un nombre en un par nombre-valor.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

El **elemento Value** se define mediante el tipo complejo [**namedValues.**](taskschedulerschema-namedvalues-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                              | Derivado de                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Especifica una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento correspondiente que se devuelve de la consulta de suscripción especificada en el [**elemento Subscription.**](taskschedulerschema-subscription-eventtriggertype-element.md) El nombre de la consulta se puede usar como variable en el mensaje de una acción ShowMessage.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Propiedad Value de ITaskNamedValuePair.**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value)

Para el desarrollo de scripts, [**vea TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





