---
title: Tipo complejo ValueMapType
description: Define una lista de asignaciones de nombre y valor entre valores enteros y valores de cadena.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- Tipo complejo EventLog de ValueMapType
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242697"
---
# <a name="valuemaptype-complex-type"></a>Tipo complejo ValueMapType

Define una lista de asignaciones de nombre y valor entre valores enteros y valores de cadena.

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                     | Tipo                                                                           | Descripción                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Mapa**](eventmanifestschema-map-valuemaptype-element.md) | [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md) | Define la asignación entre un valor entero y un valor de cadena.<br/> |



## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | Nombre del mapa de valores. Use el nombre de un elemento de datos para hacer referencia a las asignaciones.<br/>                                                                                                                                                                                                                     |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia a las asignaciones de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el mapa en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





