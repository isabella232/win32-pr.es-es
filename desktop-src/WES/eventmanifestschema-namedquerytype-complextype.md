---
title: Tipo complejo de NamedQueryType
description: No se utiliza. Define una lista de consultas con nombre que consultan la cadena de mensaje de evento de un valor y realizan una acción especificada si se encuentran. | Tipo complejo de NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType tipo complejo EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698125"
---
# <a name="namedquerytype-complex-type"></a>Tipo complejo de NamedQueryType

No se utiliza. Define una lista de consultas con nombre que consultan la cadena de mensaje de evento de un valor y realizan una acción especificada si se encuentran.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                       | Tipo                                                                             | Descripción                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | Define una lista de pares de expresiones regulares que se utilizan para modificar la cadena de mensaje.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar el elemento [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) . En este ejemplo se toma el contenido de la cadena de mensaje y se inserta en la cadena https://www .*messagestring*. com. A continuación, reemplaza la cadena de mensaje con el resultado. Por ejemplo, si la cadena de mensaje contiene Microsoft, la consulta reemplazaría la cadena de mensaje de Microsoft por https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





