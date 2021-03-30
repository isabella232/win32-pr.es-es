---
description: Novedades de Windows 7. Identifica una propiedad que está relacionada con la propiedad definida en el archivo de descripción de la propiedad.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360559"
---
# <a name="relatedproperty"></a><span data-ttu-id="c0bd9-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="c0bd9-104">relatedProperty</span></span>

<span data-ttu-id="c0bd9-105">Novedades de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-105">New for Windows 7.</span></span> <span data-ttu-id="c0bd9-106">Identifica una propiedad que está relacionada con la propiedad definida en el archivo de descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="c0bd9-107">Puede haber tantos elementos [relatedProperty]() dentro de un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0bd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0bd9-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="c0bd9-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c0bd9-109">Element Information</span></span>



| <span data-ttu-id="c0bd9-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="c0bd9-110">Parent Element</span></span>                                                   | <span data-ttu-id="c0bd9-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0bd9-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c0bd9-112">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="c0bd9-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="c0bd9-113">None</span><span class="sxs-lookup"><span data-stu-id="c0bd9-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="c0bd9-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0bd9-114">Attributes</span></span>



| <span data-ttu-id="c0bd9-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="c0bd9-115">Attribute</span></span>        | <span data-ttu-id="c0bd9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0bd9-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c0bd9-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="c0bd9-117">relationshipName</span></span> | <span data-ttu-id="c0bd9-118">Público.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-118">Public.</span></span> <span data-ttu-id="c0bd9-119">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-119">Required.</span></span> <span data-ttu-id="c0bd9-120">Nombre canónico de la relación de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="c0bd9-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="c0bd9-121">propertyName</span></span>     | <span data-ttu-id="c0bd9-122">Público.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-122">Public.</span></span> <span data-ttu-id="c0bd9-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-123">Required.</span></span> <span data-ttu-id="c0bd9-124">Nombre canónico de la propiedad relacionada.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="c0bd9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0bd9-125">Remarks</span></span>

<span data-ttu-id="c0bd9-126">Este elemento le permite asignar una propiedad a otra.</span><span class="sxs-lookup"><span data-stu-id="c0bd9-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="c0bd9-127">Por ejemplo, puede asignar el texto de su propiedad personalizada, fabrikam. StorageCapacity, a System. Capacity:</span><span class="sxs-lookup"><span data-stu-id="c0bd9-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
