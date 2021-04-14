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
# <a name="library-description-schema"></a><span data-ttu-id="9b064-103">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-103">Library Description Schema</span></span>

<span data-ttu-id="9b064-104">Los archivos de descripción de la biblioteca son archivos XML que definen las bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9b064-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="9b064-105">Las bibliotecas agregan elementos de las ubicaciones de almacenamiento local y remoto a una sola vista en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="9b064-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="9b064-106">Los archivos de descripción de la biblioteca siguen el esquema de descripción de la biblioteca y se guardan como \* . Library-MS files.</span><span class="sxs-lookup"><span data-stu-id="9b064-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="9b064-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="9b064-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9b064-108">Información general sobre el esquema de descripción de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="9b064-109">Control de versiones del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b064-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="9b064-110">Ejemplo de un archivo de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="9b064-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b064-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="9b064-112">Información general sobre el esquema de descripción de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="9b064-113">Las bibliotecas contienen archivos que se almacenan en una o varias ubicaciones de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="9b064-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="9b064-114">En realidad, las bibliotecas no almacenan estos archivos; en su lugar, supervisan las carpetas que contienen los archivos y permiten a los usuarios tener acceso a los archivos y organizarlos de diferentes maneras.</span><span class="sxs-lookup"><span data-stu-id="9b064-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="9b064-115">Por ejemplo, un usuario puede tener archivos de música en varias carpetas de un disco duro local y también en un disco duro externo.</span><span class="sxs-lookup"><span data-stu-id="9b064-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="9b064-116">Con la **biblioteca de música**, el usuario puede tener acceso a todos los archivos al mismo tiempo y ordenarlos por nombre de intérprete o título de álbum como un solo grupo.</span><span class="sxs-lookup"><span data-stu-id="9b064-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="9b064-117">El esquema de descripción de la biblioteca consta de tres partes principales, que se describen en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="9b064-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b064-118">Información general de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-118">General library information</span></span> | <span data-ttu-id="9b064-119">Información acerca de la biblioteca, como el nombre, el propietario, la versión, el icono que puede usar el explorador de Windows cuando muestra la biblioteca a un usuario.</span><span class="sxs-lookup"><span data-stu-id="9b064-119">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="9b064-120">Propiedades de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-120">Library properties</span></span>          | <span data-ttu-id="9b064-121">Una o más propiedades que describen la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b064-121">One or more properties that describe the library.</span></span> <span data-ttu-id="9b064-122">Estas propiedades personalizadas son específicas de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b064-122">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="9b064-123">Ubicaciones de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-123">Library locations</span></span>           | <span data-ttu-id="9b064-124">Uno o más conectores de búsqueda que identifican las ubicaciones de almacenamiento que se van a incluir en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b064-124">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="9b064-125">Cada una de estas ubicaciones también puede tener un conjunto de propiedades único.</span><span class="sxs-lookup"><span data-stu-id="9b064-125">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="9b064-126">Los archivos de biblioteca de Windows 7 se almacenan en la carpeta conocida, FOLDERID \_ Libraries.</span><span class="sxs-lookup"><span data-stu-id="9b064-126">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="9b064-127">De forma predeterminada, la \_ carpeta bibliotecas FOLDERID se encuentra en% userprofile% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ Libraries.</span><span class="sxs-lookup"><span data-stu-id="9b064-127">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="9b064-128">Control de versiones del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b064-128">Namespace Versioning</span></span>

<span data-ttu-id="9b064-129">Se realiza un seguimiento de las versiones del formato de archivo de descripción de la biblioteca ( \* . Library-MS) cambiando el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9b064-129">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="9b064-130">En Windows 7, el formato de archivo tiene el siguiente espacio de nombres predeterminado: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="9b064-130">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="9b064-131">No obstante, se realiza un seguimiento de las versiones del contenido de la biblioteca mediante el [<version>](schema-library-version.md) elemento de un archivo de descripción de biblioteca específico.</span><span class="sxs-lookup"><span data-stu-id="9b064-131">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="9b064-132">Ejemplo de un archivo de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b064-132">Example of a Library Description File</span></span>

<span data-ttu-id="9b064-133">El siguiente es un ejemplo de un archivo de descripción de biblioteca que define una biblioteca para los archivos de documento.</span><span class="sxs-lookup"><span data-stu-id="9b064-133">The following is an example of a Library Description file that defines a library for document files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9b064-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b064-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b064-135">Elemento folderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-135">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="9b064-136">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-136">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="9b064-137">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-137">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="9b064-138">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-138">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="9b064-139">Name (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-139">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="9b064-140">Elemento ownerSID (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-140">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="9b064-141">Property (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-141">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="9b064-142">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="9b064-143">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="9b064-144">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="9b064-145">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="9b064-146">version (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9b064-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="9b064-147">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9b064-147">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
