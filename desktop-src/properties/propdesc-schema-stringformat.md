---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec05a6eedf1734c1d62c0503027810ad05916160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666851"
---
# <a name="stringformat"></a><span data-ttu-id="e5d2a-104">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e5d2a-104">stringFormat</span></span>

<span data-ttu-id="e5d2a-105">Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="e5d2a-106">Esto solo es aplicable si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="e5d2a-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="e5d2a-107">Solo debe haber un elemento [StringFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d2a-107">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e5d2a-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e5d2a-109">Si no se proporciona ningún elemento [StringFormat]() , se aplica la configuración de atributo predeterminada a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-109">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d2a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5d2a-110">Syntax</span></span>


```
<!-- stringFormat -->
<xs:element name="stringFormat"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="formatAs">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="FileName"/>
                    <xs:enumeration value="FilePath"/>
                    <xs:enumeration value="Hyperlink"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e5d2a-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e5d2a-111">Element Information</span></span>



| <span data-ttu-id="e5d2a-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e5d2a-112">Parent Element</span></span>                                   | <span data-ttu-id="e5d2a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5d2a-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e5d2a-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e5d2a-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e5d2a-115">None</span><span class="sxs-lookup"><span data-stu-id="e5d2a-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e5d2a-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5d2a-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d2a-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="e5d2a-117">Attribute</span></span></th>
<th><span data-ttu-id="e5d2a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5d2a-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5d2a-119">formatas</span><span class="sxs-lookup"><span data-stu-id="e5d2a-119">formatAs</span></span></td>
<td><span data-ttu-id="e5d2a-120">Público.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-120">Public.</span></span> <span data-ttu-id="e5d2a-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-121">Optional.</span></span> <span data-ttu-id="e5d2a-122">El valor predeterminado es &quot; General &quot; .</span><span class="sxs-lookup"><span data-stu-id="e5d2a-122">Default is &quot;General&quot;.</span></span> <span data-ttu-id="e5d2a-123">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e5d2a-124">Value</span><span class="sxs-lookup"><span data-stu-id="e5d2a-124">Value</span></span></th>
<th><span data-ttu-id="e5d2a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="e5d2a-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5d2a-126">General</span><span class="sxs-lookup"><span data-stu-id="e5d2a-126">General</span></span></td>
<td><span data-ttu-id="e5d2a-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-127">Default.</span></span> <span data-ttu-id="e5d2a-128">Devuelve el valor como una cadena sin formato.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-128">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2a-129">FileName</span><span class="sxs-lookup"><span data-stu-id="e5d2a-129">FileName</span></span></td>
<td><span data-ttu-id="e5d2a-130">Da formato al valor como un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-130">Formats the value as a file name.</span></span> <span data-ttu-id="e5d2a-131">Oculta la extensión según la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-131">Hides the extension according to user settings.</span></span> <span data-ttu-id="e5d2a-132">Requiere que el tipo de propiedad sea una cadena.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-132">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5d2a-133">FilePath</span><span class="sxs-lookup"><span data-stu-id="e5d2a-133">FilePath</span></span></td>
<td><span data-ttu-id="e5d2a-134">Da formato al valor como una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-134">Formats the value as a file path.</span></span> <span data-ttu-id="e5d2a-135">Oculta la extensión según la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-135">Hides the extension according to user settings.</span></span> <span data-ttu-id="e5d2a-136">Requiere que el tipo de propiedad sea una cadena.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-136">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5d2a-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="e5d2a-137">Hyperlink</span></span></td>
<td><span data-ttu-id="e5d2a-138">Da formato al valor como un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="e5d2a-138">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
