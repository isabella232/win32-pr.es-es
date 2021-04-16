---
description: ModemDMConfigProfile \/ SimIccID (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_SimIccID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SimIccID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0be1e38d5048ce97d6e1c95c4ca07a8406dac36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652417"
---
# <a name="span-idwwan_profile_v4element_1_simiccidspanmodemdmconfigprofilesimiccid-v4"></a><span id="WWAN_profile_v4.element_1_SimIccID"></span>ModemDMConfigProfile \/ SimIccID (v4)

El número de Identifcation de SIM para dispositivos GSM. Para obtener más información, consulte la documentación del elemento [**SimIccID**](./schema-simiccid-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<SimIccID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<SimIccID\>**

## <a name="syntax"></a>Sintaxis

``` syntax
<SimIccID>

  simIccIDType

</SimIccID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento primario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p>
<p>Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Perfil de configuración de DM de módem.</p></td>
</tr>
</tbody>
</table>

 

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

 

 
