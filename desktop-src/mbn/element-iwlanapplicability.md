---
description: IwlanApplicability
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IwlanApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b8b0376f2ee882a57e4c71e392fb7b02f6eeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705573"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span data-ttu-id="dc522-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span><span class="sxs-lookup"><span data-stu-id="dc522-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span></span>

<span data-ttu-id="dc522-104">Especifica que este perfil solo está activo cuando se conecta a una red de IWLAN.</span><span class="sxs-lookup"><span data-stu-id="dc522-104">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="dc522-105">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="dc522-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="dc522-106">El valor de este elemento debe ser un valor [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) válido.</span><span class="sxs-lookup"><span data-stu-id="dc522-106">The value of this element must be a valid [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="dc522-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="dc522-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IwlanApplicability>**

## <a name="syntax"></a><span data-ttu-id="dc522-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc522-108">Syntax</span></span>

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="dc522-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc522-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="dc522-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="dc522-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="dc522-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc522-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="dc522-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc522-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="dc522-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc522-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="dc522-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="dc522-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc522-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="dc522-115">Parent Element</span></span></th>
<th><span data-ttu-id="dc522-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc522-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc522-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="dc522-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="dc522-118">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="dc522-118">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="dc522-119">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="dc522-119">This element is new for v4.</span></span> <span data-ttu-id="dc522-120">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="dc522-120">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="dc522-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="dc522-121">This element is optional.</span></span> <span data-ttu-id="dc522-122">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="dc522-122">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="dc522-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc522-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc522-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc522-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



