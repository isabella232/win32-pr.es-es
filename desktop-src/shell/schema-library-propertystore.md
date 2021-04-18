---
description: El <propertyStore> elemento especifica un conjunto de una o varias propiedades utilizadas por esta biblioteca. Este elemento es opcional y no tiene atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985819"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="f135d-104">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="f135d-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="f135d-105">El <propertyStore> elemento especifica un conjunto de una o varias propiedades utilizadas por esta biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f135d-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="f135d-106">Este elemento es opcional y no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="f135d-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f135d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f135d-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="f135d-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f135d-108">Element Information</span></span>



| <span data-ttu-id="f135d-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="f135d-109">Parent Element</span></span>                                                               | <span data-ttu-id="f135d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f135d-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f135d-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="f135d-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="f135d-112">Property (elemento, esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="f135d-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="f135d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f135d-113">Remarks</span></span>

<span data-ttu-id="f135d-114">El <propertyStore> elemento puede tener uno o más <property> elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f135d-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f135d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f135d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f135d-116">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="f135d-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="f135d-117">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="f135d-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
