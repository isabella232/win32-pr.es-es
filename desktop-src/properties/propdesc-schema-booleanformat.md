---
description: Especifica cómo IPropertyDescription::FormatForDisplay debe dar formato al valor de la propiedad booleanFormat como una cadena.
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405968"
---
# <a name="booleanformat"></a><span data-ttu-id="fb0c9-103">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="fb0c9-103">booleanFormat</span></span>

<span data-ttu-id="fb0c9-104">Especifica cómo [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe dar formato al valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="fb0c9-105">Esto solo es aplicable si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="fb0c9-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="fb0c9-106">Solo debe haber un elemento [booleanFormat]() para cada [elemento displayInfo.](./propdesc-schema-displayinfo.md)</span><span class="sxs-lookup"><span data-stu-id="fb0c9-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="fb0c9-107">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="fb0c9-108">Si no se proporciona ningún elemento [booleanFormat,]() la configuración de atributo predeterminada se aplica a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0c9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb0c9-109">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="fb0c9-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fb0c9-110">Element Information</span></span>



| <span data-ttu-id="fb0c9-111">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="fb0c9-111">Parent Element</span></span>                                   | <span data-ttu-id="fb0c9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb0c9-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="fb0c9-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fb0c9-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="fb0c9-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fb0c9-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="fb0c9-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb0c9-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0c9-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="fb0c9-116">Attribute</span></span></th>
<th><span data-ttu-id="fb0c9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb0c9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb0c9-118">formatAs</span><span class="sxs-lookup"><span data-stu-id="fb0c9-118">formatAs</span></span></td>
<td><span data-ttu-id="fb0c9-119">Público.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-119">Public.</span></span> <span data-ttu-id="fb0c9-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-120">Optional.</span></span> <span data-ttu-id="fb0c9-121">El valor predeterminado &quot; es &quot; SíNo.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="fb0c9-122">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fb0c9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fb0c9-123">Value</span></span></th>
<th><span data-ttu-id="fb0c9-124">Significado</span><span class="sxs-lookup"><span data-stu-id="fb0c9-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb0c9-125">SíNo</span><span class="sxs-lookup"><span data-stu-id="fb0c9-125">YesNo</span></span></td>
<td><span data-ttu-id="fb0c9-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-126">Default.</span></span> <span data-ttu-id="fb0c9-127">Da formato al valor &quot; como Sí &quot; o &quot; &quot; No.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="fb0c9-128">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb0c9-129">OnOff</span><span class="sxs-lookup"><span data-stu-id="fb0c9-129">OnOff</span></span></td>
<td><span data-ttu-id="fb0c9-130">Da formato al valor &quot; como On &quot; o &quot; &quot; Off.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="fb0c9-131">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb0c9-132">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="fb0c9-132">TrueFalse</span></span></td>
<td><span data-ttu-id="fb0c9-133">Da formato al valor como &quot; True &quot; o &quot; &quot; False.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="fb0c9-134">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="fb0c9-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
