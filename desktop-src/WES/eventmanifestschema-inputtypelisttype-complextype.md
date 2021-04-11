---
title: Tipo complejo de InputTypeListType
description: Define una lista de tipos de entrada.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151071"
---
# <a name="inputtypelisttype-complex-type"></a>Tipo complejo de InputTypeListType

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





