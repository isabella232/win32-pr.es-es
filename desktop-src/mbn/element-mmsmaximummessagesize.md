---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275510"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span data-ttu-id="3ac99-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span><span class="sxs-lookup"><span data-stu-id="3ac99-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span></span>

<span data-ttu-id="3ac99-104">Especifica el tamaño máximo de los mensajes MMS, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="3ac99-104">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="3ac99-105">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3ac99-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3ac99-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="3ac99-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a><span data-ttu-id="3ac99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ac99-107">Syntax</span></span>

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3ac99-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3ac99-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3ac99-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="3ac99-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3ac99-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ac99-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3ac99-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3ac99-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3ac99-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3ac99-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3ac99-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3ac99-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ac99-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3ac99-114">Parent Element</span></span></th>
<th><span data-ttu-id="3ac99-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ac99-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ac99-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="3ac99-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="3ac99-117">Información de configuración para el servicio de mensajería multimedia (MMS).</span><span class="sxs-lookup"><span data-stu-id="3ac99-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="3ac99-118">Además de establecer los elementos de configuración dentro de este elemento, un perfil de MMS debe tener la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ac99-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="3ac99-119">Su elemento <a href="element-name.md"><strong>Name</strong></a> debe contener un nombre único en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3ac99-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="3ac99-120">Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ac99-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="3ac99-121">Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el ICCID de la SIM para el que está diseñado este perfil.</span><span class="sxs-lookup"><span data-stu-id="3ac99-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="3ac99-122">Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ac99-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="3ac99-123">Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósitos de MMS.</span><span class="sxs-lookup"><span data-stu-id="3ac99-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="3ac99-124">Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ac99-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3ac99-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac99-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ac99-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ac99-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
