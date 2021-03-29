---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648183"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="aa7fa-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span><span class="sxs-lookup"><span data-stu-id="aa7fa-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="aa7fa-104">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="aa7fa-105">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="aa7fa-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="aa7fa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa7fa-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="aa7fa-107">Clave</span><span class="sxs-lookup"><span data-stu-id="aa7fa-107">Key</span></span>

<span data-ttu-id="aa7fa-108">`?`   opcional (cero o uno)</span><span class="sxs-lookup"><span data-stu-id="aa7fa-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="aa7fa-109">`*`   opcional (cero o más)</span><span class="sxs-lookup"><span data-stu-id="aa7fa-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="aa7fa-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa7fa-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="aa7fa-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="aa7fa-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="aa7fa-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="aa7fa-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa7fa-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa7fa-114">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="aa7fa-114">Child Element</span></span></th>
<th><span data-ttu-id="aa7fa-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa7fa-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa7fa-116"><a href="element-1-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-117">Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa7fa-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-119">Especifica si el perfil está controlado por itinerancia administrativa.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="aa7fa-120">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-120">This element is new for v4.</span></span> <span data-ttu-id="aa7fa-121">El valor de este elemento es un valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aa7fa-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="aa7fa-122">Este es un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa7fa-123"><a href="element-1-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-124">Un ID. de APN asociado a este perfil. Este elemento es nuevo en V4 y es opcional.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa7fa-125"><a href="element-1-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-126">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa7fa-127"><a href="element-1-name.md">Nombre</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-128">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-128">The name of the profile.</span></span> <span data-ttu-id="aa7fa-129">Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nombre</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa7fa-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-131">El identificador de conexión de OEM para la configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa7fa-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (en ModemDMConfigProfile)</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-133">Especifica cómo se creó este perfil de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="aa7fa-134">Este valor se usa para decidir si un usuario puede eliminar el perfil.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="aa7fa-135">Los usuarios solo pueden eliminar perfiles de <strong>UserProvisioned</strong> .</span><span class="sxs-lookup"><span data-stu-id="aa7fa-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa7fa-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-137">Especifica que este perfil solo está activo cuando la condición de itinerancia actual es la especificada.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="aa7fa-138">De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="aa7fa-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="aa7fa-139">El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa7fa-140"><a href="element-1-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="aa7fa-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="aa7fa-141">El número de Identifcation de SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="aa7fa-142">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="aa7fa-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="aa7fa-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="aa7fa-144">Es posible que este elemento externo (documento) no esté incluido en otros elementos.</span><span class="sxs-lookup"><span data-stu-id="aa7fa-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7fa-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa7fa-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa7fa-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa7fa-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



