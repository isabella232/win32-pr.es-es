---
description: Describe cómo controla el perfil la itinerancia.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamControlType Simple Type
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475847"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>RoamControlType Simple Type

Describe cómo controla el perfil la itinerancia.

Hay dos posibles estados de registro de perfiles:

-   Asociado: registrado en una red estrechamente afiliada a la red doméstica
-   No asociado: registrado en una red que no está estrechamente afiliada a la red doméstica

El significado preciso de "partner" varía en función de la red, pero representa una relación más cercana con tasas más favorables que un no asociado. Este podría ser el caso si un operador basado en la región tiene una disposición empresarial para usar la red de acceso por radio de otro operador fuera de su área principal. También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la UE) y fuera de ella.

Tenga en cuenta que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) es un atributo más expresivo que **roamControlType** y un perfil debe usar **roamControlType** o **roamApplicabilityType**, pero no ambos. (Si un perfil usa ambos, se aplican ambos. El resultado es la intersección de los dos).

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple roamControlType** define los valores siguientes.


| Value | Descripción | 
|-------|-------------|
| AllRoamAllowed | <p>La itinerancia se permite en redes de asociados y no asociados.</p> | 
| PartnerRoamAllowed | <p>La itinerancia solo se permite en las redes de asociados.</p> | 
| NoRoamAllowed | <p>No se permite itinerancia.</p> | 


 

 



