---
title: Tipo complejo de tipo de archivo (registro de eventos de Windows)
description: Define un elemento de datos.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- EventLog (tipo complejo de tipo de texto)
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359809"
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
| Nombre | string | El nombre de un elemento de datos que se definió en la plantilla (vea el tipo complejo de [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |
| Tipo | QName  | No se utiliza.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Observaciones

El elemento de datos puede ser un elemento de datos de nivel superior o un elemento de datos de una estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





