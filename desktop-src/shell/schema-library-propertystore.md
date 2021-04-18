---
description: El <propertyStore> elemento especifica un conjunto de una o varias propiedades utilizadas por esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985819"
---
# <a name="propertystore-element-library-schema"></a>Elemento propertyStore (esquema de biblioteca)

El <propertyStore> elemento especifica un conjunto de una o varias propiedades utilizadas por esta biblioteca. Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Sintaxis

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
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Property (elemento, esquema de biblioteca)](schema-library-property.md) |



 

## <a name="remarks"></a>Observaciones

El <propertyStore> elemento puede tener uno o más <property> elementos secundarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
