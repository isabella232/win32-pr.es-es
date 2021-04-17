---
description: El <templateInfo> elemento es un contenedor para el elemento folderType, que especifica un tipo de carpeta para mostrar los resultados de una consulta en esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: Elemento templateInfo (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543099"
---
# <a name="templateinfo-element-library-schema"></a>Elemento templateInfo (esquema de biblioteca)

El <templateInfo> elemento es un contenedor para el elemento [folderType](schema-library-foldertype.md) , que especifica un tipo de carpeta para mostrar los resultados de una consulta en esta biblioteca. Este elemento es opcional y no tiene atributos.

## <a name="syntax"></a>Sintaxis

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
|                                                                              | [Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
