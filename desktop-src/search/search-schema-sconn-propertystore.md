---
description: El <propertyStore> elemento opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos para este conector de búsqueda. Este elemento no tiene atributos y solo un elemento secundario.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808899"
---
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="0136c-104">Elemento propertyStore (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="0136c-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="0136c-105">El <propertyStore> elemento opcional especifica la ubicación de un IPropertyStore basado en XML para almacenar los metadatos abiertos para este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0136c-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="0136c-106">Este elemento no tiene atributos y solo un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="0136c-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="0136c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0136c-107">Syntax</span></span>


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="0136c-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0136c-108">Element Information</span></span>



| <span data-ttu-id="0136c-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="0136c-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="0136c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0136c-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0136c-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="0136c-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="0136c-112">Elemento Property de propertyStore (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="0136c-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="0136c-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0136c-113">Example</span></span>

<span data-ttu-id="0136c-114">En el ejemplo siguiente se muestra un <propertyStore> elemento con dos <property> elementos.</span><span class="sxs-lookup"><span data-stu-id="0136c-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



