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
# <a name="librarydescription-element-library-schema"></a>Elemento libraryDescription (esquema de biblioteca)

El <libraryDescription> elemento es el contenedor de nivel superior de la definición de la biblioteca. Este elemento es obligatorio.

## <a name="syntax"></a>Sintaxis


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



## <a name="element-information"></a>Información de elemento



| Elemento primario | Elementos secundarios                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [Name (elemento) (esquema de biblioteca)](schema-library-name.md). Obligatorio.                                                     |
|                | [elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md). Opcional.                                             |
|                | [elemento version (esquema de biblioteca)](schema-library-version.md). Opcional.                                               |
|                | [elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md). Opcional.                               |
|                | [elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md). Opcional.                                   |
|                | [elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md). Opcional.                                   |
|                | [elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md). Opcional.                                     |
|                | [elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md). Obligatorio. |



 

## <a name="remarks"></a>Observaciones

Cada biblioteca puede contener una o varias ubicaciones que un usuario puede examinar o buscar mediante el explorador de Windows. Los conectores de búsqueda definen las ubicaciones mediante [<searchConnectorDescription>](schema-library-searchconnectordescription.md) los elementos de un [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) elemento contenedor.

Una biblioteca puede tener un conjunto único de propiedades, y las ubicaciones de la biblioteca también pueden tener conjuntos únicos de propiedades. Estas propiedades se definen en [<property>](schema-library-property.md) elementos dentro de un [<propertyStore>](schema-library-propertystore.md) elemento contenedor.

## <a name="example"></a>Ejemplo


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

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
