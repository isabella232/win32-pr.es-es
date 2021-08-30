---
description: El &lt; elemento searchConnectorDescription &gt; es el elemento contenedor de nivel superior de una definición de conector de búsqueda.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: elemento searchConnectorDescription (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eddf7c2795f5c87009bc17b5fa3899d339ceed3c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885971"
---
# <a name="searchconnectordescription-element-library-schema"></a>elemento searchConnectorDescription (esquema de biblioteca)

El &lt; elemento searchConnectorDescription &gt; es el elemento contenedor de nivel superior de una definición de conector de búsqueda. El elemento searchConnectorDescription es una extensión del tipo de elemento &lt; &gt; &lt; searchConnectorDescriptionType asociado a los conectores de búsqueda federada de Windows; sin embargo, no puede incluir conectores de búsqueda para Windows Federated Search o controladores de protocolo en una &gt; biblioteca.

## <a name="syntax"></a>Syntax

``` syntax
<!-- searchConnectorDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```

## <a name="element-information"></a>Información de elemento

Consulte la documentación del esquema en [Windows Search.](/previous-versions/bb268030(v=msdn.10))



| Elemento primario                                                                                               | Elementos secundarios                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md) | <isSearchOnlyI.tem>             |
|                                                                                                              | &lt;description&gt;                   |
|                                                                                                              | &lt;iconReference&gt;                 |
|                                                                                                              | &lt;Imagelink&gt;                     |
|                                                                                                              | &lt;Autor&gt;                        |
|                                                                                                              | &lt;dateCreated&gt;                   |
|                                                                                                              | &lt;templateInfo&gt;                  |
|                                                                                                              | &lt;locationProvider&gt;              |
|                                                                                                              | &lt;scope&gt;                         |
|                                                                                                              | &lt;propertyStore&gt;                 |
|                                                                                                              | &lt;dominio&gt;                        |
|                                                                                                              | &lt;supportsAdvancedQuerySyntax&gt;   |
|                                                                                                              | &lt;isDefaultSaveLocation&gt;         |
|                                                                                                              | &lt;isDefaultNonOwnerSaveLocation&gt; |
|                                                                                                              | &lt;isIndexed&gt;                     |
|                                                                                                              | &lt;simpleLocation&gt;                |
|                                                                                                              | &lt;includeInStartMenu&gt;            |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Opcional. Nombre para mostrar del publicador que proporciona el conector de búsqueda.      |
| product   | Opcional. Nombre para mostrar del producto al que se aplica el conector de búsqueda. |



 

## <a name="remarks"></a>Comentarios

El elemento searchConnectorDescription de una biblioteca usa la misma definición de esquema que &lt; &gt; &lt; searchConnectorDescription &gt; para Windows búsqueda federada. Aunque usan los mismos esquemas, los conectores de búsqueda para Windows búsqueda federada no se pueden incluir en una biblioteca.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Esquema de descripción de biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
