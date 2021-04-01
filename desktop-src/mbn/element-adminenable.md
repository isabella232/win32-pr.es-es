---
description: MBNProfileExt \/ AdminEnable (v4)
MS-HAID: WWAN\_profile\_v4.element\_AdminEnable
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AdminEnable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31feff50a8af55e8958db593f4bc31d6788483a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082101"
---
# <a name="span-idwwan_profile_v4element_adminenablespanadminenablembnprofileextadminenable-v4"></a><span data-ttu-id="e00c2-103"><span id="WWAN_profile_v4.element_AdminEnable"></span>AdminEnableMBNProfileExt \/ AdminEnable (v4)</span><span class="sxs-lookup"><span data-stu-id="e00c2-103"><span id="WWAN_profile_v4.element_AdminEnable"></span>AdminEnableMBNProfileExt\/AdminEnable (v4)</span></span>

<span data-ttu-id="e00c2-104">Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</span><span class="sxs-lookup"><span data-stu-id="e00c2-104">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e00c2-105">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="e00c2-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<AdminEnable\>**

## <a name="syntax"></a><span data-ttu-id="e00c2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e00c2-106">Syntax</span></span>

``` syntax
<AdminEnable>

  boolean

</AdminEnable>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e00c2-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e00c2-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e00c2-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="e00c2-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e00c2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e00c2-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e00c2-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e00c2-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="e00c2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e00c2-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e00c2-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e00c2-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e00c2-113">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e00c2-113">Parent Element</span></span></th>
<th><span data-ttu-id="e00c2-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e00c2-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e00c2-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="e00c2-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="e00c2-116">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="e00c2-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="e00c2-117">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="e00c2-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="e00c2-118">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="e00c2-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="e00c2-119">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="e00c2-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e00c2-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="e00c2-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="e00c2-121">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="e00c2-121">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e00c2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00c2-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e00c2-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e00c2-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



