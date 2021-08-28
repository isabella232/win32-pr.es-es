---
description: El &lt; elemento folderType &gt; especifica un GUID para el tipo de carpeta. Este elemento es necesario si existe el &lt; elemento &gt; templateInfo; de lo contrario, es opcional. Este elemento no tiene atributos ni elementos secundarios.
title: Elemento folderType (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba9d0163a00ab525fb0a52267c1226b6a48230a4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880871"
---
# <a name="foldertype-element-library-schema"></a>Elemento folderType (esquema de biblioteca)

El &lt; elemento folderType &gt; especifica un GUID para el tipo de carpeta. Este elemento es necesario si existe el &lt; elemento &gt; templateInfo; de lo contrario, es opcional. Este elemento no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax


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



 

## <a name="remarks"></a>Comentarios

Establecer un tipo de carpeta determina las columnas y los detalles que aparecen en Windows Explorer de forma predeterminada. Los identificadores de tipo de carpeta [**(FOLDERTYPEID)**](foldertypeid.md)son GUID definidos en Shlguid.h. En la tabla siguiente se enumeran los GUID de los tipos de carpeta comunes.



| Tipo de carpeta      | GUID                                   |
|------------------|----------------------------------------|
| Biblioteca genérica  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Bibliotecas de usuarios  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Carpeta Documentos | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Carpeta Imágenes  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Carpeta Vídeos    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Carpeta Juegos     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Música Carpeta     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Contactos         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md)
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

 

 



