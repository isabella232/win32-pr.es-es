---
description: El &lt; elemento version especifica la versión de contenido de esta &gt; biblioteca. Este elemento no tiene atributos ni elementos secundarios.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: elemento version (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1aeac399b5fa71b4a1ca57b63d8ecb95ede57f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885461"
---
# <a name="version-element-library-schema"></a>elemento version (esquema de biblioteca)

El &lt; elemento version especifica la versión de contenido de esta &gt; biblioteca. Este elemento no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | None           |



 

## <a name="remarks"></a>Observaciones

La versión de contenido de la biblioteca es diferente de la versión de formato de archivo de la \* biblioteca (.library-ms). La versión de formato de archivo de la biblioteca se especifica en el espacio de [nombres](library-schema-entry.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
