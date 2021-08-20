---
description: Opcional <description> El elemento especifica una descripción para este conector de búsqueda. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: elemento description (Esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4cadc9b41c7c85f95db9f455fabe61e65663b30a2b6882c796ad5f0126db7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680223"
---
# <a name="description-element-search-connector-schema"></a>elemento description (Esquema del conector de búsqueda)

Opcional <description> El elemento especifica una descripción para este conector de búsqueda. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
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

La descripción debe ser fácil de usar, ya que se puede usar en la información sobre herramientas.

## <a name="example"></a>Ejemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



