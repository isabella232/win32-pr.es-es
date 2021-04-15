---
description: Especifica un alias de ordenación o una lista de alias de ordenación mediante la especificación de un elemento que contiene una propiedad de ordenación o una lista de propiedades de ordenación.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715769"
---
# <a name="aliasinfo"></a>aliasInfo

Especifica un alias de ordenación o una lista de alias de ordenación mediante la especificación de un elemento que contiene una propiedad de ordenación o una lista de propiedades de ordenación. Solo debe haber un elemento [aliasInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) . En el caso de las propiedades que establecen canGroupBy = true, a menos que se especifique una propiedad de ordenación secundaria ( aliasInfo/@additionalSortByAliases = prop: example), el usuario puede experimentar un comportamiento inesperado al cambiar el criterio de ordenación en una vista que está agrupada por la propiedad. En concreto, el orden de los grupos cambiará, pero el orden de los elementos dentro de los grupos no lo hará.

## <a name="syntax"></a>Sintaxis


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                   | Elementos secundarios |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Atributos



| Atributo               | Descripción                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Público. Opcional. Nombre canónico de la propiedad que se debe usar para ordenar por. Esta cadena es de tipo canónico-Type.                                            |
| additionalSortByAliases | Público. Opcional. Una lista delimitada por punto y coma de propiedades adicionales que se usarán al ordenar. Las propiedades se aplican a la ordenación en la secuencia en la que se proporcionan. |



 

 

 
