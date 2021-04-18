---
description: Novedades de Windows 7. Elemento contenedor para los elementos relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedPropertyInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 442de657bed7e97f74064c39cc0934c65a6f520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666853"
---
# <a name="relatedpropertyinfo"></a><span data-ttu-id="6363a-104">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="6363a-104">relatedPropertyInfo</span></span>

<span data-ttu-id="6363a-105">Novedades de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6363a-105">New for Windows 7.</span></span> <span data-ttu-id="6363a-106">Elemento contenedor para los elementos [relatedProperty](./propdesc-schema-relatedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6363a-106">Container element for [relatedProperty](./propdesc-schema-relatedproperty.md) elements.</span></span> <span data-ttu-id="6363a-107">Solo debe haber un elemento [relatedPropertyInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="6363a-107">There should be only one [relatedPropertyInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6363a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6363a-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="6363a-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6363a-109">Element Information</span></span>



| <span data-ttu-id="6363a-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6363a-110">Parent Element</span></span>                                                   | <span data-ttu-id="6363a-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6363a-111">Child Elements</span></span>                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="6363a-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6363a-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | [<span data-ttu-id="6363a-113">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="6363a-113">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a><span data-ttu-id="6363a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6363a-114">Attributes</span></span>

<span data-ttu-id="6363a-115">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="6363a-115">This element has no attributes.</span></span>

 

 
