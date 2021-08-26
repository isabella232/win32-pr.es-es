---
description: El elemento <includeInStartMenuScope> booleano opcional especifica si este conector de búsqueda debe incluirse en el menú Inicio de búsqueda.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: elemento includeInStartMenuScope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60941ef06f3f7220c7bbbae652f5e8256c6256660ea8e9ece2ddd330858958b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937955"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>elemento includeInStartMenuScope (esquema del conector de búsqueda)

El elemento <includeInStartMenuScope> booleano opcional especifica si este conector de búsqueda debe incluirse en el menú Inicio de búsqueda. El valor predeterminado es true para los conectores de búsqueda que usan el sistema de archivos como origen de datos y false para los conectores de búsqueda utilizados por los controladores de propiedades. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


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



 

## <a name="remarks"></a>Comentarios

Si incluye el conector de búsqueda en el ámbito menú Inicio, los usuarios pueden buscar en su ubicación desde el cuadro de búsqueda de la menú Inicio.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



