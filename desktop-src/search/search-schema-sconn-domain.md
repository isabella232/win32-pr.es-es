---
description: El <domain> elemento opcional especifica la dirección URL del servicio de búsqueda que usa este conector de búsqueda. Se muestra en el panel de detalles. Este elemento no tiene ningún elemento secundario y no tiene atributos.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento domain (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907739"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="14c09-105">Elemento domain (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="14c09-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="14c09-106">El <domain> elemento opcional especifica la dirección URL del servicio de búsqueda que usa este conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="14c09-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="14c09-107">Se muestra en el panel de detalles.</span><span class="sxs-lookup"><span data-stu-id="14c09-107">It is displayed in the details pane.</span></span> <span data-ttu-id="14c09-108">Este elemento no tiene ningún elemento secundario y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="14c09-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c09-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14c09-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="14c09-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="14c09-110">Element Information</span></span>



| <span data-ttu-id="14c09-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="14c09-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="14c09-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14c09-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="14c09-113">Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="14c09-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="14c09-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14c09-114">Remarks</span></span>

<span data-ttu-id="14c09-115">La dirección URL debe ser el dominio de nivel superior del proveedor de búsquedas.</span><span class="sxs-lookup"><span data-stu-id="14c09-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="14c09-116">Por ejemplo, https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="14c09-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="14c09-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14c09-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



