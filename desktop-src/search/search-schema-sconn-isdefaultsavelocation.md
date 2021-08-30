---
description: El elemento booleano opcional isDefaultSaveLocation especifica si la ubicación descrita en el conector de búsqueda debe usarse &lt; como ubicación de guardado &gt; predeterminada. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a17324f7658290c0eed9345f899f0d9c94f208
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881907"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Elemento isDefaultSaveLocation (esquema del conector de búsqueda)

El elemento booleano opcional isDefaultSaveLocation especifica si la ubicación descrita en el conector de búsqueda debe usarse &lt; como ubicación de guardado &gt; predeterminada. Este elemento no tiene elementos secundarios ni atributos.

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

Cuando un usuario decide guardar un elemento, Windows Explorer guarda el elemento en la ubicación especificada en el &lt; elemento &gt; simpleLocation. Los usuarios pueden cambiar esta configuración mediante el cuadro de diálogo Propiedades del conector de búsqueda.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



