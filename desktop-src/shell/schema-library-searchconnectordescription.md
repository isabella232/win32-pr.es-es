---
description: El <searchConnectorDescription> elemento es el elemento contenedor de nivel superior de una definición de conector de búsqueda.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Elemento searchConnectorDescription (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985895"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="9a1c6-103">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9a1c6-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="9a1c6-104">El <searchConnectorDescription> elemento es el elemento contenedor de nivel superior de una definición de conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="9a1c6-105">El <searchConnectorDescription> elemento es una extensión del <searchConnectorDescriptionType> tipo de elemento asociado con los conectores de búsqueda federada de Windows; sin embargo, no puede incluir conectores de búsqueda para los controladores de protocolo o de búsqueda federada de Windows en una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1c6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a1c6-106">Syntax</span></span>

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

## <a name="element-information"></a><span data-ttu-id="9a1c6-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9a1c6-107">Element Information</span></span>

<span data-ttu-id="9a1c6-108">Consulte la documentación del esquema en [Windows Search](/previous-versions/bb268030(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a1c6-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="9a1c6-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="9a1c6-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="9a1c6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9a1c6-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="9a1c6-111">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="9a1c6-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="9a1c6-112"><isSearchOnlyI. TEM></span><span class="sxs-lookup"><span data-stu-id="9a1c6-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="9a1c6-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a1c6-113">Attributes</span></span>



| <span data-ttu-id="9a1c6-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="9a1c6-114">Attribute</span></span> | <span data-ttu-id="9a1c6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a1c6-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9a1c6-116">publisher</span><span class="sxs-lookup"><span data-stu-id="9a1c6-116">publisher</span></span> | <span data-ttu-id="9a1c6-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-117">Optional.</span></span> <span data-ttu-id="9a1c6-118">El nombre para mostrar del publicador que proporciona el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="9a1c6-119">product</span><span class="sxs-lookup"><span data-stu-id="9a1c6-119">product</span></span>   | <span data-ttu-id="9a1c6-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-120">Optional.</span></span> <span data-ttu-id="9a1c6-121">El nombre para mostrar del producto al que se aplica el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a1c6-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a1c6-122">Remarks</span></span>

<span data-ttu-id="9a1c6-123">El <searchConnectorDescription> elemento de una biblioteca usa la misma definición de esquema que <searchConnectorDescription> para la búsqueda federada de Windows.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="9a1c6-124">Aunque utilizan los mismos esquemas, los conectores de búsqueda para la búsqueda federada de Windows no se pueden incluir en una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9a1c6-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a1c6-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a1c6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a1c6-126">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a1c6-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="9a1c6-127">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="9a1c6-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
