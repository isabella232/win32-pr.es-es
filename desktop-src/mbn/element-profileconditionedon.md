---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0be79fd82b7fa92400a4d828149912cfc1aeb7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987078"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Especifica las condiciones que deben cumplirse para que un perfil sea aplicable.

Este elemento es nuevo para v4. Permite especificar varios perfiles que se aplican en condiciones diferentes y para que el perfil adecuado se utilice automáticamente cuando sea aplicable. Este elemento es opcional. Si no lo especifica, el perfil siempre es aplicable con respecto a las condiciones enumeradas.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;ProfileConditionedOn&gt;**

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


| Elemento secundario | Descripción | 
|---------------|-------------|
| <a href="element-cellularclass.md">CellularClass</a> | <p>Especifica que este perfil está activo solo cuando la clase de telefonía móvil actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP).</p> | 
| <a href="element-imsi.md">IMSI</a> | <p>Especifica que este perfil está activo solo cuando el IMSI actual que se usa en EL IDDEPI es el especificado. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP).</p> | 
| <a href="element-iwlanapplicability.md">IwlanApplicability</a> | <p>Especifica que este perfil solo está activo cuando se conecta a una red IWLAN. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> válido.</p> | 
| <a href="element-ratapplicability.md">CAPACIDADAplicidad</a> | <p>Especifica que este perfil está activo solo cuando el tipo DETE es el especificado. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP).</p> | 
| <a href="element-roamapplicability.md">RoamApplicability</a> | <p>Especifica que este perfil está activo solo cuando la condición de itinerancia actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un valor <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> válido.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p>El <strong>elemento MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p><p>Puede haber más de un elemento MbnProfileExt en un perfil que describa la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el <a href="element-profileconditionedon.md"><strong>elemento secundario ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p> | 


 

## <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



