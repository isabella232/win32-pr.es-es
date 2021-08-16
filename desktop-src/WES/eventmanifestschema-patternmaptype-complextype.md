---
title: Tipo complejo PatternMapType
description: No se usa. Define una asignación entre dos expresiones regulares. Una expresión se usa para buscar una cadena correspondiente en la cadena del mensaje y la otra para modificar la cadena antes de que el servicio la vuelva a coloca en la cadena del mensaje.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- EventLog de tipo complejo PatternMapType
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d4ba0c404220023a124c082ea448cbb7bdcab192b611bf35a2afc90df82e9e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136198"
---
# <a name="patternmaptype-complex-type"></a>Tipo complejo PatternMapType

No se usa. Define una asignación entre dos expresiones regulares. Una expresión se usa para buscar una cadena correspondiente en la cadena del mensaje y la otra para modificar la cadena antes de que el servicio la vuelva a coloca en la cadena del mensaje.

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
| [**Mapa**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | Define las expresiones regulares utilizadas para buscar una cadena correspondiente en la cadena del mensaje y modificarla.<br/> |



## <a name="attributes"></a>Atributos



| Nombre   | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Motor de expresiones regulares que se usará.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Nombre del mapa de patrones. Use el nombre de un elemento de datos para hacer referencia a las asignaciones.<br/>                                                                                                                                                                                                                   |
| símbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia a las asignaciones de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el mapa en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





