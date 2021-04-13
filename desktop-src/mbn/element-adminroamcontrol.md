---
description: MBNProfileExt \/ AdminRoamControl (v4)
MS-HAID: WWAN\_profile\_v4.element\_AdminRoamControl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AdminRoamControl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06ac2a3e29e04c5821ebab3be6e6f822c66b8e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360275"
---
# <a name="span-idwwan_profile_v4element_adminroamcontrolspanmbnprofileextadminroamcontrol-v4"></a><span data-ttu-id="36987-103"><span id="WWAN_profile_v4.element_AdminRoamControl"></span>MBNProfileExt \/ AdminRoamControl (v4)</span><span class="sxs-lookup"><span data-stu-id="36987-103"><span id="WWAN_profile_v4.element_AdminRoamControl"></span>MBNProfileExt\/AdminRoamControl (v4)</span></span>

<span data-ttu-id="36987-104">Especifica si el perfil está controlado por itinerancia administrativa.</span><span class="sxs-lookup"><span data-stu-id="36987-104">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="36987-105">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="36987-105">This element is new for v4.</span></span> <span data-ttu-id="36987-106">El valor de este elemento es un valor de [**roamControlType**](simpletype-roamcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="36987-106">The value of this element is a [**roamControlType**](simpletype-roamcontroltype.md) value.</span></span> <span data-ttu-id="36987-107">Este es un elemento opcional; Si no se especifica ningún valor, **AllRoamAllowed** es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="36987-107">This is an optional element; if no value is specified, then **AllRoamAllowed** is the default.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="36987-108">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="36987-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminRoamControl\>**

## <a name="syntax"></a><span data-ttu-id="36987-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36987-109">Syntax</span></span>

``` syntax
<AdminRoamControl>

  "AllRoamAllowed" | "PartnerRoamAllowed" | "NoRoamAllowed"

</AdminRoamControl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="36987-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="36987-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="36987-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="36987-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="36987-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36987-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="36987-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36987-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="36987-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36987-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="36987-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="36987-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36987-116">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="36987-116">Parent Element</span></span></th>
<th><span data-ttu-id="36987-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="36987-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36987-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="36987-118"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="36987-119">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="36987-119">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="36987-120">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="36987-120">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="36987-121">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="36987-121">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="36987-122">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="36987-122">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36987-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="36987-123"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="36987-124">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="36987-124">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="36987-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36987-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36987-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36987-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



