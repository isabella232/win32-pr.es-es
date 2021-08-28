---
description: El elemento opcional &lt; booleano isDefaultNonOwnerSaveLocation especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de guardado predeterminada cuando un usuario de otro equipo de un grupo de inicio decide guardar &gt; un elemento.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2a20912b10864d856bd4513e31a37eeee5c2a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881941"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)

El elemento opcional &lt; booleano isDefaultNonOwnerSaveLocation especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de guardado predeterminada cuando un usuario de otro equipo de un grupo de inicio decide guardar &gt; un elemento. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Si es true, cuando un usuario de otro equipo de un grupo de inicio decide guardar un elemento, Windows Explorer guarda el elemento en la ubicación especificada en el &lt; elemento &gt; simpleLocation.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



