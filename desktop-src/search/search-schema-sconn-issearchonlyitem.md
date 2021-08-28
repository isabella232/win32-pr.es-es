---
description: El elemento &lt; booleano isSearchOnlyItem especifica si el proveedor de búsqueda admite el &gt; modo de exploración además del modo de búsqueda. Este elemento es opcional y no tiene elementos secundarios ni atributos.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524a69198a650e0cb995d2ff8b4fc942ebfdaddc
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883417"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Elemento isSearchOnlyItem (esquema del conector de búsqueda)

El elemento &lt; booleano isSearchOnlyItem especifica si el proveedor de búsqueda admite el &gt; modo de exploración además del modo de búsqueda. Este elemento es opcional y no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
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



 

## <a name="remarks"></a>Comentarios

El valor indica que los usuarios no pueden examinar la ubicación del `true` conector de búsqueda. El valor `false` indica que los usuarios pueden examinar la ubicación del conector de búsqueda.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



