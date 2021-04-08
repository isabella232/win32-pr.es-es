---
description: ConnectionMode
MS-HAID: WWAN\_profile\_v4.element\_ConnectionMode
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ConnectionMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b356780908f8fb6ce6d41e41d2db78e823d6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001129"
---
# <a name="span-idwwan_profile_v4element_connectionmodespanconnectionmode"></a><span data-ttu-id="a81fe-103"><span id="WWAN_profile_v4.element_ConnectionMode"></span>ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="a81fe-103"><span id="WWAN_profile_v4.element_ConnectionMode"></span>ConnectionMode</span></span>

<span data-ttu-id="a81fe-104">Especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="a81fe-104">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="a81fe-105">Para obtener más información, consulte la documentación del elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="a81fe-105">For more information, see the documentation for the v1 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a81fe-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="a81fe-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ConnectionMode>**

## <a name="syntax"></a><span data-ttu-id="a81fe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a81fe-107">Syntax</span></span>

``` syntax
<ConnectionMode>

  "manual" | "auto" | "auto-home"

</ConnectionMode>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a81fe-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a81fe-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a81fe-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="a81fe-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a81fe-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a81fe-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a81fe-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a81fe-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a81fe-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a81fe-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a81fe-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a81fe-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a81fe-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a81fe-114">Parent Element</span></span></th>
<th><span data-ttu-id="a81fe-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a81fe-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a81fe-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a81fe-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a81fe-117">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="a81fe-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a81fe-118">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="a81fe-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a81fe-119">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="a81fe-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a81fe-120">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="a81fe-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a81fe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a81fe-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a81fe-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a81fe-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
