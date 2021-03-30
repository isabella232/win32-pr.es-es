---
description: 'Especifica cómo IPropertyDescription:: FormatForDisplay debe formatear el valor de la propiedad como una cadena. Esto solo es aplicable si <displayInfo displayType=&\#0034;String&\#0034;> .'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: booleanFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002047"
---
# <a name="booleanformat"></a><span data-ttu-id="a5c2f-104">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a5c2f-104">booleanFormat</span></span>

<span data-ttu-id="a5c2f-105">Especifica cómo [**IPropertyDescription:: FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) debe formatear el valor de la propiedad como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="a5c2f-106">Esto solo es aplicable si <displayInfo displayType="String"> .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="a5c2f-107">Solo debe haber un elemento [booleanFormat]() para cada elemento [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="a5c2f-108">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="a5c2f-109">Si no se proporciona ningún elemento [booleanFormat]() , los valores de atributo predeterminados se aplican a la descripción de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c2f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5c2f-110">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="a5c2f-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a5c2f-111">Element Information</span></span>



| <span data-ttu-id="a5c2f-112">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a5c2f-112">Parent Element</span></span>                                   | <span data-ttu-id="a5c2f-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5c2f-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="a5c2f-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a5c2f-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="a5c2f-115">None</span><span class="sxs-lookup"><span data-stu-id="a5c2f-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="a5c2f-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5c2f-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5c2f-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="a5c2f-117">Attribute</span></span></th>
<th><span data-ttu-id="a5c2f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5c2f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5c2f-119">formatas</span><span class="sxs-lookup"><span data-stu-id="a5c2f-119">formatAs</span></span></td>
<td><span data-ttu-id="a5c2f-120">Público.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-120">Public.</span></span> <span data-ttu-id="a5c2f-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-121">Optional.</span></span> <span data-ttu-id="a5c2f-122">El valor predeterminado es &quot; síno &quot; .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="a5c2f-123">Estos son los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a5c2f-124">Value</span><span class="sxs-lookup"><span data-stu-id="a5c2f-124">Value</span></span></th>
<th><span data-ttu-id="a5c2f-125">Significado</span><span class="sxs-lookup"><span data-stu-id="a5c2f-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5c2f-126">SíNo</span><span class="sxs-lookup"><span data-stu-id="a5c2f-126">YesNo</span></span></td>
<td><span data-ttu-id="a5c2f-127">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-127">Default.</span></span> <span data-ttu-id="a5c2f-128">Da formato al valor como &quot; sí &quot; o &quot; no &quot; .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="a5c2f-129">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5c2f-130">OnOff</span><span class="sxs-lookup"><span data-stu-id="a5c2f-130">OnOff</span></span></td>
<td><span data-ttu-id="a5c2f-131">Da formato al valor como &quot; activado &quot; o &quot; desactivado &quot; .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="a5c2f-132">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5c2f-133">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="a5c2f-133">TrueFalse</span></span></td>
<td><span data-ttu-id="a5c2f-134">Da formato al valor como &quot; true &quot; o &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="a5c2f-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="a5c2f-135">Requiere que el tipo de propiedad sea booleano.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
