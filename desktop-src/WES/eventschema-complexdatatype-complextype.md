---
title: Tipo complejo de ComplexDataType
description: Define una estructura que contiene uno o más elementos de datos.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695992"
---
# <a name="complexdatatype-complex-type"></a>Tipo complejo de ComplexDataType

Define una estructura que contiene uno o más elementos de datos.

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
| [**Data**](eventschema-data-complexdatatype-element.md) | [**DataType**](eventschema-datafieldtype-complextype.md) | Lista de elementos de datos de la estructura. La lista de elementos está en el mismo orden que se define en la plantilla.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre | string | Nombre de la estructura. Este es el nombre que se especifica cuando se define la estructura en la plantilla (vea el tipo complejo de [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Observaciones

La función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa el contenido de una estructura como un BLOB binario; la función no representa los elementos de datos individuales de la estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





