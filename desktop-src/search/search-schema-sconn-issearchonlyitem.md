---
description: El <isSearchOnlyItem> elemento booleano especifica si el proveedor de búsquedas admite el modo de exploración además del modo de búsqueda. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540630"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Elemento isSearchOnlyItem (esquema del conector de búsqueda)

El <isSearchOnlyItem> elemento booleano especifica si el proveedor de búsquedas admite el modo de exploración además del modo de búsqueda. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.

## <a name="syntax"></a>Sintaxis


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



 

## <a name="remarks"></a>Observaciones

El valor `true` indica que los usuarios no pueden examinar la ubicación del conector de búsqueda. El valor `false` indica que los usuarios pueden examinar la ubicación del conector de búsqueda.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



