---
title: Tipo complejo ComplexDataType
description: Define una estructura que contiene uno o varios elementos de datos.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055813"
---
# <a name="complexdatatype-complex-type"></a>Tipo complejo ComplexDataType

Define una estructura que contiene uno o varios elementos de datos.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                  | Tipo                                                      | Descripción                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**data**](eventschema-data-complexdatatype-element.md) | [**Datatype**](eventschema-datafieldtype-complextype.md) | Lista de elementos de datos de la estructura . La lista de elementos está en el mismo orden que se define en la plantilla.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre | string | Nombre de la estructura. Este es el nombre que se especifica al definir la estructura en la plantilla (vea el tipo [**complejo TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |



## <a name="remarks"></a>Comentarios

La [**función EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa el contenido de una estructura como un blob binario; la función no representa los elementos de datos individuales de la estructura .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





