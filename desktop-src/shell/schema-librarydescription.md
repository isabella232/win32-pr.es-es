---
description: El <libraryDescription> elemento es el contenedor de nivel superior de la definición de la biblioteca. Este elemento es obligatorio.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Elemento libraryDescription (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984582"
---
# <a name="librarydescription-element-library-schema"></a><span data-ttu-id="8770f-104">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8770f-104">libraryDescription Element (Library Schema)</span></span>

<span data-ttu-id="8770f-105">El <libraryDescription> elemento es el contenedor de nivel superior de la definición de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8770f-105">The <libraryDescription> element is the top-level container for the library definition.</span></span> <span data-ttu-id="8770f-106">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8770f-106">This element is required.</span></span>

## <a name="syntax"></a><span data-ttu-id="8770f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8770f-107">Syntax</span></span>


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a><span data-ttu-id="8770f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8770f-108">Element Information</span></span>



| <span data-ttu-id="8770f-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="8770f-109">Parent element</span></span> | <span data-ttu-id="8770f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8770f-110">Child elements</span></span>                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | <span data-ttu-id="8770f-111">[Name (elemento) (esquema de biblioteca)](schema-library-name.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-111">[name Element (Library Schema)](schema-library-name.md).</span></span> <span data-ttu-id="8770f-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8770f-112">Required.</span></span>                                                     |
|                | <span data-ttu-id="8770f-113">[elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-113">[ownerSID Element (Library Schema)](schema-library-ownersid.md).</span></span> <span data-ttu-id="8770f-114">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-114">Optional.</span></span>                                             |
|                | <span data-ttu-id="8770f-115">[elemento version (esquema de biblioteca)](schema-library-version.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-115">[version Element (Library Schema)](schema-library-version.md).</span></span> <span data-ttu-id="8770f-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-116">Optional.</span></span>                                               |
|                | <span data-ttu-id="8770f-117">[elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-117">[isLibraryPinned Element (Library Schema)](schema-library-islibrarypinned.md).</span></span> <span data-ttu-id="8770f-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-118">Optional.</span></span>                               |
|                | <span data-ttu-id="8770f-119">[elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-119">[iconReference Element (Library Schema)](schema-library-iconreference.md).</span></span> <span data-ttu-id="8770f-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-120">Optional.</span></span>                                   |
|                | <span data-ttu-id="8770f-121">[elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-121">[propertyStore Element (Library Schema)](schema-library-propertystore.md).</span></span> <span data-ttu-id="8770f-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-122">Optional.</span></span>                                   |
|                | <span data-ttu-id="8770f-123">[elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-123">[templateInfo Element (Library Schema)](schema-library-templateinfo.md).</span></span> <span data-ttu-id="8770f-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8770f-124">Optional.</span></span>                                     |
|                | <span data-ttu-id="8770f-125">[elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md).</span><span class="sxs-lookup"><span data-stu-id="8770f-125">[searchConnectorDescriptionList Element (Library Schema)](schema-library-searchconnectordescriptionlist.md).</span></span> <span data-ttu-id="8770f-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8770f-126">Required.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8770f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8770f-127">Remarks</span></span>

<span data-ttu-id="8770f-128">Cada biblioteca puede contener una o varias ubicaciones que un usuario puede examinar o buscar mediante el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="8770f-128">Each library can contain one or more locations that can be browsed or searched by a user using Windows Explorer.</span></span> <span data-ttu-id="8770f-129">Los conectores de búsqueda definen las ubicaciones mediante [<searchConnectorDescription>](schema-library-searchconnectordescription.md) los elementos de un [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) elemento contenedor.</span><span class="sxs-lookup"><span data-stu-id="8770f-129">The locations are defined by search connectors using [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elements in a [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) container element.</span></span>

<span data-ttu-id="8770f-130">Una biblioteca puede tener un conjunto único de propiedades, y las ubicaciones de la biblioteca también pueden tener conjuntos únicos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8770f-130">A library can have a unique set of properties, and locations in the library can also have unique sets of properties.</span></span> <span data-ttu-id="8770f-131">Estas propiedades se definen en [<property>](schema-library-property.md) elementos dentro de un [<propertyStore>](schema-library-propertystore.md) elemento contenedor.</span><span class="sxs-lookup"><span data-stu-id="8770f-131">These properties are defined in [<property>](schema-library-property.md) elements within a [<propertyStore>](schema-library-propertystore.md) container element.</span></span>

## <a name="example"></a><span data-ttu-id="8770f-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8770f-132">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8770f-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8770f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8770f-134">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="8770f-134">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="8770f-135">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8770f-135">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
