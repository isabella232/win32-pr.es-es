---
description: MBNProfileExt \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79c35cf8b20a2be85f4ef51e4a3745c9096d9e0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481101"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4)

Especifica que este perfil está activo solo cuando la condición de itinerancia actual es la especificada. De lo contrario, el perfil no es aplicable y no se puede usar para activar un contexto de Protocolo de datos de paquetes (PDP). El valor de este elemento debe ser un [**valor roamApplicabilityType**](simpletype-roamapplicabilitytype.md) válido.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a>Syntax

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Perfil de configuración de DM de módem.</p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Especifica las condiciones que se deben cumplir para que un perfil sea aplicable.</p><p>Este elemento es nuevo para v4. Permite especificar varios perfiles que se aplican en condiciones diferentes y para que el perfil adecuado se utilice automáticamente cuando sea aplicable. Este elemento es opcional. Si no lo especifica, el perfil siempre es aplicable con respecto a las condiciones enumeradas.</p> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



