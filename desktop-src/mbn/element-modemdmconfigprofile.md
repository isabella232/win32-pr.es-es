---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80684cdf2d47d203318afbfd7b5e6bc02de1d3dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982748"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>MódemDMConfigProfile

Perfil de configuración de DM de módem.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**&lt;ModemDMConfigProfile&gt;**

## <a name="syntax"></a>Sintaxis

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

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

`*`   opcional (cero o más)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios


| Elemento secundario | Descripción | 
|---------------|-------------|
| <a href="element-1-adminenable.md">AdminEnable</a> | <p>Especifica si el perfil está habilitado administrativamente. Se trata de un nuevo elemento para v4.</p> | 
| <a href="element-1-adminroamcontrol.md">AdminRoamControl</a> | <p>Especifica si el perfil se controla administrativamente. Este elemento es nuevo para v4. El valor de este elemento es <a href="simpletype-roamcontroltype.md"><strong>un valor roamControlType.</strong></a> Se trata de un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</p> | 
| <a href="element-1-apnid.md">ApnID</a> | <p>Identificador de APN asociado a este perfil. Este elemento es nuevo en v4 y es opcional.</p> | 
| <a href="element-1-context.md">Contexto</a> | <p>Especifica los parámetros necesarios para establecer una conexión de datos.</p> | 
| <a href="element-1-name.md">Nombre</a> | <p>Nombre del perfil. Para obtener más información, vea la documentación del elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name v1.</strong></a></p> | 
| <a href="element-oemconnectionid.md">OemConnectionId</a> | <p>Identificador de conexión de OEM para la configuración de DM del módem.</p> | 
| <a href="element-1-profilecreationtype.md">ProfileCreationType (en ModemDMConfigProfile)</a> | <p>Especifica cómo se creó este perfil de DM de módem.</p><p>Este valor se usa para decidir si un usuario puede eliminar el perfil. Los usuarios solo pueden eliminar <strong>perfiles de UserProvisioned.</strong></p> | 
| <a href="element-1-roamapplicability.md">RoamApplicability</a> | <p>Especifica que este perfil está activo solo cuando la condición de itinerancia actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p> | 
| <a href="element-1-simiccid.md">SimIccID</a> | <p>Número de identificación de SIM para dispositivos GSM. Para más información, consulte la documentación del elemento <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

Este elemento más externo (documento) no puede estar contenido en ningún otro elemento.

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



