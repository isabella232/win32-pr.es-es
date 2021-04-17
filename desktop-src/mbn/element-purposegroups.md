---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696342"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="cad51-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span><span class="sxs-lookup"><span data-stu-id="cad51-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="cad51-104">Lista opcional de grupos de perfiles, donde cada grupo incluye perfiles usados para un propósito común.</span><span class="sxs-lookup"><span data-stu-id="cad51-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="cad51-105">Este elemento es nuevo para V4 del esquema.</span><span class="sxs-lookup"><span data-stu-id="cad51-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="cad51-106">Un perfil puede aparecer en varios grupos.</span><span class="sxs-lookup"><span data-stu-id="cad51-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="cad51-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="cad51-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="cad51-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cad51-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="cad51-109">Clave</span><span class="sxs-lookup"><span data-stu-id="cad51-109">Key</span></span>

<span data-ttu-id="cad51-110">`{}`   intervalo específico de repeticiones</span><span class="sxs-lookup"><span data-stu-id="cad51-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="cad51-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cad51-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="cad51-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="cad51-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="cad51-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cad51-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="cad51-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cad51-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cad51-115">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="cad51-115">Child Element</span></span></th>
<th><span data-ttu-id="cad51-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cad51-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cad51-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span><span class="sxs-lookup"><span data-stu-id="cad51-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="cad51-118">Representa un perfil en un PurposeGroup de perfiles.</span><span class="sxs-lookup"><span data-stu-id="cad51-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="cad51-119">Los perfiles se especifican mediante su valor <a href="simpletype-guidtype.md"><strong>guidType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cad51-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="cad51-120">Se definen cuatro valores GUID, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cad51-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cad51-121">Grupo de propósitos</span><span class="sxs-lookup"><span data-stu-id="cad51-121">Purpose group</span></span></th>
<th><span data-ttu-id="cad51-122">GUID</span><span class="sxs-lookup"><span data-stu-id="cad51-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cad51-123">Internet</span><span class="sxs-lookup"><span data-stu-id="cad51-123">Internet</span></span></td>
<td><span data-ttu-id="cad51-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="cad51-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cad51-125">mms</span><span class="sxs-lookup"><span data-stu-id="cad51-125">MMS</span></span></td>
<td><span data-ttu-id="cad51-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="cad51-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cad51-127">IMS</span><span class="sxs-lookup"><span data-stu-id="cad51-127">IMS</span></span></td>
<td><span data-ttu-id="cad51-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="cad51-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cad51-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="cad51-129">SUPL</span></span></td>
<td><span data-ttu-id="cad51-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="cad51-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="cad51-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="cad51-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cad51-132">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cad51-132">Parent Element</span></span></th>
<th><span data-ttu-id="cad51-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="cad51-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cad51-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="cad51-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="cad51-135">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="cad51-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="cad51-136">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="cad51-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="cad51-137">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="cad51-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="cad51-138">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="cad51-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="cad51-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cad51-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cad51-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cad51-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



