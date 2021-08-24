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
ms.openlocfilehash: 84e200fa4969dc376661bd32851296d80c74120939afc995754cb2937ea04be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820235"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (esquema de biblioteca)

El <iconReference> elemento especifica un icono personalizado para esta biblioteca. Este elemento es opcional y no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentarios

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

 

 



