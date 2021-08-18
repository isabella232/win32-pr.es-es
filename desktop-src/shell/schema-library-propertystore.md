---
description: El <propertyStore> elemento especifica un conjunto de una o varias propiedades usadas por esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff30972a358916e715ff1b374a555c6db24ee6d512d114bcf47f57ac8a1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452980"
---
# <a name="propertystore-element-library-schema"></a>elemento propertyStore (esquema de biblioteca)

El <propertyStore> elemento especifica un conjunto de una o varias propiedades usadas por esta biblioteca. Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [elemento property (Esquema de biblioteca)](schema-library-property.md) |



 

## <a name="remarks"></a>Comentarios

El <propertyStore> elemento puede tener uno o varios elementos <property> secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
