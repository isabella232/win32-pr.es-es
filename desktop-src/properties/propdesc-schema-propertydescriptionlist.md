---
description: Contenedor de uno o varios elementos propertyDescription individuales.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648285"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="03143-103">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="03143-103">propertyDescriptionList</span></span>

<span data-ttu-id="03143-104">Contenedor de uno o varios elementos [propertyDescription](./propdesc-schema-propertydescription.md) individuales.</span><span class="sxs-lookup"><span data-stu-id="03143-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="03143-105">Un archivo de esquema de descripción de la propiedad. propDesc debe contener al menos un elemento [propertyDescriptionList]() .</span><span class="sxs-lookup"><span data-stu-id="03143-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="03143-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03143-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="03143-107">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="03143-107">Element Information</span></span>



| <span data-ttu-id="03143-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="03143-108">Parent Element</span></span>                        | <span data-ttu-id="03143-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="03143-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="03143-110">schema</span><span class="sxs-lookup"><span data-stu-id="03143-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="03143-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="03143-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="03143-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="03143-112">Attributes</span></span>



| <span data-ttu-id="03143-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="03143-113">Attribute</span></span> | <span data-ttu-id="03143-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="03143-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="03143-115">publisher</span><span class="sxs-lookup"><span data-stu-id="03143-115">publisher</span></span> | <span data-ttu-id="03143-116">Público.</span><span class="sxs-lookup"><span data-stu-id="03143-116">Public.</span></span> <span data-ttu-id="03143-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03143-117">Required.</span></span> <span data-ttu-id="03143-118">El nombre para mostrar del publicador que proporciona el esquema.</span><span class="sxs-lookup"><span data-stu-id="03143-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="03143-119">product</span><span class="sxs-lookup"><span data-stu-id="03143-119">product</span></span>   | <span data-ttu-id="03143-120">Público.</span><span class="sxs-lookup"><span data-stu-id="03143-120">Public.</span></span> <span data-ttu-id="03143-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03143-121">Required.</span></span> <span data-ttu-id="03143-122">Nombre para mostrar del producto que proporciona el esquema.</span><span class="sxs-lookup"><span data-stu-id="03143-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="03143-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03143-123">Remarks</span></span>

<span data-ttu-id="03143-124">[PropertyDescriptionList]() no se debe confundir con "listas de propiedades" y [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que son completamente independientes.</span><span class="sxs-lookup"><span data-stu-id="03143-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
