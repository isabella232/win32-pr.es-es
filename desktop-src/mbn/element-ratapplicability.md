---
description: RATApplicability
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RATApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155f8e216b6ec00f123d0fe0f378fd9db2e4d75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908049"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span data-ttu-id="568fd-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span><span class="sxs-lookup"><span data-stu-id="568fd-103"><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability</span></span>

<span data-ttu-id="568fd-104">Especifica que este perfil solo está activo cuando el tipo RAT es el especificado.</span><span class="sxs-lookup"><span data-stu-id="568fd-104">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="568fd-105">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="568fd-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="568fd-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="568fd-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<RATApplicability>**

## <a name="syntax"></a><span data-ttu-id="568fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="568fd-107">Syntax</span></span>

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="568fd-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="568fd-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="568fd-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="568fd-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="568fd-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="568fd-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="568fd-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="568fd-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="568fd-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="568fd-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="568fd-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="568fd-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="568fd-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="568fd-114">Parent Element</span></span></th>
<th><span data-ttu-id="568fd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="568fd-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="568fd-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="568fd-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="568fd-117">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="568fd-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="568fd-118">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="568fd-118">This element is new for v4.</span></span> <span data-ttu-id="568fd-119">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="568fd-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="568fd-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="568fd-120">This element is optional.</span></span> <span data-ttu-id="568fd-121">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="568fd-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="568fd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="568fd-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="568fd-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="568fd-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



