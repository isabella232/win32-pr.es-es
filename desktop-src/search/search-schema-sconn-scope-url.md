---
description: El <url> elemento especifica una dirección URL que representa el ámbito del conector de búsqueda. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: scopeItem URL (elemento) (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907737"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="3fd67-104">scopeItem URL (elemento) (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="3fd67-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="3fd67-105">El <url> elemento especifica una dirección URL que representa el ámbito del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3fd67-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="3fd67-106">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="3fd67-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd67-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fd67-107">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="3fd67-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3fd67-108">Element Information</span></span>



| <span data-ttu-id="3fd67-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3fd67-109">Parent Element</span></span>                                                                   | <span data-ttu-id="3fd67-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3fd67-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="3fd67-111">Elemento scopeItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="3fd67-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="3fd67-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fd67-112">Remarks</span></span>

<span data-ttu-id="3fd67-113">El valor puede ser una ruta de acceso del sistema de archivos local o una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="3fd67-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="3fd67-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3fd67-114">Example</span></span>

<span data-ttu-id="3fd67-115">En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ ExampleFolder y todas sus carpetas secundarias excepto c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="3fd67-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



