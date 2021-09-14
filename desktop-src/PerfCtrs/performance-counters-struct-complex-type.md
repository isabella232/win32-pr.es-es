---
description: Define una estructura que contiene uno o varios valores de contador.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complejo de struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250580"
---
# <a name="struct-complex-type"></a>Tipo complejo de struct

Define una estructura que contiene uno o varios valores de contador.

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
| name | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nombre de la estructura.<br/>                                                                                                            |
| type | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nombre simbólico que identifica la estructura. La [herramienta CTRPP](ctrpp.md) crea una variable de estructura con este nombre que puede usar.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




