---
title: Tipo complejo InputTypeListType
description: Define una lista de tipos de entrada.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Tipo complejo InputTypeListType EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 156ee19a90cdbb64e742d9876a39741155a3d5172f8da05f38f666cc077fc47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343746"
---
# <a name="inputtypelisttype-complex-type"></a>Tipo complejo InputTypeListType

Define una lista de tipos de entrada.

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                | Tipo                                                           | Descripción                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [**Intype**](eventmanifestschema-intype-inputtypelisttype-element.md) | [**InputType**](eventmanifestschema-inputtype-complextype.md) | Define un tipo de entrada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





