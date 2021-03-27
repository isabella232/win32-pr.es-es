---
description: El <iconReference> elemento especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.
title: Elemento iconReference (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997441"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (esquema de biblioteca)

El <iconReference> elemento especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Sintaxis


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Observaciones

La referencia de icono debe especificarse en un formato adecuado para la función [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) . Por ejemplo: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

[Elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Name (elemento, esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[Elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[version (elemento, esquema de biblioteca)](schema-library-version.md)
</dt> </dl>

 

 



