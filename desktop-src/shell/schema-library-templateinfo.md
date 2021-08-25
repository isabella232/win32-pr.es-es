---
description: El elemento es un contenedor para el elemento folderType, que especifica un tipo de carpeta para mostrar los resultados de una <templateInfo> consulta sobre esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda0c42e71db2e47335371b51d9dc819620e6b28dfac63ee9c0e2a640ccab0b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942095"
---
# <a name="templateinfo-element-library-schema"></a>elemento templateInfo (esquema de biblioteca)

El <templateInfo> elemento es un contenedor para el elemento [folderType,](schema-library-foldertype.md) que especifica un tipo de carpeta para mostrar los resultados de una consulta sobre esta biblioteca. Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Syntax

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)       |
|                                                                              | [elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
