---
description: El &lt; elemento propertyStore &gt; especifica un conjunto de una o varias propiedades usadas por esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089e87e6e7bdfa568ffa2e8903f6347cb6dc7b3d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880431"
---
# <a name="propertystore-element-library-schema"></a>elemento propertyStore (esquema de biblioteca)

El &lt; elemento propertyStore &gt; especifica un conjunto de una o varias propiedades usadas por esta biblioteca. Este elemento es opcional y no tiene atributos.

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

El &lt; elemento propertyStore &gt; puede tener uno o varios elementos secundarios de &lt; &gt; propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
