---
description: Los archivos de descripción de biblioteca son archivos XML que definen bibliotecas.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Esquema de descripción de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5881ad7e97612c93e88708e21a10eeed35e3e443a442ddbb49df7c6f5abe7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049271"
---
# <a name="library-description-schema"></a>Esquema de descripción de biblioteca

Los archivos de descripción de biblioteca son archivos XML que definen bibliotecas. Las bibliotecas agregan elementos de ubicaciones de almacenamiento locales y remotas en una sola vista en Windows Explorer. Los archivos de descripción de biblioteca siguen el esquema Descripción de la biblioteca y se guardan como \* archivos .library-ms.

Este tema contiene las siguientes secciones:

-   [Información general del esquema de descripción de la biblioteca](#overview-of-the-library-description-schema)
-   [Control de versiones del espacio de nombres](#namespace-versioning)
-   [Ejemplo de un archivo de descripción de biblioteca](#example-of-a-library-description-file)
-   [Temas relacionados](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Información general del esquema de descripción de la biblioteca

Las bibliotecas contienen archivos que se almacenan en una o varias ubicaciones de almacenamiento. Las bibliotecas no almacenan realmente estos archivos; en su lugar, supervisan las carpetas que contienen los archivos y permiten a los usuarios acceder y organizar los archivos de maneras diferentes. Por ejemplo, un usuario puede tener archivos de música en varias carpetas en un disco duro local y también en un disco duro externo. Con la **biblioteca Música**, el usuario puede acceder a todos esos archivos al mismo tiempo y ordenarlos todos por nombre de intérprete o título de álbum como un único grupo.

El esquema de descripción de la biblioteca consta de tres partes principales, que se describen en la tabla siguiente:



| Parte                        | Descripción                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Información general de la biblioteca | Información sobre la biblioteca, como el nombre, el propietario, la versión, el icono, que Windows Explorer puede usar cuando muestra la biblioteca a un usuario.                   |
| Propiedades de la biblioteca          | Una o varias propiedades que describen la biblioteca. Estas propiedades personalizadas son específicas de la biblioteca.                                                     |
| Ubicaciones de biblioteca           | Uno o varios conectores de búsqueda que identifican las ubicaciones de almacenamiento que se incluirán en la biblioteca. Cada una de estas ubicaciones también puede tener un conjunto único de propiedades. |



 

Los archivos de biblioteca Windows 7 se almacenan en la carpeta conocida, \_ Bibliotecas FOLDERID. De forma predeterminada, la carpeta Bibliotecas FOLDERID se encuentra en \_ %USERPROFILE% \\ AppData \\ Roaming \\ Microsoft Windows \\ \\ Libraries.

## <a name="namespace-versioning"></a>Control de versiones del espacio de nombres

Se realiza el seguimiento de las versiones del formato de archivo Descripción de la biblioteca \* (.library-ms) cambiando el espacio de nombres . Para Windows 7, el formato de archivo tiene el siguiente espacio de nombres predeterminado: https://schemas.microsoft.com/windows/2009/library .

Sin embargo, se realiza un seguimiento de las versiones del contenido de la biblioteca mediante el [<version>](schema-library-version.md) elemento en un archivo de descripción de biblioteca específico.

## <a name="example-of-a-library-description-file"></a>Ejemplo de un archivo de descripción de biblioteca

A continuación se muestra un ejemplo de un archivo de descripción de biblioteca que define una biblioteca para los archivos de documento.


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

[elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

[elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md)
</dt> <dt>

[elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[elemento name (esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[elemento property (Esquema de biblioteca)](schema-library-property.md)
</dt> <dt>

[elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[elemento version (esquema de biblioteca)](schema-library-version.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
