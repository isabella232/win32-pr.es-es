---
description: El elemento booleano opcional <isIndexed> especifica si la ubicación descrita por el conector de búsqueda está indizada (ya sea de forma local o remota mediante Windows Search 4 o superior).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento isIndexed (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153935"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="2a1f7-103">Elemento isIndexed (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2a1f7-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="2a1f7-104">El elemento booleano opcional <isIndexed> especifica si la ubicación descrita por el conector de búsqueda está indizada (ya sea de forma local o remota mediante Windows Search 4 o superior).</span><span class="sxs-lookup"><span data-stu-id="2a1f7-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="2a1f7-105">El valor predeterminado es true para las carpetas locales.</span><span class="sxs-lookup"><span data-stu-id="2a1f7-105">The default value is true for local folders.</span></span> <span data-ttu-id="2a1f7-106">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2a1f7-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a1f7-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="2a1f7-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2a1f7-108">Element Information</span></span>



| <span data-ttu-id="2a1f7-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2a1f7-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="2a1f7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a1f7-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2a1f7-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2a1f7-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="2a1f7-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a1f7-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



