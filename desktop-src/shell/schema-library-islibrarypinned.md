---
description: El <isLibraryPinned> elemento especifica si esta biblioteca está anclada al panel de navegación en el explorador de Windows. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.
title: Elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 743ddc6df6b4a1a0df44e19bf063e417fc052e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997957"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (esquema de biblioteca)

El <isLibraryPinned> elemento especifica si esta biblioteca está anclada al panel de navegación en el explorador de Windows. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.

## <a name="syntax"></a>Sintaxis


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Observaciones

Si es true, la biblioteca está anclada al panel de navegación del explorador de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



