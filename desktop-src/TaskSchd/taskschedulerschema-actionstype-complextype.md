---
title: actionsType Complex Type
description: Define los elementos secundarios y el atributo para el elemento Actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- actionsType complex type Programador de tareas
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d84cab2f0977a3b5bf980f594f1b26b543d8e5e7de000959488e874e640dc9d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010935"
---
# <a name="actionstype-complex-type"></a>actionsType Complex Type

Define los elementos secundarios y el atributo para el [**elemento**](taskschedulerschema-actions-tasktype-element.md) Actions.

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre    | Tipo  | Descripción                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| Context | IDREF | Identificador principal del utilizado que es el contexto de seguridad para las acciones de la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





