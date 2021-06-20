---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad stringFormat como una cadena.
ms.assetid: 7c38bc15-be86-4260-b2e4-13afc90de6d7
title: stringFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730355507b78d99eba02e82666427dd29425c942
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408358"
---
# <a name="stringformat"></a><span data-ttu-id="06ee8-103">stringFormat</span><span class="sxs-lookup"><span data-stu-id="06ee8-103">stringFormat</span></span>

<span data-ttu-id="06ee8-104">Especifica cómo [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe dar formato al valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="06ee8-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="06ee8-105">Esto solo es aplicable si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="06ee8-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="06ee8-106">Solo debe haber un [elemento stringFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)</span><span class="sxs-lookup"><span data-stu-id="06ee8-106">There should be only one [stringFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="06ee8-107">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="06ee8-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="06ee8-108">Si no se proporciona ningún elemento [stringFormat,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="06ee8-108">If no [stringFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="06ee8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06ee8-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="06ee8-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="06ee8-110">Element Information</span></span>



| <span data-ttu-id="06ee8-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="06ee8-111">Parent Element</span></span>                                   | <span data-ttu-id="06ee8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06ee8-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="06ee8-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="06ee8-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="06ee8-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="06ee8-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="06ee8-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="06ee8-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06ee8-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="06ee8-116">Attribute</span></span></th>
<th><span data-ttu-id="06ee8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="06ee8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06ee8-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="06ee8-118">formatAs</span></span></td>
<td><span data-ttu-id="06ee8-119">Público.</span><span class="sxs-lookup"><span data-stu-id="06ee8-119">Public.</span></span> <span data-ttu-id="06ee8-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="06ee8-120">Optional.</span></span> <span data-ttu-id="06ee8-121">El valor predeterminado &quot; es &quot; General.</span><span class="sxs-lookup"><span data-stu-id="06ee8-121">Default is &quot;General&quot;.</span></span> <span data-ttu-id="06ee8-122">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="06ee8-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06ee8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="06ee8-123">Value</span></span></th>
<th><span data-ttu-id="06ee8-124">Significado</span><span class="sxs-lookup"><span data-stu-id="06ee8-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06ee8-125">General</span><span class="sxs-lookup"><span data-stu-id="06ee8-125">General</span></span></td>
<td><span data-ttu-id="06ee8-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="06ee8-126">Default.</span></span> <span data-ttu-id="06ee8-127">Devuelve el valor como una cadena sin formato.</span><span class="sxs-lookup"><span data-stu-id="06ee8-127">Returns the value as an unformatted string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06ee8-128">FileName</span><span class="sxs-lookup"><span data-stu-id="06ee8-128">FileName</span></span></td>
<td><span data-ttu-id="06ee8-129">Da formato al valor como un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="06ee8-129">Formats the value as a file name.</span></span> <span data-ttu-id="06ee8-130">Oculta la extensión según la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="06ee8-130">Hides the extension according to user settings.</span></span> <span data-ttu-id="06ee8-131">Requiere que el tipo de propiedad sea String.</span><span class="sxs-lookup"><span data-stu-id="06ee8-131">Requires the property type to be String.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06ee8-132">FilePath</span><span class="sxs-lookup"><span data-stu-id="06ee8-132">FilePath</span></span></td>
<td><span data-ttu-id="06ee8-133">Da formato al valor como una ruta de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="06ee8-133">Formats the value as a file path.</span></span> <span data-ttu-id="06ee8-134">Oculta la extensión según la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="06ee8-134">Hides the extension according to user settings.</span></span> <span data-ttu-id="06ee8-135">Requiere que el tipo de propiedad sea String.</span><span class="sxs-lookup"><span data-stu-id="06ee8-135">Requires the property type to be String.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06ee8-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="06ee8-136">Hyperlink</span></span></td>
<td><span data-ttu-id="06ee8-137">Da formato al valor como un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="06ee8-137">Formats the value as a hyperlink.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
