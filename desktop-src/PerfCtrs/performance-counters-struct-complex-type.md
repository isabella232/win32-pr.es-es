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
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978855"
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
| tipo | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nombre simbólico que identifica la estructura. La [herramienta CTRPP](ctrpp.md) crea una variable de estructura con este nombre que puede usar.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




