---
description: Los archivos de descripción de la biblioteca son archivos XML que definen las bibliotecas.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Esquema de descripción de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104986191"
---
# <a name="library-description-schema"></a>Esquema de descripción de biblioteca

Los archivos de descripción de la biblioteca son archivos XML que definen las bibliotecas. Las bibliotecas agregan elementos de las ubicaciones de almacenamiento local y remoto a una sola vista en el explorador de Windows. Los archivos de descripción de la biblioteca siguen el esquema de descripción de la biblioteca y se guardan como \* . Library-MS files.

Este tema contiene las siguientes secciones:

-   [Información general sobre el esquema de descripción de la biblioteca](#overview-of-the-library-description-schema)
-   [Control de versiones del espacio de nombres](#namespace-versioning)
-   [Ejemplo de un archivo de descripción de biblioteca](#example-of-a-library-description-file)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Información general sobre el esquema de descripción de la biblioteca

Las bibliotecas contienen archivos que se almacenan en una o varias ubicaciones de almacenamiento. En realidad, las bibliotecas no almacenan estos archivos; en su lugar, supervisan las carpetas que contienen los archivos y permiten a los usuarios tener acceso a los archivos y organizarlos de diferentes maneras. Por ejemplo, un usuario puede tener archivos de música en varias carpetas de un disco duro local y también en un disco duro externo. Con la **biblioteca de música**, el usuario puede tener acceso a todos los archivos al mismo tiempo y ordenarlos por nombre de intérprete o título de álbum como un solo grupo.

El esquema de descripción de la biblioteca consta de tres partes principales, que se describen en la tabla siguiente:



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Información general de la biblioteca | Información acerca de la biblioteca, como el nombre, el propietario, la versión, el icono que puede usar el explorador de Windows cuando muestra la biblioteca a un usuario.                   |
| Propiedades de la biblioteca          | Una o más propiedades que describen la biblioteca. Estas propiedades personalizadas son específicas de la biblioteca.                                                     |
| Ubicaciones de biblioteca           | Uno o más conectores de búsqueda que identifican las ubicaciones de almacenamiento que se van a incluir en la biblioteca. Cada una de estas ubicaciones también puede tener un conjunto de propiedades único. |



 

Los archivos de biblioteca de Windows 7 se almacenan en la carpeta conocida, FOLDERID \_ Libraries. De forma predeterminada, la \_ carpeta bibliotecas FOLDERID se encuentra en% userprofile% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ Libraries.

## <a name="namespace-versioning"></a>Control de versiones del espacio de nombres

Se realiza un seguimiento de las versiones del formato de archivo de descripción de la biblioteca ( \* . Library-MS) cambiando el espacio de nombres. En Windows 7, el formato de archivo tiene el siguiente espacio de nombres predeterminado: https://schemas.microsoft.com/windows/2009/library .

No obstante, se realiza un seguimiento de las versiones del contenido de la biblioteca mediante el [<version>](schema-library-version.md) elemento de un archivo de descripción de biblioteca específico.

## <a name="example-of-a-library-description-file"></a>Ejemplo de un archivo de descripción de biblioteca

El siguiente es un ejemplo de un archivo de descripción de biblioteca que define una biblioteca para los archivos de documento.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

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

[Property (elemento, esquema de biblioteca)](schema-library-property.md)
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
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
