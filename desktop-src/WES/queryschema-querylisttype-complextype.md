---
title: Tipo complejo de QueryListType
description: Define una lista de consultas que pueden contener un conjunto de selectores e supresors que se usan para incluir eventos en el conjunto de resultados o para excluir eventos del mismo.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695916"
---
# <a name="querylisttype-complex-type"></a>Tipo complejo de QueryListType

Define una lista de consultas que pueden contener un conjunto de selectores e supresors que se usan para incluir eventos en el conjunto de resultados o para excluir eventos del mismo.

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
| [**Consulta**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | Define un conjunto de selectores y suprimidores que se usan para incluir eventos en o excluir eventos del conjunto de resultados.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





