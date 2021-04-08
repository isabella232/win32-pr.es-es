---
description: Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipo complejo de contadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001969"
---
# <a name="counters-complex-type"></a>Tipo complejo de contadores

Define la sección del manifiesto de instrumentación que identifica el proveedor y los contadores que proporcionan.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento      | Tipo                                                               | Descripción                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **presta** | [**Man: proveedor**](performance-counters-provider-complex-type.md) | Identifica un proveedor que proporciona contadores.<br/> |



## <a name="attributes"></a>Atributos



| Nombre          | Tipo | Descripción                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Versión del esquema que se usa para escribir el manifiesto.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**instrumentación**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

