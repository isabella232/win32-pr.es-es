---
description: El <scopeItem> elemento representa una única entrada en la tabla de ámbito de inclusión/exclusión.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Elemento scopeItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153933"
---
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="84fdb-103">Elemento scopeItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="84fdb-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="84fdb-104">El <scopeItem> elemento representa una única entrada en la tabla de ámbito de inclusión/exclusión.</span><span class="sxs-lookup"><span data-stu-id="84fdb-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="84fdb-105"><scopeItem> extiende el tipo shellLinkType estándar agregando tres nuevos elementos que controlan la inclusión y exclusión de carpetas, controlan la profundidad de los resultados y especifican la ubicación del ámbito.</span><span class="sxs-lookup"><span data-stu-id="84fdb-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="84fdb-106">Si el <scope> elemento existe, este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84fdb-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="84fdb-107">Tiene tres elementos secundarios y ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="84fdb-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fdb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84fdb-108">Syntax</span></span>


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
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



## <a name="element-information"></a><span data-ttu-id="84fdb-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="84fdb-109">Element Information</span></span>



| <span data-ttu-id="84fdb-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="84fdb-110">Parent Element</span></span>                                                           | <span data-ttu-id="84fdb-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84fdb-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="84fdb-112">Elemento Scope (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="84fdb-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="84fdb-113">[elemento Scope (esquema del conector de búsqueda)](search-schema-sconn-scope-mode.md).</span><span class="sxs-lookup"><span data-stu-id="84fdb-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="84fdb-114">[elemento Scope (esquema del conector de búsqueda)](search-schema-sconn-scope-depth.md).</span><span class="sxs-lookup"><span data-stu-id="84fdb-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="84fdb-115">[elemento URL scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scope-url.md).</span><span class="sxs-lookup"><span data-stu-id="84fdb-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="84fdb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84fdb-116">Remarks</span></span>

<span data-ttu-id="84fdb-117">Use los <scope> <scopeItem> elementos y para identificar las ubicaciones en las que se debe buscar y qué ubicaciones se deben excluir de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84fdb-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="84fdb-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84fdb-118">Example</span></span>

<span data-ttu-id="84fdb-119">En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ ExampleFolder y todas sus carpetas secundarias excepto c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="84fdb-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



