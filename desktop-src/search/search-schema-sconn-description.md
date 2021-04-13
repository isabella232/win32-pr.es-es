---
description: El parámetro opcional <description> elemento especifica una descripción para este conector de búsqueda. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Elemento Description (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360183"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="85e59-105">Elemento Description (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="85e59-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="85e59-106">El parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="85e59-106">The optional</span></span> <description> <span data-ttu-id="85e59-107">elemento especifica una descripción para este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="85e59-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="85e59-108">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="85e59-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e59-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85e59-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="85e59-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="85e59-110">Element Information</span></span>



| <span data-ttu-id="85e59-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="85e59-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="85e59-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85e59-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="85e59-113">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="85e59-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="85e59-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85e59-114">Remarks</span></span>

<span data-ttu-id="85e59-115">La descripción debe ser fácil de usar, ya que se puede utilizar en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="85e59-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="85e59-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85e59-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



