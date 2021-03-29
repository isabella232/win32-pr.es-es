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
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Perfil de configuración de DM de módem.

## <a name="element-hierarchy"></a>Jerarquía de elemento

**<ModemDMConfigProfile>**

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
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Especifica si el perfil está habilitado de forma administrativa. Se trata de un nuevo elemento para V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Especifica si el perfil está controlado por itinerancia administrativa. Este elemento es nuevo para V4. El valor de este elemento es un valor de <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Este es un elemento opcional; Si no se especifica ningún valor, <strong>AllRoamAllowed</strong> es el valor predeterminado.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>Un ID. de APN asociado a este perfil. Este elemento es nuevo en V4 y es opcional.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Contexto</a></td>
<td><p>Especifica los parámetros necesarios para establecer una conexión de datos.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Nombre</a></td>
<td><p>Nombre del perfil. Para obtener más información, vea la documentación del elemento de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nombre</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>El identificador de conexión de OEM para la configuración de DM de módem.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (en ModemDMConfigProfile)</a></td>
<td><p>Especifica cómo se creó este perfil de DM de módem.</p>
<p>Este valor se usa para decidir si un usuario puede eliminar el perfil. Los usuarios solo pueden eliminar perfiles de <strong>UserProvisioned</strong> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Especifica que este perfil solo está activo cuando la condición de itinerancia actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>El número de Identifcation de SIM para dispositivos GSM. Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</p></td>
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

 

 



