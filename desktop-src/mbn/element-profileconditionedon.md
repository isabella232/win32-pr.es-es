---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154201"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Especifica las condiciones que deben satisfacerse para que un perfil sea aplicable.

Este elemento es nuevo para V4. Permite especificar varios perfiles que se aplican en diferentes condiciones y para que el perfil adecuado se use automáticamente cuando sea aplicable. Este elemento es opcional. Si no se especifica, el perfil siempre es aplicable con respecto a las condiciones indicadas.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Sintaxis

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

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
<td><a href="element-cellularclass.md">CellularClass</a></td>
<td><p>Especifica que este perfil solo está activo cuando la clase de teléfono móvil actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>Especifica que este perfil solo está activo cuando el IMSI actual que se usa en ICCID es el especificado. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">IwlanApplicability</a></td>
<td><p>Especifica que este perfil solo está activo cuando se conecta a una red de IWLAN. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> válido.</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">RATApplicability</a></td>
<td><p>Especifica que este perfil solo está activo cuando el tipo RAT es el especificado. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP).</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">RoamApplicability</a></td>
<td><p>Especifica que este perfil solo está activo cuando la condición de itinerancia actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto del Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p></td>
</tr>
</tbody>
</table>

 

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

 

 



