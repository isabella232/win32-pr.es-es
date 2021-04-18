---
description: MBNProfileExt \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29438df96a3a12bb791870b1cc0d59e84f77d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705571"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span data-ttu-id="1129a-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4)</span><span class="sxs-lookup"><span data-stu-id="1129a-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt\/RoamApplicability (v4)</span></span>

<span data-ttu-id="1129a-104">Especifica que este perfil solo está activo cuando la condición de itinerancia actual es la especificada.</span><span class="sxs-lookup"><span data-stu-id="1129a-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="1129a-105">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="1129a-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="1129a-106">El valor de este elemento debe ser un valor [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) válido.</span><span class="sxs-lookup"><span data-stu-id="1129a-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1129a-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="1129a-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="1129a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1129a-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1129a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1129a-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1129a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1129a-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1129a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1129a-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1129a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1129a-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1129a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1129a-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1129a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1129a-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1129a-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1129a-115">Parent Element</span></span></th>
<th><span data-ttu-id="1129a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1129a-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1129a-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="1129a-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="1129a-118">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="1129a-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1129a-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="1129a-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="1129a-120">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="1129a-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="1129a-121">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="1129a-121">This element is new for v4.</span></span> <span data-ttu-id="1129a-122">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="1129a-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="1129a-123">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="1129a-123">This element is optional.</span></span> <span data-ttu-id="1129a-124">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="1129a-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1129a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1129a-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1129a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1129a-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



