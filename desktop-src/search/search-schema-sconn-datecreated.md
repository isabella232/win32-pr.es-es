---
description: El elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda <dateCreated> mediante el estándar ISO 8601. No tiene elementos secundarios ni atributos.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: elemento dateCreated (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b59af62b2bd7ce8678fafb1fdd84646314f41a51414b4285db3077b5db0e0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944405"
---
# <a name="datecreated-element-search-connector-schema"></a>elemento dateCreated (esquema del conector de búsqueda)

El elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda <dateCreated> mediante el estándar ISO 8601. No tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
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

El formato del valor de este elemento sigue el estándar ISO 8601. Un uso común sería cualquiera de los siguientes:

-   \[YYYY \] - \[ MM \] - \[ DD \] T hh : mm : \[ \] \[ \] \[ ss ± hh : \] mm \[ \] \[ \] ("1981-04-05T14:30:30-05:00")
-   \[YYYY \] \[ MM \] \[ DD \] T hh mm \[ \] \[ \] \[ ss Z \] ("19810405T193030Z")

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



