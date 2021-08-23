---
title: Tipo complejo PatternMapValueType
description: No se usa. Define las expresiones regulares utilizadas para buscar una cadena correspondiente en la cadena del mensaje y modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- EventLog de tipo complejo PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136169"
---
# <a name="patternmapvaluetype-complex-type"></a>Tipo complejo PatternMapValueType

No se usa. Define las expresiones regulares utilizadas para buscar una cadena correspondiente en la cadena del mensaje y modificarla.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre  | Tipo   | Descripción                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | string | Expresión regular que se usa para buscar una cadena que coincida en la cadena del mensaje.<br/>                   |
| value | string | Expresión regular usada para modificar la cadena de coincidencia que se encontró en la cadena del mensaje.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





