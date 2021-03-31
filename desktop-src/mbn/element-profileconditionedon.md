---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154201"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="3dfd1-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span><span class="sxs-lookup"><span data-stu-id="3dfd1-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="3dfd1-104">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="3dfd1-105">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-105">This element is new for v4.</span></span> <span data-ttu-id="3dfd1-106">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="3dfd1-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-107">This element is optional.</span></span> <span data-ttu-id="3dfd1-108">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3dfd1-109">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="3dfd1-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="3dfd1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dfd1-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="3dfd1-111">Clave</span><span class="sxs-lookup"><span data-stu-id="3dfd1-111">Key</span></span>

<span data-ttu-id="3dfd1-112">`?`   opcional (cero o uno)</span><span class="sxs-lookup"><span data-stu-id="3dfd1-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3dfd1-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3dfd1-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3dfd1-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="3dfd1-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3dfd1-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3dfd1-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3dfd1-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dfd1-117">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="3dfd1-117">Child Element</span></span></th>
<th><span data-ttu-id="3dfd1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3dfd1-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dfd1-119"><a href="element-cellularclass.md">CellularClass</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-120">Especifica que este perfil solo está activo cuando la clase de teléfono móvil actual es la especificada.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="3dfd1-121">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="3dfd1-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dfd1-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-123">Especifica que este perfil solo está activo cuando el IMSI actual que se usa en ICCID es el especificado.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="3dfd1-124">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="3dfd1-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dfd1-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-126">Especifica que este perfil solo está activo cuando se conecta a una red de IWLAN.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="3dfd1-127">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="3dfd1-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="3dfd1-128">El valor de este elemento debe ser un valor <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dfd1-129"><a href="element-ratapplicability.md">RATApplicability</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-130">Especifica que este perfil solo está activo cuando el tipo RAT es el especificado.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="3dfd1-131">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="3dfd1-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dfd1-132"><a href="element-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-133">Especifica que este perfil solo está activo cuando la condición de itinerancia actual es la especificada.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="3dfd1-134">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="3dfd1-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="3dfd1-135">El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3dfd1-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3dfd1-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dfd1-137">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3dfd1-137">Parent Element</span></span></th>
<th><span data-ttu-id="3dfd1-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="3dfd1-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dfd1-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3dfd1-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3dfd1-140">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3dfd1-141">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3dfd1-142">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3dfd1-143">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="3dfd1-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3dfd1-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dfd1-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3dfd1-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3dfd1-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



