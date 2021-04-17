---
description: Especifica cómo se muestran las etiquetas de la propiedad.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666861"
---
# <a name="labelinfo"></a><span data-ttu-id="b5ec7-103">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b5ec7-103">labelInfo</span></span>

<span data-ttu-id="b5ec7-104">Especifica cómo se muestran las etiquetas de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="b5ec7-105">Solo debe haber un elemento [labelInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="b5ec7-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="b5ec7-106">Si hay varios elementos, se usa el último.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="b5ec7-107">Si no se proporciona ningún elemento [labelInfo]() , no se muestra la etiqueta de la propiedad; sin embargo, esto suele ser un defecto.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ec7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5ec7-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="b5ec7-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b5ec7-109">Element Information</span></span>



| <span data-ttu-id="b5ec7-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b5ec7-110">Parent Element</span></span>                                                   | <span data-ttu-id="b5ec7-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5ec7-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b5ec7-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b5ec7-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="b5ec7-113">None</span><span class="sxs-lookup"><span data-stu-id="b5ec7-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="b5ec7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5ec7-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5ec7-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="b5ec7-115">Attribute</span></span></th>
<th><span data-ttu-id="b5ec7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ec7-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5ec7-117">etiqueta</span><span class="sxs-lookup"><span data-stu-id="b5ec7-117">label</span></span></td>
<td><span data-ttu-id="b5ec7-118">Público.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-118">Public.</span></span> <span data-ttu-id="b5ec7-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-119">Optional.</span></span> <span data-ttu-id="b5ec7-120">La etiqueta tal como se muestra en la interfaz de usuario (por ejemplo, la etiqueta de la columna de detalles o el panel de vista previa).</span><span class="sxs-lookup"><span data-stu-id="b5ec7-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="b5ec7-121">La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="b5ec7-122">Use la cadena de presentación indirecta porque se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="b5ec7-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: getDisplayName</strong></a> devuelve el nombre para mostrar resuelto.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5ec7-124">sortDescription</span><span class="sxs-lookup"><span data-stu-id="b5ec7-124">sortDescription</span></span></td>
<td><span data-ttu-id="b5ec7-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-125">Optional.</span></span> <span data-ttu-id="b5ec7-126">Especifica las cadenas que se ofrecen como opciones de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="b5ec7-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> devuelve esta descripción de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="b5ec7-128">Los valores siguientes proporcionan las cadenas de interfaz de usuario correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="b5ec7-129">General: orden de marcha en orden &quot; &quot;  /  &quot; descendente&quot;</span><span class="sxs-lookup"><span data-stu-id="b5ec7-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="b5ec7-130">AToZ: a &quot; en la parte superior &quot;  /  &quot; Z en la parte superior&quot;</span><span class="sxs-lookup"><span data-stu-id="b5ec7-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="b5ec7-131">LowestHighest: &quot; más &quot;  /  &quot; alto en la parte superior superior&quot;</span><span class="sxs-lookup"><span data-stu-id="b5ec7-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="b5ec7-132">OldestNewest: &quot; más antiguo en la parte superior &quot;  /  &quot; más reciente&quot;</span><span class="sxs-lookup"><span data-stu-id="b5ec7-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="b5ec7-133">SmallestLargest: más pequeño en la parte superior &quot; &quot;  /  &quot; más grande&quot;</span><span class="sxs-lookup"><span data-stu-id="b5ec7-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5ec7-134">invitationText</span><span class="sxs-lookup"><span data-stu-id="b5ec7-134">invitationText</span></span></td>
<td><span data-ttu-id="b5ec7-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-135">Optional.</span></span> <span data-ttu-id="b5ec7-136">El texto de la cadena de ayuda que se muestra como una instrucción al usuario para el control o la información sobre herramientas (por ejemplo, &quot; Escriba el nombre del autor &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b5ec7-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="b5ec7-137">La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="b5ec7-138">Use la cadena de presentación indirecta porque se puede localizar.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="b5ec7-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> devuelve el texto de la invitación resuelta.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5ec7-140">hideLabel</span><span class="sxs-lookup"><span data-stu-id="b5ec7-140">hideLabel</span></span></td>
<td><span data-ttu-id="b5ec7-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-141">Optional.</span></span> <span data-ttu-id="b5ec7-142">El valor predeterminado es &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="b5ec7-143">Indica si la etiqueta está oculta.</span><span class="sxs-lookup"><span data-stu-id="b5ec7-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
