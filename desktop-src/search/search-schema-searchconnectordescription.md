---
description: El <searchConnectorDescriptionType> elemento es el contenedor de nivel superior para la definición del conector de búsqueda.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696256"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a><span data-ttu-id="ab63f-103">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-103">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>

<span data-ttu-id="ab63f-104">El <searchConnectorDescriptionType> elemento es el contenedor de nivel superior para la definición del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab63f-104">The <searchConnectorDescriptionType> element is the top level container for the search connector definition.</span></span>

-   [<span data-ttu-id="ab63f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab63f-105">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="ab63f-106">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ab63f-106">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ab63f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab63f-107">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="ab63f-108">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="ab63f-108">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ab63f-109">Ejemplo de un archivo de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ab63f-109">Example of a Search Connector Description File</span></span>](#example-of-a-search-connector-description-file)
-   [<span data-ttu-id="ab63f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab63f-110">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="ab63f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab63f-111">Syntax</span></span>


```
<!-- searchConnectorDescriptionType -->
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



## <a name="element-information"></a><span data-ttu-id="ab63f-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ab63f-112">Element Information</span></span>



| <span data-ttu-id="ab63f-113">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ab63f-113">Parent Element</span></span> | <span data-ttu-id="ab63f-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab63f-114">Child Elements</span></span>                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [<span data-ttu-id="ab63f-115">Elemento isSearchOnlyItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-115">isSearchOnlyItem Element (Search Connector Schema)</span></span>](search-schema-sconn-issearchonlyitem.md)                           |
|                | [<span data-ttu-id="ab63f-116">Elemento isDefaultSaveLocation (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-116">isDefaultSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [<span data-ttu-id="ab63f-117">Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-117">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [<span data-ttu-id="ab63f-118">Elemento Description (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-118">description Element (Search Connector Schema)</span></span>](search-schema-sconn-description.md)                                     |
|                | [<span data-ttu-id="ab63f-119">Elemento iconReference (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-119">iconReference Element (Search Connector Schema)</span></span>](search-schema-sconn-iconreference.md)                                 |
|                | [<span data-ttu-id="ab63f-120">Elemento imageLink (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-120">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md)                                         |
|                | [<span data-ttu-id="ab63f-121">Elemento Author (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-121">author Element (Search Connector Schema)</span></span>](search-schema-sconn-author.md)                                               |
|                | [<span data-ttu-id="ab63f-122">Elemento dateCreated (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-122">dateCreated Element (Search Connector Schema)</span></span>](search-schema-sconn-datecreated.md)                                     |
|                | [<span data-ttu-id="ab63f-123">Elemento templateInfo (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-123">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md)                                   |
|                | [<span data-ttu-id="ab63f-124">Elemento locationProvider (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-124">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md)                           |
|                | [<span data-ttu-id="ab63f-125">Elemento Scope (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-125">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md)                                                 |
|                | [<span data-ttu-id="ab63f-126">Elemento propertyStore (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-126">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md)                                 |
|                | [<span data-ttu-id="ab63f-127">Elemento includeInStartMenuScope (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-127">includeInStartMenuScope Element (Search Connector Schema)</span></span>](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [<span data-ttu-id="ab63f-128">Elemento domain (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-128">domain Element (Search Connector Schema)</span></span>](search-schema-sconn-domain.md)                                               |
|                | [<span data-ttu-id="ab63f-129">Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-129">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [<span data-ttu-id="ab63f-130">Elemento isIndexed (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ab63f-130">isIndexed Element (Search Connector Schema)</span></span>](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a><span data-ttu-id="ab63f-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab63f-131">Attributes</span></span>



| <span data-ttu-id="ab63f-132">Atributo</span><span class="sxs-lookup"><span data-stu-id="ab63f-132">Attribute</span></span> | <span data-ttu-id="ab63f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab63f-133">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab63f-134">publisher</span><span class="sxs-lookup"><span data-stu-id="ab63f-134">publisher</span></span> | <span data-ttu-id="ab63f-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab63f-135">Optional.</span></span> <span data-ttu-id="ab63f-136">El nombre para mostrar del publicador que proporciona el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab63f-136">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="ab63f-137">product</span><span class="sxs-lookup"><span data-stu-id="ab63f-137">product</span></span>   | <span data-ttu-id="ab63f-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab63f-138">Optional.</span></span> <span data-ttu-id="ab63f-139">El nombre para mostrar del producto al que se aplica el conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ab63f-139">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab63f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab63f-140">Remarks</span></span>

<span data-ttu-id="ab63f-141">Los conectores de búsqueda para la búsqueda federada no se pueden usar en bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="ab63f-141">Search connectors for federated search cannot be used in libraries.</span></span> <span data-ttu-id="ab63f-142">El esquema de los conectores de búsqueda de biblioteca es una extensión del esquema que se describe aquí e incluye información específica de las bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="ab63f-142">The schema for library search connectors is an extension of the schema described here and includes information specific to libraries.</span></span>

## <a name="example-of-a-search-connector-description-file"></a><span data-ttu-id="ab63f-143">Ejemplo de un archivo de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ab63f-143">Example of a Search Connector Description File</span></span>

<span data-ttu-id="ab63f-144">El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un servicio Web de búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="ab63f-144">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



<span data-ttu-id="ab63f-145">El siguiente es un ejemplo de un archivo de Descripción del conector de búsqueda para un controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab63f-145">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a><span data-ttu-id="ab63f-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab63f-146">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ab63f-147">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ab63f-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab63f-148">Información general sobre el esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ab63f-148">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="ab63f-149">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ab63f-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ab63f-150">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="ab63f-150">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> </dl>

 

 



