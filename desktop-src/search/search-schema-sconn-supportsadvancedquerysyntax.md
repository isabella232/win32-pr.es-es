---
description: El elemento &lt; booleano supportsAdvancedQuerySyntax especifica si el proveedor de &gt; búsqueda admite la sintaxis de consulta avanzada. El valor predeterminado es false. Este elemento es opcional y no tiene elementos secundarios ni atributos.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432c6917ccf03ddf4a00f30029e01b9075309c65
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880436"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)

El elemento &lt; booleano supportsAdvancedQuerySyntax especifica si el proveedor de &gt; búsqueda admite la sintaxis de consulta [avanzada](-search-3x-advancedquerysyntax.md). El valor predeterminado es false. Este elemento es opcional y no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
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

El valor `true` indica que el proveedor de búsqueda admite la sintaxis de consulta avanzada enviada en las consultas de búsqueda.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



