---
description: El <domain> elemento opcional especifica la dirección URL del servicio de búsqueda que usa este conector de búsqueda. Se muestra en el panel de detalles. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento domain (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907739"
---
# <a name="domain-element-search-connector-schema"></a>Elemento domain (esquema del conector de búsqueda)

El <domain> elemento opcional especifica la dirección URL del servicio de búsqueda que usa este conector de búsqueda. Se muestra en el panel de detalles. Este elemento no tiene ningún elemento secundario y no tiene atributos.

## <a name="syntax"></a>Sintaxis


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

La dirección URL debe ser el dominio de nivel superior del proveedor de búsquedas. Por ejemplo, https://www.example.com.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



