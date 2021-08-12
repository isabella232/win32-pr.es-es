---
title: Tipo complejo QueryType
description: Define un conjunto de consultas de selector y supresor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- EventLog de tipo complejo QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6585b43e1e9e48bc0be69001d471c74e52506177250d66316273ca447b38084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587630"
---
# <a name="querytype-complex-type"></a>Tipo complejo QueryType

Define un conjunto de consultas de selector y supresor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                    | Tipo | Descripción                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Seleccionar**](queryschema-select-querytype-element.md)     |      | Una consulta XPath que identifica los eventos que se incluirán en el conjunto de resultados de la consulta. Especifique XPath en el cuerpo de texto de este elemento. XPath está limitado a 32 expresiones.<br/>   |
| [**Suprimir**](queryschema-suppress-querytype-element.md) |      | Una consulta XPath que identifica los eventos que se excluirán del conjunto de resultados de la consulta. Especifique XPath en el cuerpo de texto de este elemento. XPath está limitado a 32 expresiones.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador   | long   | Identificador que identifica de forma única esta consulta en la lista de consultas. El identificador es de base cero. Debe especificar un identificador si la lista de consultas contiene más de una consulta.<br/> |
| Path | anyURI | Nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/>                                                                                                            |
| Path | anyURI | Nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/>                                                                                                            |
| Path | anyURI | No se usa.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Comentarios

La consulta debe tener al menos una instrucción select. Para cada instrucción suppress, debe haber al menos una instrucción select que especifique la misma ruta de acceso. Si la consulta select y suppress devuelve los mismos eventos, la instrucción suppress tiene prioridad. Si selecciona eventos de varios orígenes, los eventos se devuelven en el orden de marca de tiempo. Si usa la marca de tiempo del sistema y la tasa de eventos es alta, es posible que más de un evento tenga la misma marca de tiempo. Cuando esto ocurre, el orden de los eventos se vuelve ambiguo y los eventos pueden aparecer fuera de orden.

Si especifica una ruta de acceso para una de las consultas de la lista de consultas, todas las consultas deben especificar una ruta de acceso. Si no especifica una ruta de acceso para todas las consultas, debe especificar la ruta de acceso al llamar a la [**función EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe.**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





