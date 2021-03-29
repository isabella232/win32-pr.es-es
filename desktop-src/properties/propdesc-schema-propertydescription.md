---
description: Describe una única propiedad canónica única.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001571"
---
# <a name="propertydescription"></a><span data-ttu-id="18d31-103">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="18d31-103">propertyDescription</span></span>

<span data-ttu-id="18d31-104">Describe una única propiedad canónica única.</span><span class="sxs-lookup"><span data-stu-id="18d31-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="18d31-105">Cada una de estas propiedades pensadas para estar disponibles en el sistema debe tener un elemento [propertyDescription]() correspondiente.</span><span class="sxs-lookup"><span data-stu-id="18d31-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="18d31-106">Sintaxis para Windows 7</span><span class="sxs-lookup"><span data-stu-id="18d31-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="18d31-107">Sintaxis para vista</span><span class="sxs-lookup"><span data-stu-id="18d31-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="18d31-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="18d31-108">Element Information</span></span>



| <span data-ttu-id="18d31-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="18d31-109">Parent Element</span></span>                                                           | <span data-ttu-id="18d31-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18d31-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="18d31-111">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="18d31-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="18d31-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="18d31-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="18d31-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="18d31-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="18d31-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="18d31-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="18d31-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="18d31-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="18d31-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="18d31-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="18d31-117">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="18d31-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="18d31-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="18d31-118">Attributes</span></span>



| <span data-ttu-id="18d31-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="18d31-119">Attribute</span></span> | <span data-ttu-id="18d31-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="18d31-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d31-121">name</span><span class="sxs-lookup"><span data-stu-id="18d31-121">name</span></span>      | <span data-ttu-id="18d31-122">Necesario.</span><span class="sxs-lookup"><span data-stu-id="18d31-122">Required.</span></span> <span data-ttu-id="18d31-123">Nombre canónico de la propiedad, único para el sistema; por ejemplo, `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="18d31-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="18d31-124">Esta cadena es de tipo canónico-Type y está limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="18d31-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="18d31-125">El nombre distingue entre mayúsculas y minúsculas y debe usar la sintaxis siguiente: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="18d31-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="18d31-126">[**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="18d31-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="18d31-127">formatID</span><span class="sxs-lookup"><span data-stu-id="18d31-127">formatID</span></span>  | <span data-ttu-id="18d31-128">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d31-128">Required.</span></span> <span data-ttu-id="18d31-129">Identificador de formato de la propiedad (FMTID).</span><span class="sxs-lookup"><span data-stu-id="18d31-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="18d31-130">El valor debe incluir llaves envolventes; por ejemplo, `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="18d31-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="18d31-131">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="18d31-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="18d31-132">propID</span><span class="sxs-lookup"><span data-stu-id="18d31-132">propID</span></span>    | <span data-ttu-id="18d31-133">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d31-133">Required.</span></span> <span data-ttu-id="18d31-134">Identificador de propiedad (PID); por ejemplo, `9` .</span><span class="sxs-lookup"><span data-stu-id="18d31-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="18d31-135">[**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="18d31-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="18d31-136">Este valor debe ser mayor o igual que 2.</span><span class="sxs-lookup"><span data-stu-id="18d31-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="18d31-137">El sistema reserva los valores 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="18d31-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
