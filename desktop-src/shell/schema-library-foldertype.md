---
description: El <folderType> elemento especifica un GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe; de lo contrario, es opcional. Este elemento no tiene atributos ni elementos secundarios.
title: Elemento folderType (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984590"
---
# <a name="foldertype-element-library-schema"></a>Elemento folderType (esquema de biblioteca)

El <folderType> elemento especifica un GUID para el tipo de carpeta. Este elemento es necesario si el <templateInfo> elemento existe; de lo contrario, es opcional. Este elemento no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Sintaxis


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                           | Elementos secundarios |
|--------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Observaciones

La configuración de un tipo de carpeta determina las columnas y los detalles que aparecen en el explorador de Windows de forma predeterminada. Los identificadores de tipo de carpeta ([**FOLDERTYPEID**](foldertypeid.md)) son GUID definidos en Shlguid. h. En la tabla siguiente se enumeran los GUID de tipos de carpetas comunes.



| Tipo de carpeta      | GUID                                   |
|------------------|----------------------------------------|
| Biblioteca genérica  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Bibliotecas de usuarios  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Carpeta documentos | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Carpeta imágenes  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Carpeta de vídeos    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Carpeta Juegos     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Carpeta música     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Contactos         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md)
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

 

 



