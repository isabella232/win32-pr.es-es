---
title: Tipo complejo de PatternMapValueType
description: No se utiliza. Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType tipo complejo EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800949"
---
# <a name="patternmapvaluetype-complex-type"></a>Tipo complejo de PatternMapValueType

No se utiliza. Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.

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
| name  | string | Expresión regular utilizada para buscar una cadena coincidente en la cadena de mensaje.<br/>                   |
| value | string | Expresión regular que se usa para modificar la cadena coincidente que se encontró en la cadena de mensaje.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





