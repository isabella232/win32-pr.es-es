---
title: Tipo complejo de KeywordListType
description: Define una lista de palabras clave que clasifican eventos. | Tipo complejo de KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- KeywordListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698091"
---
# <a name="keywordlisttype-complex-type"></a>Tipo complejo de KeywordListType

Define una lista de palabras clave que clasifican eventos.

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                | Tipo                                                               | Descripción                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**palabra clave**](eventmanifestschema-keyword-keywordlisttype-element.md) | [**KeywordType**](eventmanifestschema-keywordtype-complextype.md) | Define una palabra clave que identifica una categoría de eventos. Puede especificar un máximo de 48 palabras clave.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





