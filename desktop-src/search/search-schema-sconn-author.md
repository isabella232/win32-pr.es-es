---
description: El <author> elemento opcional especifica el autor de esta biblioteca. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Elemento Author (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714995"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="2f46d-104">Elemento Author (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2f46d-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="2f46d-105">El <author> elemento opcional especifica el autor de esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2f46d-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="2f46d-106">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="2f46d-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f46d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f46d-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="2f46d-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2f46d-108">Element Information</span></span>



| <span data-ttu-id="2f46d-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2f46d-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="2f46d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f46d-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2f46d-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="2f46d-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="2f46d-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f46d-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



