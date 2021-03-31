---
title: QueryType (tipo complejo)
description: Define un conjunto de consultas de selector y suprimidor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Registro de eventos de tipo complejo de QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150241"
---
# <a name="querytype-complex-type"></a>QueryType (tipo complejo)

Define un conjunto de consultas de selector y suprimidor que se usan para incluir eventos en o excluir eventos del conjunto de resultados.

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
| [**Seleccionar**](queryschema-select-querytype-element.md)     |      | Consulta XPath que identifica los eventos que se van a incluir en el conjunto de resultados de la consulta. Especifique el XPath en el cuerpo del texto de este elemento. XPath está limitado a 32 expresiones.<br/>   |
| [**Suprimir**](queryschema-suppress-querytype-element.md) |      | Consulta XPath que identifica los eventos que se van a excluir del conjunto de resultados de la consulta. Especifique el XPath en el cuerpo del texto de este elemento. XPath está limitado a 32 expresiones.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador   | long   | Identificador que identifica de forma única esta consulta en la lista de consultas. El identificador es de base cero. Debe especificar un identificador si la lista de consultas contiene más de una consulta.<br/> |
| Ruta | anyURI | El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/>                                                                                                            |
| Ruta | anyURI | El nombre del canal o la ruta de acceso al archivo de registro que contiene los eventos.<br/>                                                                                                            |
| Ruta | anyURI | No se utiliza.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Observaciones

La consulta debe tener al menos una instrucción SELECT. Para cada instrucción Suppress, debe haber al menos una instrucción SELECT que especifique la misma ruta de acceso. Si la consulta SELECT y Suppress devuelve los mismos eventos, la instrucción Suppress tiene prioridad. Si selecciona eventos de varios orígenes, los eventos se devuelven en el orden de marca de tiempo. Si utiliza la marca de tiempo del sistema y la tasa de eventos es alta, es posible que más de un evento tenga la misma marca de tiempo. Cuando esto ocurre, el orden de los eventos se vuelve ambiguo y los eventos pueden aparecer desordenados.

Si especifica una ruta de acceso para una de las consultas de la lista de consultas, todas las consultas deben especificar una ruta de acceso. Si no especifica una ruta de acceso para todas las consultas, debe especificar la ruta de acceso al llamar a la función [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





