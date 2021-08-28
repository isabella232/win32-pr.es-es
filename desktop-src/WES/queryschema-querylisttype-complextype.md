---
title: Tipo complejo QueryListType
description: Define una lista de consultas que pueden contener un conjunto de selectores y supresores que se usan para incluir eventos en o excluir eventos del conjunto de resultados.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType de tipo complejo EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1692427538dcd500cd4190839ffcc148c7358e0aee7f5a27b4906192a0810b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904165"
---
# <a name="querylisttype-complex-type"></a>Tipo complejo QueryListType

Define una lista de consultas que pueden contener un conjunto de selectores y supresores que se usan para incluir eventos en o excluir eventos del conjunto de resultados.

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                  | Tipo                                                   | Descripción                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Consulta**](queryschema-query-querylisttype-element.md) | [**Querytype**](queryschema-querytype-complextype.md) | Define un conjunto de selectores y supresores que se usan para incluir eventos en o excluir eventos del conjunto de resultados.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





