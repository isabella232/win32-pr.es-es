---
title: Tipo complejo TemplateListType
description: Define una lista de plantillas que especifican los datos que se incluirán con los eventos. | Tipo complejo TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- TemplateListType de tipo complejo EventLog
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8659270ffded1724ce308e2a6c69aeefb34271f2be39f4468d8e7e460b20fd3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005715"
---
# <a name="templatelisttype-complex-type"></a>Tipo complejo TemplateListType

Define una lista de plantillas que especifican los datos que se incluirán con los eventos.

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo                                                                         | Descripción                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Plantilla**](eventmanifestschema-template-templatelisttype-element.md) | [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) | Plantilla que define los datos que se incluirán con un evento .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





