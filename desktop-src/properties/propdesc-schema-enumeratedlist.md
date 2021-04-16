---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: enumeratedList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706348"
---
# <a name="enumeratedlist"></a><span data-ttu-id="1459e-103">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1459e-103">enumeratedList</span></span>

<span data-ttu-id="1459e-104">Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="1459e-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="1459e-105">También influye en cómo se puede agrupar la propiedad o en qué valores se muestran en la lista si "editControl" es un listblox.</span><span class="sxs-lookup"><span data-stu-id="1459e-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="1459e-106">Esto solo es aplicable si <displayInfo displayType="Enumerated"> .</span><span class="sxs-lookup"><span data-stu-id="1459e-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="1459e-107">Solo debe haber un elemento [enumeratedList]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1459e-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="1459e-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="1459e-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="1459e-109">Si no se proporciona ningún elemento [enumeratedList]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1459e-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1459e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1459e-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="1459e-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="1459e-111">Element Information</span></span>



| <span data-ttu-id="1459e-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1459e-112">Parent Element</span></span>                                   | <span data-ttu-id="1459e-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1459e-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="1459e-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1459e-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="1459e-115">enum</span><span class="sxs-lookup"><span data-stu-id="1459e-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="1459e-116">enumRange</span><span class="sxs-lookup"><span data-stu-id="1459e-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="1459e-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="1459e-117">Attributes</span></span>



| <span data-ttu-id="1459e-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="1459e-118">Attribute</span></span>          | <span data-ttu-id="1459e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1459e-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1459e-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="1459e-120">defaultText</span></span>        | <span data-ttu-id="1459e-121">Público.</span><span class="sxs-lookup"><span data-stu-id="1459e-121">Public.</span></span> <span data-ttu-id="1459e-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1459e-122">Optional.</span></span> <span data-ttu-id="1459e-123">Especifique el texto predeterminado que se va a usar si se asigna un valor a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) que no se asigna a uno de los elementos enumerados de la lista.</span><span class="sxs-lookup"><span data-stu-id="1459e-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="1459e-124">La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; Use la referencia para que se pueda localizar.</span><span class="sxs-lookup"><span data-stu-id="1459e-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="1459e-125">useValueForDefault</span><span class="sxs-lookup"><span data-stu-id="1459e-125">useValueForDefault</span></span> | <span data-ttu-id="1459e-126">Público.</span><span class="sxs-lookup"><span data-stu-id="1459e-126">Public.</span></span> <span data-ttu-id="1459e-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1459e-127">Optional.</span></span> <span data-ttu-id="1459e-128">Si se establece en "true", se informará a [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) de usar el valor tal cual si el valor no se asigna a uno de los elementos enumerados de la lista.</span><span class="sxs-lookup"><span data-stu-id="1459e-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="1459e-129">En el caso de **IPropertyDescription:: FormatForDisplay**, si se establece en "true" tiene prioridad sobre la configuración de "defaultText".</span><span class="sxs-lookup"><span data-stu-id="1459e-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="1459e-130">El valor predeterminado es "false".</span><span class="sxs-lookup"><span data-stu-id="1459e-130">The default is "false".</span></span> |



 

 

 
