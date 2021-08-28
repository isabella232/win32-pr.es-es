---
title: Tipo complejo DataType (Windows de eventos)
description: Define un elemento de datos.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- EventLog de tipo complejo DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620285"
---
# <a name="datatype-complex-type"></a>Tipo complejo DataType

Define un elemento de datos.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre | string | Nombre de un elemento de datos definido en la plantilla (vea el tipo [**complejo TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |
| Tipo | QName  | No se usa.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Comentarios

El elemento de datos puede ser un elemento de datos de nivel superior o un elemento de datos de una estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





