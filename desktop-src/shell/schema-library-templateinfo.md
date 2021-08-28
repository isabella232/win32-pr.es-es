---
description: El elemento templateInfo es un contenedor para el &lt; elemento folderType, que especifica un tipo de carpeta para mostrar los resultados de una consulta &gt; sobre esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55fec64bf7418eef8e70c4cf8fa1ee47006c5f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885531"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (esquema de biblioteca)

El elemento templateInfo es un contenedor para el &lt; elemento &gt; [folderType,](schema-library-foldertype.md) que especifica un tipo de carpeta para mostrar los resultados de una consulta sobre esta biblioteca. Este elemento es opcional y no tiene atributos.

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
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | [Elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)       |
|                                                                              | [elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
