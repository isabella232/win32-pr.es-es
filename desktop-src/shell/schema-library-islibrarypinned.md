---
description: El &lt; elemento isLibraryPinned especifica si esta biblioteca está anclada al panel de &gt; navegación en Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.
title: Elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a535619fd38a0a557546f97f0a6ace64a065b61c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885641"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (esquema de biblioteca)

El &lt; elemento isLibraryPinned especifica si esta biblioteca está anclada al panel de &gt; navegación en Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentarios

Si es true, la biblioteca se ancla al panel de navegación Windows Explorer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



