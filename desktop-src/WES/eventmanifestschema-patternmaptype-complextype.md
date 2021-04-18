---
title: Tipo complejo de PatternMapType
description: No se utiliza. Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType tipo complejo EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491284"
---
# <a name="patternmaptype-complex-type"></a>Tipo complejo de PatternMapType

No se utiliza. Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                       | Tipo                                                                               | Descripción                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**mapa**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.<br/> |



## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Motor de expresiones regulares que se va a usar.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Nombre del mapa de patrones. Use el nombre en un elemento de datos para hacer referencia a las asignaciones.<br/>                                                                                                                                                                                                                   |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se va a usar para hacer referencia a las asignaciones de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para la asignación en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





