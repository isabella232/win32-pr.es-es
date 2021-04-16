---
title: Tipo complejo de headerFieldType
description: Define los elementos que se usan para crear un campo de encabezado en un mensaje de correo electrónico.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- tipo complejo de headerFieldType Programador de tareas
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676683"
---
# <a name="headerfieldtype-complex-type"></a>Tipo complejo de headerFieldType

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
| [**Name**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica el nombre del campo de encabezado en un mensaje de correo electrónico.<br/> |
| [**Value**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Especifica el valor de un campo de encabezado en un mensaje de correo electrónico.<br/>  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





