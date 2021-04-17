---
description: Define una estructura que contiene uno o más valores de contador.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: struct (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667272"
---
# <a name="struct-complex-type"></a>struct (tipo complejo)

Define una estructura que contiene uno o más valores de contador.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre | Tipo                                                                    | Descripción                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**Man: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nombre de la estructura.<br/>                                                                                                            |
| type | [**Man: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nombre simbólico que identifica la estructura. La herramienta [CTRPP](ctrpp.md) crea una variable de estructura con este nombre que puede usar.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




