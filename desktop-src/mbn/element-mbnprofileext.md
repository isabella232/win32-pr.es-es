---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360355"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="447fb-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span><span class="sxs-lookup"><span data-stu-id="447fb-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="447fb-104">El elemento **MBNProfileExt** es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="447fb-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="447fb-105">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="447fb-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="447fb-106">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="447fb-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="447fb-107">Use el elemento secundario [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="447fb-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="447fb-108">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="447fb-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="447fb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="447fb-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="447fb-110">Clave</span><span class="sxs-lookup"><span data-stu-id="447fb-110">Key</span></span>

<span data-ttu-id="447fb-111">`?`   opcional (cero o uno)</span><span class="sxs-lookup"><span data-stu-id="447fb-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="447fb-112">`*`   opcional (cero o más)</span><span class="sxs-lookup"><span data-stu-id="447fb-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="447fb-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="447fb-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="447fb-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="447fb-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="447fb-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="447fb-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="447fb-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="447fb-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="447fb-117">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="447fb-117">Child Element</span></span></th>
<th><span data-ttu-id="447fb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="447fb-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="447fb-119"><a href="element-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="447fb-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="447fb-120">Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="447fb-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="447fb-122">Especifica si el perfil está controlado por itinerancia administrativa.</span><span class="sxs-lookup"><span data-stu-id="447fb-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="447fb-123">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-123">This element is new for v4.</span></span> <span data-ttu-id="447fb-124">El valor de este elemento es un valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="447fb-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="447fb-125">Este es un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="447fb-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-126"><a href="element-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="447fb-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="447fb-127">Un ID. de APN asociado a este perfil. Este elemento es nuevo en V4 y es opcional.</span><span class="sxs-lookup"><span data-stu-id="447fb-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span><span class="sxs-lookup"><span data-stu-id="447fb-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="447fb-129">Especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.</span><span class="sxs-lookup"><span data-stu-id="447fb-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="447fb-130">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="447fb-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="447fb-132">Especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.</span><span class="sxs-lookup"><span data-stu-id="447fb-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="447fb-133">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-134"><a href="element-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="447fb-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="447fb-135">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="447fb-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="447fb-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="447fb-137">Especifica una lista de proveedores de red preferidos en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="447fb-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="447fb-138">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-139"><a href="element-description.md">Descripción</a></span><span class="sxs-lookup"><span data-stu-id="447fb-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="447fb-140">Descripción del perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="447fb-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="447fb-142">El nombre del proveedor de inicio de la SIM o el dispositivo especificados.</span><span class="sxs-lookup"><span data-stu-id="447fb-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="447fb-143">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-144"><a href="element-iconfilepath.md">ICONFilePath</a></span><span class="sxs-lookup"><span data-stu-id="447fb-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="447fb-145">La ruta de acceso al archivo de icono para la conexión.</span><span class="sxs-lookup"><span data-stu-id="447fb-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="447fb-146">La interfaz de usuario de la conexión del sistema operativo muestra el icono cuando se realiza una conexión con este perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="447fb-147">Para obtener más información sobre el uso de este elemento, consulte la documentación de la versión 1 de <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="447fb-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="447fb-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="447fb-149">Especifica si este perfil es el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="447fb-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="447fb-150">Para obtener más información sobre este elemento, consulte la documentación de la versión 1 de <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="447fb-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span><span class="sxs-lookup"><span data-stu-id="447fb-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="447fb-152">Especifica que este perfil es exclusivo de otros perfiles de los mismos conjuntos de perfiles. Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span><span class="sxs-lookup"><span data-stu-id="447fb-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="447fb-154">Especifica que este perfil es un perfil de contexto PDP adicional de larga duración. Si el valor de este elemento es <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> también debe establecerse en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="447fb-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="447fb-155">Se trata de un nuevo elemento para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span><span class="sxs-lookup"><span data-stu-id="447fb-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="447fb-157">Especifica que este perfil se va a usar solo para el aprovisionamiento. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="447fb-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="447fb-158">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="447fb-159">Si <strong>IsProvisioningProfile</strong> es true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> debe ser false y <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> debe ser manual.</span><span class="sxs-lookup"><span data-stu-id="447fb-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="447fb-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="447fb-161">Información de configuración para el servicio de mensajería multimedia (MMS).</span><span class="sxs-lookup"><span data-stu-id="447fb-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="447fb-162">Además de establecer los elementos de configuración dentro de este elemento, un perfil de MMS debe tener la configuración siguiente.</span><span class="sxs-lookup"><span data-stu-id="447fb-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="447fb-163">Su elemento <a href="element-name.md"><strong>Name</strong></a> debe contener un nombre único en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="447fb-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="447fb-164">Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned</strong>.</span><span class="sxs-lookup"><span data-stu-id="447fb-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="447fb-165">Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el ICCID de la SIM para el que está diseñado este perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="447fb-166">Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>manual</strong>.</span><span class="sxs-lookup"><span data-stu-id="447fb-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="447fb-167">Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósitos de MMS.</span><span class="sxs-lookup"><span data-stu-id="447fb-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="447fb-168">Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="447fb-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-169"><a href="element-name.md">Nombre</a></span><span class="sxs-lookup"><span data-stu-id="447fb-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="447fb-170">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-170">The name of the profile.</span></span> <span data-ttu-id="447fb-171">Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nombre</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="447fb-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="447fb-173">Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="447fb-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="447fb-174">Este elemento es nuevo para V4.</span><span class="sxs-lookup"><span data-stu-id="447fb-174">This element is new for v4.</span></span> <span data-ttu-id="447fb-175">Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable.</span><span class="sxs-lookup"><span data-stu-id="447fb-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="447fb-176">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="447fb-176">This element is optional.</span></span> <span data-ttu-id="447fb-177">Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="447fb-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-178"><a href="element-profilecreationtype.md">ProfileCreationType (en MBNProfileExt)</a></span><span class="sxs-lookup"><span data-stu-id="447fb-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="447fb-179">Especifica el creador del perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="447fb-180">Para obtener más información sobre este elemento, consulte la documentación del elemento <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-181"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="447fb-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="447fb-182">Lista opcional de grupos de perfiles, donde cada grupo incluye perfiles usados para un propósito común.</span><span class="sxs-lookup"><span data-stu-id="447fb-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="447fb-183">Este elemento es nuevo para V4 del esquema.</span><span class="sxs-lookup"><span data-stu-id="447fb-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="447fb-184">Un perfil puede aparecer en varios grupos.</span><span class="sxs-lookup"><span data-stu-id="447fb-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="447fb-185"><a href="element-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="447fb-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="447fb-186">El número de Identifcation de SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="447fb-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="447fb-187">Para obtener más información, consulte la documentación del elemento <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="447fb-188"><a href="element-subscriberid.md">SubscriberID</a></span><span class="sxs-lookup"><span data-stu-id="447fb-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="447fb-189">Identifica el identificador único del perfil.</span><span class="sxs-lookup"><span data-stu-id="447fb-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="447fb-190">En el caso de una red GSM, debe contener la IMSI (identidad del suscriptor móvil internacional) de la tarjeta SIM y los dispositivos CDMA deben contener el número mínimo de identificación móvil del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="447fb-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="447fb-191">Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="447fb-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="447fb-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="447fb-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="447fb-193">Es posible que este elemento externo (documento) no esté incluido en otros elementos.</span><span class="sxs-lookup"><span data-stu-id="447fb-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="447fb-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="447fb-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="447fb-195">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="447fb-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
