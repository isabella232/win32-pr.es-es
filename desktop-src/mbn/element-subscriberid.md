---
description: SubscriberID
MS-HAID: WWAN\_profile\_v4.element\_SubscriberID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SubscriberID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525cd75dbf1ab752ab17ea32d566e57977ab74a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686757"
---
# <a name="span-idwwan_profile_v4element_subscriberidspansubscriberid"></a><span data-ttu-id="119e6-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span><span class="sxs-lookup"><span data-stu-id="119e6-103"><span id="WWAN_profile_v4.element_SubscriberID"></span>SubscriberID</span></span>

<span data-ttu-id="119e6-104">Identifica el identificador único del perfil.</span><span class="sxs-lookup"><span data-stu-id="119e6-104">Identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="119e6-105">En el caso de una red GSM, debe contener la IMSI (identidad del suscriptor móvil internacional) de la tarjeta SIM y los dispositivos CDMA deben contener el número mínimo de identificación móvil del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="119e6-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="119e6-106">Para obtener más información, vea la documentación del elemento de [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="119e6-106">For more information, see the documentation for the v1 [**SubscriberID**](./schema-subscriberid-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="119e6-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="119e6-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<SubscriberID>**

## <a name="syntax"></a><span data-ttu-id="119e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="119e6-108">Syntax</span></span>

``` syntax
<SubscriberID>

  subscriberIdType

</SubscriberID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="119e6-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="119e6-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="119e6-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="119e6-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="119e6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="119e6-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="119e6-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="119e6-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="119e6-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="119e6-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="119e6-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="119e6-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="119e6-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="119e6-115">Parent Element</span></span></th>
<th><span data-ttu-id="119e6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="119e6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="119e6-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="119e6-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="119e6-118">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="119e6-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="119e6-119">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="119e6-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="119e6-120">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="119e6-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="119e6-121">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="119e6-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="119e6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="119e6-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="119e6-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="119e6-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
