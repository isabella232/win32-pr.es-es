---
description: El elemento booleano opcional <includeInStartMenuScope> especifica si este conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696267"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Elemento includeInStartMenuScope (esquema del conector de búsqueda)

El elemento booleano opcional <includeInStartMenuScope> especifica si este conector de búsqueda debe incluirse en el ámbito de búsqueda del menú Inicio. El valor predeterminado es true para los conectores de búsqueda que usan el sistema de archivos como origen de datos y false para los conectores de búsqueda utilizados por los controladores de propiedades. Este elemento no tiene ningún elemento secundario y no tiene atributos.

## <a name="syntax"></a>Sintaxis


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
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

Si incluye el conector de búsqueda en el ámbito del menú Inicio, los usuarios pueden buscar en su ubicación en el cuadro de búsqueda del menú Inicio.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



