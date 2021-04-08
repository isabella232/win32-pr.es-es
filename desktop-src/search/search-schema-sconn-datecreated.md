---
description: El <dateCreated> elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda con el estándar ISO 8601. No tiene elementos secundarios ni atributos.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808906"
---
# <a name="datecreated-element-search-connector-schema"></a>Elemento dateCreated (esquema del conector de búsqueda)

El <dateCreated> elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda con el estándar ISO 8601. No tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Sintaxis


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



 

## <a name="remarks"></a>Observaciones

El formato del valor de este elemento sigue el estándar ISO 8601. Un uso común sería cualquiera de los siguientes:

-   \[YYYY \] - \[ mm \] - \[ DD \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05T14:30:30-05:00")
-   \[AAAA \] \[ mm \] \[ DD \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405T193030Z")

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



