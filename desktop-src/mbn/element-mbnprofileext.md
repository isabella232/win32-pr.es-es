---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf6b821d36fc69c06fd42fad58efc4102e64f6a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987918"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

El **elemento MBNProfileExt** es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.

Puede haber más de un elemento MbnProfileExt en un perfil que describa la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el [**elemento secundario ProfileConditionedOn**](element-profileconditionedon.md) de **MBNProfileExt** para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**&lt;MBNProfileExt&gt;**

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


| Elemento secundario | Descripción | 
|---------------|-------------|
| <a href="element-adminenable.md">AdminEnable</a> | <p>Especifica si el perfil está habilitado administrativamente. Se trata de un nuevo elemento para v4.</p> | 
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>Especifica si el perfil se controla administrativamente. Este elemento es nuevo para v4. El valor de este elemento es <a href="simpletype-roamcontroltype.md"><strong>un valor roamControlType.</strong></a> Se trata de un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</p> | 
| <a href="element-apnid.md">ApnID</a> | <p>Identificador de APN asociado a este perfil. Este elemento es nuevo en v4 y es opcional.</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>Especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.</p><p>Para más información, consulte la documentación del elemento <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>Especifica la configuración de conexión automática que se va a usar para un dispositivo de banda ancha móvil.</p><p>Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p> | 
| <a href="element-context.md">Contexto</a> | <p>Especifica los parámetros necesarios para establecer una conexión de datos.</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Especifica una lista de proveedores de red preferidos en itinerancia.</p><p>Para más información, consulte la documentación del elemento <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</p> | 
| <a href="element-description.md">Descripción</a> | <p>Descripción del perfil.</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>Nombre del proveedor de inicio para la SIM o el dispositivo especificados. Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>Ruta de acceso al archivo de icono de la conexión. La interfaz de usuario de conexión de sistema operativo muestra el icono cuando se realiza una conexión con este perfil.</p><p>Para obtener más información sobre el uso de este elemento, vea la documentación de v1 para <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath.</strong></a></p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>Especifica si este perfil es el perfil predeterminado.</p><p>Para más información sobre este elemento, consulte la documentación de la versión v1 de <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault.</strong></a></p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>Especifica que este perfil es exclusivo de otros perfiles de los mismos conjunto de perfiles. Este elemento es nuevo para v4.</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a> | <p>Especifica que este perfil es un perfil de contexto de PDP adicional de larga duración. Si el valor de este elemento es <strong>true,</strong> <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> también debe establecerse en <strong>true.</strong> Se trata de un nuevo elemento para v4.</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>Especifica que este perfil se usará solo para el aprovisionamiento. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). Este elemento es nuevo para v4.</p><p>Si <strong>IsProvisioningProfile</strong> es true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> debe ser false y <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> debe ser manual.</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Información de configuración para El servicio de mensajería multimedia (MMS).</p><p>Además de establecer los elementos de configuración dentro de este elemento, un perfil mms debe tener la siguiente configuración.</p><ul><li>Su <a href="element-name.md"><strong>elemento Name</strong></a> debe contener un nombre único para todo el sistema.</li><li>Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned.</strong></li><li>Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el VALOR DEID DE LA SIM para la que está pensado este perfil.</li><li>Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>Manual.</strong></li><li>Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósito de MMS.</li><li>Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true.</strong></li></ul> | 
| <a href="element-name.md">Nombre</a> | <p>Nombre del perfil. Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name v1.</strong></a></p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Especifica las condiciones que deben cumplirse para que un perfil sea aplicable.</p><p>Este elemento es nuevo para v4. Permite especificar varios perfiles que se aplican en condiciones diferentes y para que el perfil adecuado se utilice automáticamente cuando sea aplicable. Este elemento es opcional. Si no lo especifica, el perfil siempre es aplicable con respecto a las condiciones enumeradas.</p> | 
| <a href="element-profilecreationtype.md">ProfileCreationType (en MBNProfileExt)</a> | <p>Especifica el creador del perfil.</p><p>Para obtener más información sobre este elemento, vea la documentación del elemento <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Una lista opcional de grupos de perfiles, donde cada grupo incluye perfiles usados para un propósito común.</p><p>Este elemento es nuevo para la versión 4 del esquema.</p><p>Un perfil se puede enumerar en varios grupos.</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>Número de identificación de SIM para dispositivos GSM. Para más información, consulte la documentación del elemento <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> v1.</p> | 
| <a href="element-subscriberid.md">SubscriberID</a> | <p>Identifica el identificador único del perfil.</p><p>En el caso de una red GSM, debe contener el IMSI (Identidad internacional del suscriptor móvil) de la SIM y, en el caso de los dispositivos CDMA, debe contener el valor MIN (número de identificación móvil) del dispositivo.</p><p>Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

Este elemento más externo (documento) no puede estar contenido en ningún otro elemento.

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
