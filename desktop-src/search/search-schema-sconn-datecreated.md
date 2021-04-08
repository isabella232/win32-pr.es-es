---
description: El <dateCreated> elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda con el estándar ISO 8601. No tiene elementos secundarios ni atributos.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808906"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="96c62-104">Elemento dateCreated (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="96c62-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="96c62-105">El <dateCreated> elemento opcional identifica la fecha y la hora en que se creó este conector de búsqueda con el estándar ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="96c62-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="96c62-106">No tiene elementos secundarios ni atributos.</span><span class="sxs-lookup"><span data-stu-id="96c62-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c62-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96c62-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="96c62-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="96c62-108">Element Information</span></span>



| <span data-ttu-id="96c62-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="96c62-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="96c62-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96c62-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="96c62-111">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="96c62-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="96c62-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96c62-112">Remarks</span></span>

<span data-ttu-id="96c62-113">El formato del valor de este elemento sigue el estándar ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="96c62-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="96c62-114">Un uso común sería cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="96c62-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="96c62-115">\[YYYY \] - \[ mm \] - \[ DD \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05T14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="96c62-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="96c62-116">\[AAAA \] \[ mm \] \[ DD \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405T193030Z")</span><span class="sxs-lookup"><span data-stu-id="96c62-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="96c62-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96c62-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



