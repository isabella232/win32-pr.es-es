---
description: El elemento &lt; de dominio opcional especifica la dirección URL del servicio de búsqueda utilizado por este conector de &gt; búsqueda. Se muestra en el panel de detalles. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: elemento domain (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd84ffa2ee5bcc5f5f6dcdb93c9abbd12c57bd96
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882474"
---
# <a name="domain-element-search-connector-schema"></a>elemento domain (esquema del conector de búsqueda)

El elemento &lt; de dominio opcional especifica la dirección URL del servicio de búsqueda utilizado por este conector de &gt; búsqueda. Se muestra en el panel de detalles. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


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



 

## <a name="remarks"></a>Comentarios

La dirección URL debe ser el dominio de nivel superior para el proveedor de búsqueda. Por ejemplo, https://www.example.com.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



