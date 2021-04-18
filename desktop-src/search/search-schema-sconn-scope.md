---
description: El <scope> elemento opcional especifica una colección de <scopeItem> elementos que definen las inclusiones y exclusiones del ámbito de este conector de búsqueda concreto.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento Scope (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696261"
---
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="ccd5e-103">Elemento Scope (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ccd5e-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="ccd5e-104">El <scope> elemento opcional especifica una colección de <scopeItem> elementos que definen las inclusiones y exclusiones del ámbito de este conector de búsqueda concreto.</span><span class="sxs-lookup"><span data-stu-id="ccd5e-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="ccd5e-105">Si <scope> está presente, debe contener al menos un <scopeItem> elemento.</span><span class="sxs-lookup"><span data-stu-id="ccd5e-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="ccd5e-106">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="ccd5e-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccd5e-107">Syntax</span></span>


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="ccd5e-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ccd5e-108">Element Information</span></span>



| <span data-ttu-id="ccd5e-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ccd5e-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="ccd5e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccd5e-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ccd5e-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="ccd5e-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="ccd5e-112">[elemento scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scopeitem.md).</span><span class="sxs-lookup"><span data-stu-id="ccd5e-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ccd5e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccd5e-113">Remarks</span></span>

<span data-ttu-id="ccd5e-114">Use los <scope> <scopeItem> elementos y para identificar las ubicaciones en las que se debe buscar y qué ubicaciones se deben excluir de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ccd5e-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="ccd5e-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccd5e-115">Example</span></span>

<span data-ttu-id="ccd5e-116">En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ ExampleFolder y todas sus carpetas secundarias excepto c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="ccd5e-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



