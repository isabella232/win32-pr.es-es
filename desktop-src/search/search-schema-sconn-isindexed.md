---
description: El elemento opcional booleano isIndexed especifica si la ubicación descrita por el conector de búsqueda está indexada (ya sea de forma local o remota mediante Windows Search 4 o &lt; &gt; superior).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento isIndexed (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881842"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento isIndexed (esquema del conector de búsqueda)

El elemento opcional booleano isIndexed especifica si la ubicación descrita por el conector de búsqueda está indexada (ya sea de forma local o remota mediante Windows Search 4 o &lt; &gt; superior). El valor predeterminado es true para las carpetas locales. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                                                   | Elementos secundarios |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



