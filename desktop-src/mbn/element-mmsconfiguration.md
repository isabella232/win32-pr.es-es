---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275367"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="a880a-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span><span class="sxs-lookup"><span data-stu-id="a880a-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="a880a-104">Información de configuración para el servicio de mensajería multimedia (MMS).</span><span class="sxs-lookup"><span data-stu-id="a880a-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="a880a-105">Además de establecer los elementos de configuración dentro de este elemento, un perfil de MMS debe tener la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="a880a-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="a880a-106">Su elemento [**Name**](element-name.md) debe contener un nombre único en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="a880a-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="a880a-107">Su [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) debe establecerse en **UserProvisioned**.</span><span class="sxs-lookup"><span data-stu-id="a880a-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="a880a-108">Su [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) debe contener el ICCID de la SIM para el que está diseñado este perfil.</span><span class="sxs-lookup"><span data-stu-id="a880a-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="a880a-109">Su [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) debe establecerse en **manual**.</span><span class="sxs-lookup"><span data-stu-id="a880a-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="a880a-110">Su [**PurposeGroupGuid**](element-purposegroupguid.md) debe contener el GUID para el grupo de propósitos de MMS.</span><span class="sxs-lookup"><span data-stu-id="a880a-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="a880a-111">Su [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) debe establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="a880a-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a880a-112">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="a880a-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="a880a-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a880a-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="a880a-114">Clave</span><span class="sxs-lookup"><span data-stu-id="a880a-114">Key</span></span>

<span data-ttu-id="a880a-115">`?`   opcional (cero o uno)</span><span class="sxs-lookup"><span data-stu-id="a880a-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a880a-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a880a-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a880a-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="a880a-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a880a-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a880a-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a880a-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a880a-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a880a-120">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="a880a-120">Child Element</span></span></th>
<th><span data-ttu-id="a880a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a880a-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a880a-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="a880a-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="a880a-123">Especifica el tamaño máximo de los mensajes MMS, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="a880a-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="a880a-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a880a-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a880a-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="a880a-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="a880a-126">Especifica el número de puerto del servidor de MMSC para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a880a-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="a880a-127">Especifique 0 para indicar que no se ha especificado ningún puerto específico.</span><span class="sxs-lookup"><span data-stu-id="a880a-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="a880a-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a880a-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a880a-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="a880a-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="a880a-130">Especifica la dirección URL del servidor de MMSC para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a880a-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="a880a-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a880a-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a880a-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a880a-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a880a-133">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a880a-133">Parent Element</span></span></th>
<th><span data-ttu-id="a880a-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="a880a-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a880a-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="a880a-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="a880a-136">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="a880a-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a880a-137">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="a880a-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="a880a-138">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="a880a-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a880a-139">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="a880a-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a880a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a880a-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a880a-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a880a-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
