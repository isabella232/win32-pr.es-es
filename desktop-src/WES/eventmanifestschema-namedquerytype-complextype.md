---
title: Tipo complejo NamedQueryType
description: No se usa. Define una lista de consultas con nombre que consultan la cadena del mensaje de evento para obtener un valor y realizan una acción especificada si se encuentran. | Tipo complejo NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- EventLog de tipo complejo NamedQueryType
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba83c2716b765082cdd32458a093bc0300fea369a810251e6f5ebf28e97f9485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652165"
---
# <a name="namedquerytype-complex-type"></a>Tipo complejo NamedQueryType

No se usa. Define una lista de consultas con nombre que consultan la cadena del mensaje de evento para obtener un valor y realizan una acción especificada si se encuentran.

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
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | Define una lista de pares de expresiones regulares que se usan para modificar la cadena del mensaje.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar el [**elemento namedQueries.**](eventmanifestschema-namedqueries-metadatatype-element.md) En este ejemplo se toma el contenido de la cadena de mensaje y se inserta en la cadena https://www .*messagestring*.com. A continuación, reemplaza la cadena de mensaje por el resultado. Por ejemplo, si la cadena de mensaje contenía Microsoft, la consulta reemplazaría la cadena de mensaje de Microsoft por https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





