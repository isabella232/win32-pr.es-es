---
description: El elemento booleano opcional <isDefaultNonOwnerSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696266"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)

El elemento booleano opcional <isDefaultNonOwnerSaveLocation> especifica si la ubicación descrita en el conector de búsqueda debe usarse como ubicación de almacenamiento predeterminada cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento. Este elemento no tiene ningún elemento secundario y no tiene atributos.

## <a name="syntax"></a>Sintaxis


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



 

## <a name="remarks"></a>Observaciones

Si es true, cuando un usuario de otro equipo de un grupo en el hogar decide guardar un elemento, el explorador de Windows guarda el elemento en la ubicación especificada en el <simpleLocation> elemento.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



