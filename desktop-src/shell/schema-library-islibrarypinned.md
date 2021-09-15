---
description: El &lt; elemento isLibraryPinned especifica si esta biblioteca está anclada al panel de &gt; navegación de Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.
title: elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a535619fd38a0a557546f97f0a6ace64a065b61c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579545"
---
# <a name="islibrarypinned-element-library-schema"></a>elemento isLibraryPinned (esquema de biblioteca)

El &lt; elemento isLibraryPinned especifica si esta biblioteca está anclada al panel de &gt; navegación de Windows Explorer. Este elemento es opcional y no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Sintaxis


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Observaciones

Si es true, la biblioteca se ancla al panel de navegación Windows explorador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



