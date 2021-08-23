---
description: El elemento booleano opcional especifica si la ubicación descrita en el <isDefaultSaveLocation> conector de búsqueda debe usarse como ubicación de guardado predeterminada. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94cfe2f620dd7c4ccac2bed27dd87511e9174861aeb74dce9ac5737263e9275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597485"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Elemento isDefaultSaveLocation (esquema del conector de búsqueda)

El elemento booleano opcional especifica si la ubicación descrita en el <isDefaultSaveLocation> conector de búsqueda debe usarse como ubicación de guardado predeterminada. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Cuando un usuario elige guardar un elemento, Windows Explorer lo guarda en la ubicación especificada en el <simpleLocation> elemento. Los usuarios pueden cambiar esta configuración mediante el cuadro de diálogo Propiedades del conector de búsqueda.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



