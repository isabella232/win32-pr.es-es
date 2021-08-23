---
title: Tipo complejo PatternMapListType
description: No se usa. Define una lista de pares de expresiones regulares que se usan para modificar la cadena del mensaje.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Tipo complejo EventLog de PatternMapListType
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbf96f7033f353662578e477fb8e35e0bfcda6db390f6492e29840e5e1faa5cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136208"
---
# <a name="patternmaplisttype-complex-type"></a>Tipo complejo PatternMapListType

No se usa. Define una lista de pares de expresiones regulares que se usan para modificar la cadena del mensaje.

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                                     | Descripción                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**patternMap**](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md) | Define una asignación entre dos expresiones regulares. Una expresión se usa para buscar una cadena correspondiente en la cadena del mensaje y la otra para modificar la cadena antes de que el servicio la vuelva a coloca en la cadena del mensaje. Se usa la primera asignación de patrones que coincide y no se prueban otros patrones.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





