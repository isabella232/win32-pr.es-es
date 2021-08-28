---
description: El elemento opcional booleano includeInStartMenuScope especifica si este conector de búsqueda debe incluirse en el &lt; &gt; menú Inicio de búsqueda.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20696dc6d2bc41b3f693e771a59541204e376e7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882394"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Elemento includeInStartMenuScope (esquema del conector de búsqueda)

El elemento opcional booleano includeInStartMenuScope especifica si este conector de búsqueda debe incluirse en el &lt; &gt; menú Inicio de búsqueda. El valor predeterminado es true para los conectores de búsqueda que usan el sistema de archivos como origen de datos y false para los conectores de búsqueda utilizados por los controladores de propiedades. Este elemento no tiene elementos secundarios ni atributos.

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



 

 



