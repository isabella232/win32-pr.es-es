---
description: El <version> elemento especifica la versión de contenido de esta biblioteca. Este elemento no tiene atributos ni elementos secundarios.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: version (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984583"
---
# <a name="version-element-library-schema"></a>version (elemento, esquema de biblioteca)

El <version> elemento especifica la versión de contenido de esta biblioteca. Este elemento no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Sintaxis

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | Ninguno           |



 

## <a name="remarks"></a>Observaciones

La versión de contenido de la biblioteca es diferente de la versión de formato de archivo ( \* . Library-MS) de la biblioteca. La versión de formato de archivo de la biblioteca se especifica en el [espacio de nombres](library-schema-entry.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
