---
description: El <isLibraryPinned> elemento especifica si esta biblioteca está anclada al panel de navegación en Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.
title: Elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8b5fe37b2a9b31708c1b6a49bd22745b37af8fa8ec21b0b424b7c6da3baaae53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592865"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (esquema de biblioteca)

El <isLibraryPinned> elemento especifica si esta biblioteca está anclada al panel de navegación en Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.

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

 

 



