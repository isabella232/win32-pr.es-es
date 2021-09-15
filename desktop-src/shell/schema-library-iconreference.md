---
description: El &lt; elemento iconReference &gt; especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.
title: Elemento iconReference (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: db34a387200f3078da08747191242ae7414be410
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579548"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (esquema de biblioteca)

El &lt; elemento iconReference &gt; especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.

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

La referencia de icono debe especificarse en un formulario adecuado para la [**función PathParseIconLocation.**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) Por ejemplo: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

[Elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[elemento name (Esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[elemento version (esquema de biblioteca)](schema-library-version.md)
</dt> </dl>

 

 



