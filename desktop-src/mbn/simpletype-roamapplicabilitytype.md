---
description: RoamApplicabilityType describe las condiciones de itinerancia a las que se aplica un perfil de itinerancia.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: roamApplicabilityType Simple Type
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2ce8f24e0987d5e8463838b33d4f2f2cf859da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474761"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type

RoamApplicabilityType describe las condiciones de itinerancia a las que se aplica un perfil de itinerancia.

Se trata de un atributo más expresivo que [**roamControlType**](simpletype-roamcontroltype.md)y un perfil debe usar **roamControlType** o **roamApplicabilityType,** pero no ambos. (Si un perfil usa ambos, se aplican ambos. El resultado es la intersección de los dos).

Use este atributo para diferenciar entre varios perfiles con condiciones de itinerancia desconexas, para especificar atributos de perfil diferentes para, por ejemplo, inicio frente a itinerancia.

Hay tres posibles estados de registro de inicio o de vuelta:

-   Inicio: registrado en la red principal
-   Asociado: registrado en una red estrechamente afiliada a la red doméstica
-   No asociado: registrado en una red que no está estrechamente afiliada a la red doméstica

El significado preciso de "partner" varía en función de la red, pero representa una relación más cercana con tasas más favorables que un no asociado. Este podría ser el caso si un operador basado en la región tiene una disposición empresarial para usar la red de acceso de radio de otro operador fuera de su área principal. También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la UE) y fuera de ella.

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple roamApplicabilityType** define los valores siguientes.


| Valor | Descripción | 
|-------|-------------|
| NonPartnerOnly | <p>Este perfil solo se usa cuando se itinerancia en una red que no es de asociado</p> | 
| PartnerOnly | <p>Este perfil solo se usa cuando se itinerancia en una red de asociados</p> | 
| HomeOnly | <p>Este perfil solo se usa cuando se encuentra en la red doméstica.</p> | 
| HomeAndPartner | <p>Este perfil solo se usa cuando se encuentra en casa o en una red de asociados.</p> | 
| PartnerAndNonpartner | <p>Este perfil se usa cuando no está en casa (itinerancia en cualquier red).</p> | 
| Itinerancia total | <p>Este perfil se usa en todas las redes</p> | 


 

 



