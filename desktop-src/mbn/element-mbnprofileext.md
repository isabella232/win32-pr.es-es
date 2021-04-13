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
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

El elemento **MBNProfileExt** es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.

Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el elemento secundario [**ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**<MBNProfileExt>**

## <a name="syntax"></a>Sintaxis

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

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

`*`   opcional (cero o más)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento secundario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-adminenable.md">AdminEnable</a></td>
<td><p>Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Especifica si el perfil está controlado por itinerancia administrativa. Este elemento es nuevo para V4. El valor de este elemento es un valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Este es un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">ApnID</a></td>
<td><p>Un ID. de APN asociado a este perfil. Este elemento es nuevo en V4 y es opcional.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></td>
<td><p>Especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Contexto</a></td>
<td><p>Especifica los parámetros necesarios para establecer una conexión de datos.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Especifica una lista de proveedores de red preferidos en itinerancia.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Descripción</a></td>
<td><p>Descripción del perfil.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>El nombre del proveedor de inicio de la SIM o el dispositivo especificados. Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">ICONFilePath</a></td>
<td><p>La ruta de acceso al archivo de icono para la conexión. La interfaz de usuario de la conexión del sistema operativo muestra el icono cuando se realiza una conexión con este perfil.</p>
<p>Para obtener más información sobre el uso de este elemento, consulte la documentación de la versión 1 de <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Especifica si este perfil es el perfil predeterminado.</p>
<p>Para obtener más información sobre este elemento, consulte la documentación de la versión 1 de <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></td>
<td><p>Especifica que este perfil es exclusivo de otros perfiles de los mismos conjuntos de perfiles. Este elemento es nuevo para V4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></td>
<td><p>Especifica que este perfil es un perfil de contexto PDP adicional de larga duración. Si el valor de este elemento es <strong>true</strong>, <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> también debe establecerse en <strong>true</strong>. Se trata de un nuevo elemento para V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></td>
<td><p>Especifica que este perfil se va a usar solo para el aprovisionamiento. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP). Este elemento es nuevo para V4.</p>
<p>Si <strong>IsProvisioningProfile</strong> es true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> debe ser false y <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> debe ser manual.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">MmsConfiguration</a></td>
<td><p>Información de configuración para el servicio de mensajería multimedia (MMS).</p>
<p>Además de establecer los elementos de configuración dentro de este elemento, un perfil de MMS debe tener la configuración siguiente.</p>
<ul>
<li>Su elemento <a href="element-name.md"><strong>Name</strong></a> debe contener un nombre único en todo el sistema.</li>
<li>Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned</strong>.</li>
<li>Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el ICCID de la SIM para el que está diseñado este perfil.</li>
<li>Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>manual</strong>.</li>
<li>Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósitos de MMS.</li>
<li>Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">Nombre</a></td>
<td><p>Nombre del perfil. Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nombre</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.</p>
<p>Este elemento es nuevo para V4. Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable. Este elemento es opcional. Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">ProfileCreationType (en MBNProfileExt)</a></td>
<td><p>Especifica el creador del perfil.</p>
<p>Para obtener más información sobre este elemento, consulte la documentación del elemento <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">PurposeGroups</a></td>
<td><p>Lista opcional de grupos de perfiles, donde cada grupo incluye perfiles usados para un propósito común.</p>
<p>Este elemento es nuevo para V4 del esquema.</p>
<p>Un perfil puede aparecer en varios grupos.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">SimIccID</a></td>
<td><p>El número de Identifcation de SIM para dispositivos GSM. Para obtener más información, consulte la documentación del elemento <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">SubscriberID</a></td>
<td><p>Identifica el identificador único del perfil.</p>
<p>En el caso de una red GSM, debe contener la IMSI (identidad del suscriptor móvil internacional) de la tarjeta SIM y los dispositivos CDMA deben contener el número mínimo de identificación móvil del dispositivo.</p>
<p>Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

Es posible que este elemento externo (documento) no esté incluido en otros elementos.

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espacio de nombres</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
