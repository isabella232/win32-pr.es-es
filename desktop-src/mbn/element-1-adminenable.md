---
description: ModemDMConfigProfile \/ AdminEnable (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AdminEnable
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AdminEnable (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20ab248c585e6f599ddb43e6c3f93183baf7373
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388880"
---
# <a name="span-idwwan_profile_v4element_1_adminenablespanmodemdmconfigprofileadminenable-v4"></a><span data-ttu-id="90b39-103"><span id="WWAN_profile_v4.element_1_AdminEnable"></span>ModemDMConfigProfile \/ AdminEnable (v4)</span><span class="sxs-lookup"><span data-stu-id="90b39-103"><span id="WWAN_profile_v4.element_1_AdminEnable"></span>ModemDMConfigProfile\/AdminEnable (v4)</span></span>

<span data-ttu-id="90b39-104">Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</span><span class="sxs-lookup"><span data-stu-id="90b39-104">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="90b39-105">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="90b39-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

## <a name="syntax"></a><span data-ttu-id="90b39-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90b39-106">Syntax</span></span>

``` syntax
<AdminEnable>

  boolean

</AdminEnable>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="90b39-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90b39-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="90b39-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="90b39-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="90b39-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90b39-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="90b39-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90b39-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="90b39-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90b39-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="90b39-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="90b39-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90b39-113">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="90b39-113">Parent Element</span></span></th>
<th><span data-ttu-id="90b39-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b39-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90b39-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="90b39-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="90b39-116">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="90b39-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="90b39-117">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="90b39-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="90b39-118">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="90b39-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="90b39-119">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="90b39-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90b39-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="90b39-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="90b39-121">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="90b39-121">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="90b39-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90b39-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90b39-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90b39-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



