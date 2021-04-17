---
description: El <locationProvider> elemento opcional especifica el proveedor de búsquedas que va a usar el conector de búsqueda del proveedor de servicios Web. Este elemento contiene un atributo obligatorio y un elemento secundario opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705473"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="baa6f-104">Elemento locationProvider (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="baa6f-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="baa6f-105">El <locationProvider> elemento opcional especifica el proveedor de búsquedas que va a usar el conector de búsqueda del proveedor de servicios Web.</span><span class="sxs-lookup"><span data-stu-id="baa6f-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="baa6f-106">Este elemento contiene un atributo obligatorio y un elemento secundario opcional.</span><span class="sxs-lookup"><span data-stu-id="baa6f-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa6f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="baa6f-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="baa6f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="baa6f-108">Element Information</span></span>



| <span data-ttu-id="baa6f-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="baa6f-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="baa6f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="baa6f-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="baa6f-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="baa6f-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="baa6f-112">Elemento propertyBag (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="baa6f-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="baa6f-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="baa6f-113">Attributes</span></span>



| <span data-ttu-id="baa6f-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="baa6f-114">Attribute</span></span> | <span data-ttu-id="baa6f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="baa6f-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="baa6f-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="baa6f-116">Required.</span></span> <span data-ttu-id="baa6f-117">Identificador de clase (CLSID) del proveedor de búsquedas.</span><span class="sxs-lookup"><span data-stu-id="baa6f-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="baa6f-118">codebase</span><span class="sxs-lookup"><span data-stu-id="baa6f-118">codebase</span></span>  | <span data-ttu-id="baa6f-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="baa6f-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="baa6f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="baa6f-120">Remarks</span></span>

<span data-ttu-id="baa6f-121">El @clsid valor de atributo para el proveedor de OpenSearch es {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span><span class="sxs-lookup"><span data-stu-id="baa6f-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="baa6f-122">El sistema de archivos y los conectores de búsqueda basados en el controlador de protocolo pueden usar el [<simpleLocation>](search-schema-sconn-simplelocation.md) elemento en su lugar.</span><span class="sxs-lookup"><span data-stu-id="baa6f-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="baa6f-123">Si <locationProvider> está presente, no debe haber un <simpleLocation> elemento en la descripción del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="baa6f-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="baa6f-124">Ejemplo de un elemento locationProvider</span><span class="sxs-lookup"><span data-stu-id="baa6f-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



