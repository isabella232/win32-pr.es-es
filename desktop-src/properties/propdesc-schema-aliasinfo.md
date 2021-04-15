---
description: Especifica un alias de ordenación o una lista de alias de ordenación mediante la especificación de un elemento que contiene una propiedad de ordenación o una lista de propiedades de ordenación.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715769"
---
# <a name="aliasinfo"></a><span data-ttu-id="0ff3a-103">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="0ff3a-103">aliasInfo</span></span>

<span data-ttu-id="0ff3a-104">Especifica un alias de ordenación o una lista de alias de ordenación mediante la especificación de un elemento que contiene una propiedad de ordenación o una lista de propiedades de ordenación.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-104">Specifies a sort alias or list of sort aliases by specifying an element that contains a sort property or list of sort properties.</span></span> <span data-ttu-id="0ff3a-105">Solo debe haber un elemento [aliasInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff3a-105">There should be only one [aliasInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span> <span data-ttu-id="0ff3a-106">En el caso de las propiedades que establecen canGroupBy = true, a menos que se especifique una propiedad de ordenación secundaria ( aliasInfo/@additionalSortByAliases = prop: example), el usuario puede experimentar un comportamiento inesperado al cambiar el criterio de ordenación en una vista que está agrupada por la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-106">For properties that set canGroupBy=true, unless a secondary sort property is specified (aliasInfo/@additionalSortByAliases=prop:example), the user may experience unexpected behavior when changing the sort order in a view that is grouped by the property.</span></span> <span data-ttu-id="0ff3a-107">En concreto, el orden de los grupos cambiará, pero el orden de los elementos dentro de los grupos no lo hará.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-107">Specifically, the order of the groups will change, but the order of items within the groups will not.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff3a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ff3a-108">Syntax</span></span>


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0ff3a-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0ff3a-109">Element Information</span></span>



| <span data-ttu-id="0ff3a-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="0ff3a-110">Parent Element</span></span>                                                   | <span data-ttu-id="0ff3a-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ff3a-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="0ff3a-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0ff3a-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="0ff3a-113">None</span><span class="sxs-lookup"><span data-stu-id="0ff3a-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0ff3a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ff3a-114">Attributes</span></span>



| <span data-ttu-id="0ff3a-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="0ff3a-115">Attribute</span></span>               | <span data-ttu-id="0ff3a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ff3a-116">Description</span></span>                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff3a-117">sortByAlias</span><span class="sxs-lookup"><span data-stu-id="0ff3a-117">sortByAlias</span></span>             | <span data-ttu-id="0ff3a-118">Público.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-118">Public.</span></span> <span data-ttu-id="0ff3a-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-119">Optional.</span></span> <span data-ttu-id="0ff3a-120">Nombre canónico de la propiedad que se debe usar para ordenar por.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-120">The canonical name of the property that should be used to sort by.</span></span> <span data-ttu-id="0ff3a-121">Esta cadena es de tipo canónico-Type.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-121">This string is of type canonical-type.</span></span>                                            |
| <span data-ttu-id="0ff3a-122">additionalSortByAliases</span><span class="sxs-lookup"><span data-stu-id="0ff3a-122">additionalSortByAliases</span></span> | <span data-ttu-id="0ff3a-123">Público.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-123">Public.</span></span> <span data-ttu-id="0ff3a-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-124">Optional.</span></span> <span data-ttu-id="0ff3a-125">Una lista delimitada por punto y coma de propiedades adicionales que se usarán al ordenar.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-125">A semi-colon delimited list of additional properties to be used when sorting.</span></span> <span data-ttu-id="0ff3a-126">Las propiedades se aplican a la ordenación en la secuencia en la que se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="0ff3a-126">The properties are applied to the sort in the sequence they are given.</span></span> |



 

 

 
