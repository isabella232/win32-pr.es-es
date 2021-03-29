---
description: El <mode> elemento especifica si la dirección URL se debe incluir o excluir del ámbito del conector de búsqueda. Los valores permitidos son include y exclude. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento Mode (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808894"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="c0476-105">Elemento Mode (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="c0476-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="c0476-106">El <mode> elemento especifica si la dirección URL se debe incluir o excluir del ámbito del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c0476-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="c0476-107">Los valores permitidos son `Include` y `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="c0476-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="c0476-108">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="c0476-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0476-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0476-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
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



## <a name="element-information"></a><span data-ttu-id="c0476-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c0476-110">Element Information</span></span>



| <span data-ttu-id="c0476-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c0476-111">Parent Element</span></span>                                                                   | <span data-ttu-id="c0476-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0476-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c0476-113">Elemento scopeItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="c0476-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c0476-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0476-114">Remarks</span></span>

<span data-ttu-id="c0476-115">No se puede buscar ni examinar un ámbito excluido.</span><span class="sxs-lookup"><span data-stu-id="c0476-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="c0476-116">Puede anidar las direcciones URL de scopeItem.</span><span class="sxs-lookup"><span data-stu-id="c0476-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="c0476-117">Por ejemplo, puede incluir un ámbito primario y todos sus elementos secundarios, excepto uno, agregando la dirección URL primaria tal como se incluye, con un valor de profundidad de profundidad y sin incluir la dirección URL secundaria.</span><span class="sxs-lookup"><span data-stu-id="c0476-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="c0476-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0476-118">Example</span></span>

<span data-ttu-id="c0476-119">En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ ExampleFolder y todas sus carpetas secundarias excepto c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="c0476-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



