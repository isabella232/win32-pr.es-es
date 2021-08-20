---
title: tipo complejo headerFieldType
description: Define los elementos que se usan para crear un campo de encabezado en un mensaje de correo electrónico.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Tipo complejo headerFieldType Programador de tareas
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78c4fb3a8ca85cea5b765fc1fc4521f968efd76e9169613dc4a1565a43ee1b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131834"
---
# <a name="headerfieldtype-complex-type"></a>tipo complejo headerFieldType

Define los elementos que se usan para crear un campo de encabezado en un mensaje de correo electrónico.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                            | Tipo                                                                    | Descripción                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nombre**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica el nombre del campo de encabezado en un mensaje de correo electrónico.<br/> |
| [**Valor**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Especifica el valor de un campo de encabezado en un mensaje de correo electrónico.<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





