---
title: Tipo complejo de OpcodeListType
description: Define una lista de códigos de operación que se usan para identificar las operaciones de un componente de la aplicación.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490420"
---
# <a name="opcodelisttype-complex-type"></a>Tipo complejo de OpcodeListType

Define una lista de códigos de operación que se usan para identificar las operaciones de un componente de la aplicación.

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo                                                             | Descripción                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Código**](eventmanifestschema-opcode-opcodelisttype-element.md) | [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md) | Define una operación dentro de un componente de la aplicación.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





