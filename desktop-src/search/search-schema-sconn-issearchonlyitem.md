---
description: El <isSearchOnlyItem> elemento booleano especifica si el proveedor de búsquedas admite el modo de exploración además del modo de búsqueda. Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540630"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="4a8b5-104">Elemento isSearchOnlyItem (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="4a8b5-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="4a8b5-105">El <isSearchOnlyItem> elemento booleano especifica si el proveedor de búsquedas admite el modo de exploración además del modo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4a8b5-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="4a8b5-106">Este elemento es opcional y no tiene ningún elemento secundario y ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="4a8b5-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a8b5-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="4a8b5-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4a8b5-108">Element Information</span></span>



| <span data-ttu-id="4a8b5-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4a8b5-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="4a8b5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a8b5-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="4a8b5-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="4a8b5-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="4a8b5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a8b5-112">Remarks</span></span>

<span data-ttu-id="4a8b5-113">El valor `true` indica que los usuarios no pueden examinar la ubicación del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4a8b5-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="4a8b5-114">El valor `false` indica que los usuarios pueden examinar la ubicación del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4a8b5-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="4a8b5-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a8b5-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



