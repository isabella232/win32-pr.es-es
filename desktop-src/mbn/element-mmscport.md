---
description: MmscPort
MS-HAID: WWAN\_profile\_v4.element\_MmscPort
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscPort
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08812a87b404cdec3caab43d56d4b9afdca9212b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360354"
---
# <a name="span-idwwan_profile_v4element_mmscportspanmmscport"></a><span data-ttu-id="d3340-103"><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort</span><span class="sxs-lookup"><span data-stu-id="d3340-103"><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort</span></span>

<span data-ttu-id="d3340-104">Especifica el número de puerto del servidor de MMSC para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3340-104">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="d3340-105">Especifique 0 para indicar que no se ha especificado ningún puerto específico.</span><span class="sxs-lookup"><span data-stu-id="d3340-105">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="d3340-106">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3340-106">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d3340-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="d3340-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscPort>**

## <a name="syntax"></a><span data-ttu-id="d3340-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3340-108">Syntax</span></span>

``` syntax
<MmscPort>

  [TBD (missing description)]

</MmscPort>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d3340-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d3340-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d3340-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="d3340-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d3340-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3340-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d3340-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d3340-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d3340-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3340-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d3340-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d3340-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3340-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d3340-115">Parent Element</span></span></th>
<th><span data-ttu-id="d3340-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3340-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3340-117"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="d3340-117"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="d3340-118">Información de configuración para el servicio de mensajería multimedia (MMS).</span><span class="sxs-lookup"><span data-stu-id="d3340-118">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="d3340-119">Además de establecer los elementos de configuración dentro de este elemento, un perfil de MMS debe tener la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="d3340-119">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="d3340-120">Su elemento <a href="element-name.md"><strong>Name</strong></a> debe contener un nombre único en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="d3340-120">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="d3340-121">Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3340-121">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="d3340-122">Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el ICCID de la SIM para el que está diseñado este perfil.</span><span class="sxs-lookup"><span data-stu-id="d3340-122">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="d3340-123">Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3340-123">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="d3340-124">Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósitos de MMS.</span><span class="sxs-lookup"><span data-stu-id="d3340-124">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="d3340-125">Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="d3340-125">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d3340-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3340-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3340-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d3340-127">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
