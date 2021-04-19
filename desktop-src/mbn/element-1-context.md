---
description: Contexto de ModemDMConfigProfile \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexto (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388852"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="cfea9-103"><span id="WWAN_profile_v4.element_1_Context"></span>Contexto de ModemDMConfigProfile \/ (v4)</span><span class="sxs-lookup"><span data-stu-id="cfea9-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="cfea9-104">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="cfea9-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="cfea9-105">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="cfea9-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="cfea9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfea9-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="cfea9-107">Clave</span><span class="sxs-lookup"><span data-stu-id="cfea9-107">Key</span></span>

<span data-ttu-id="cfea9-108">`?`   opcional (cero o uno)</span><span class="sxs-lookup"><span data-stu-id="cfea9-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="cfea9-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cfea9-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="cfea9-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="cfea9-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="cfea9-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cfea9-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="cfea9-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cfea9-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfea9-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="cfea9-113">Child Element</span></span></th>
<th><span data-ttu-id="cfea9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfea9-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cfea9-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="cfea9-116">Identifica el APN o la cadena de marcado que se va a utilizar para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="cfea9-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="cfea9-117">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="cfea9-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfea9-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="cfea9-119">>Especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="cfea9-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="cfea9-120">Tenga en cuenta que en V4, hay un nuevo valor de enumeración disponible para este elemento.</span><span class="sxs-lookup"><span data-stu-id="cfea9-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="cfea9-121"><strong>La selección activa</strong> significa que un protocolo de autenticación se va a seleccionar por las capas inferiores.</span><span class="sxs-lookup"><span data-stu-id="cfea9-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="cfea9-122">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="cfea9-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfea9-123"><a href="element-1-compression.md">Compresión</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="cfea9-124">Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="cfea9-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="cfea9-125">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="cfea9-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfea9-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="cfea9-127">Especifica el tipo de IP que se va a usar en esta conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="cfea9-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="cfea9-128">Este elemento es nuevo en V4 del esquema.</span><span class="sxs-lookup"><span data-stu-id="cfea9-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="cfea9-129">El elemento puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cfea9-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cfea9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="cfea9-130">Value</span></span></th>
<th><span data-ttu-id="cfea9-131">Significado</span><span class="sxs-lookup"><span data-stu-id="cfea9-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cfea9-132">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cfea9-132">Default</span></span></td>
<td><span data-ttu-id="cfea9-133">El tipo de IP se va a seleccionar por las capas inferiores</span><span class="sxs-lookup"><span data-stu-id="cfea9-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfea9-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="cfea9-134">IPv4</span></span></td>
<td><span data-ttu-id="cfea9-135">Usar IPv4</span><span class="sxs-lookup"><span data-stu-id="cfea9-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfea9-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="cfea9-136">IPv6</span></span></td>
<td><span data-ttu-id="cfea9-137">Usar IPv6</span><span class="sxs-lookup"><span data-stu-id="cfea9-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfea9-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="cfea9-138">IPv4v6</span></span></td>
<td><span data-ttu-id="cfea9-139">Usar IPv4 y/o IPv6, como están disponibles.</span><span class="sxs-lookup"><span data-stu-id="cfea9-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfea9-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="cfea9-140">XLAT</span></span></td>
<td><span data-ttu-id="cfea9-141">Usar 464XLAT para canalizar redes IPv4 a través de IPv6</span><span class="sxs-lookup"><span data-stu-id="cfea9-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfea9-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="cfea9-143">Credenciales de inicio de sesión para una conexión.</span><span class="sxs-lookup"><span data-stu-id="cfea9-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="cfea9-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="cfea9-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfea9-145">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cfea9-145">Parent Element</span></span></th>
<th><span data-ttu-id="cfea9-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfea9-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cfea9-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="cfea9-148">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="cfea9-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="cfea9-149">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="cfea9-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="cfea9-150">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="cfea9-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="cfea9-151">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="cfea9-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfea9-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="cfea9-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="cfea9-153">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="cfea9-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="cfea9-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfea9-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfea9-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cfea9-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



