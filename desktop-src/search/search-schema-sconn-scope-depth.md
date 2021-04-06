---
description: El <depth> elemento especifica si el ámbito del conector de búsqueda debe incluir direcciones URL secundarias. Los valores permitidos son Deep y Shallow. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Depth (elemento) (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000994"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="7cfc5-105">Depth (elemento) (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="7cfc5-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="7cfc5-106">El <depth> elemento especifica si el ámbito del conector de búsqueda debe incluir direcciones URL secundarias.</span><span class="sxs-lookup"><span data-stu-id="7cfc5-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="7cfc5-107">Los valores permitidos son `Deep` y `Shallow`.</span><span class="sxs-lookup"><span data-stu-id="7cfc5-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="7cfc5-108">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="7cfc5-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cfc5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cfc5-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="7cfc5-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7cfc5-110">Element Information</span></span>



| <span data-ttu-id="7cfc5-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7cfc5-111">Parent Element</span></span>                                                                   | <span data-ttu-id="7cfc5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cfc5-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7cfc5-113">Elemento scopeItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="7cfc5-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="7cfc5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cfc5-114">Remarks</span></span>

<span data-ttu-id="7cfc5-115">Si la profundidad es profunda, los usuarios pueden examinar o buscar elementos en el nivel de dirección URL de scopeItem o en cualquier dirección URL secundaria.</span><span class="sxs-lookup"><span data-stu-id="7cfc5-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="7cfc5-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7cfc5-116">Example</span></span>

<span data-ttu-id="7cfc5-117">En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: \\ FolderA y todas sus carpetas secundarias y c: \\ FolderB, pero ninguna de sus carpetas secundarias.</span><span class="sxs-lookup"><span data-stu-id="7cfc5-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



