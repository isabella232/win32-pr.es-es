---
description: CellularClass
MS-HAID: WWAN\_profile\_v4.element\_CellularClass
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CellularClass
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1953d07176262aba35f54cc80c9b712002cd857
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705577"
---
# <a name="span-idwwan_profile_v4element_cellularclassspancellularclass"></a><span data-ttu-id="d98ff-103"><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass</span><span class="sxs-lookup"><span data-stu-id="d98ff-103"><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass</span></span>

<span data-ttu-id="d98ff-104">Especifica que este perfil solo está activo cuando la clase de teléfono móvil actual es la especificada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-104">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="d98ff-105">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="d98ff-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d98ff-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="d98ff-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<CellularClass>**

## <a name="syntax"></a><span data-ttu-id="d98ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d98ff-107">Syntax</span></span>

``` syntax
<CellularClass>

  "3GPP" | "3GPP2"

</CellularClass>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d98ff-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d98ff-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d98ff-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="d98ff-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d98ff-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d98ff-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d98ff-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d98ff-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d98ff-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d98ff-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d98ff-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d98ff-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d98ff-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d98ff-114">Parent Element</span></span></th>
<th><span data-ttu-id="d98ff-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d98ff-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d98ff-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="d98ff-116"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="d98ff-117">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="d98ff-117">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="d98ff-118">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="d98ff-118">This element is new for v4.</span></span> <span data-ttu-id="d98ff-119">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="d98ff-119">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="d98ff-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="d98ff-120">This element is optional.</span></span> <span data-ttu-id="d98ff-121">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="d98ff-121">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d98ff-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d98ff-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d98ff-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d98ff-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



