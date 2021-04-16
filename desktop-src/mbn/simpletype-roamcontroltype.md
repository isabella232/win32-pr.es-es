---
description: Describe cómo el perfil controla la itinerancia.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple de roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705713"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo simple de roamControlType

Describe cómo el perfil controla la itinerancia.

Hay dos Estados posibles de registro de itinerancia:

-   Asociado: registrado en una red estrechamente ligada a la red doméstica
-   No asociado: registrado en una red que no está estrechamente asociada con la red doméstica

El significado preciso de "asociado" varía en función de la red, pero representa una relación más estrecha con las tarifas más favorables que un no asociado. Este podría ser el caso si un operador basado en regiones tiene un acuerdo empresarial para usar la red de acceso de radio de otro operador fuera de su área principal. También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la Unión Europea) y fuera de ella.

Tenga en cuenta que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) es un atributo más expresivo que **roamControlType** y un perfil debe utilizar **roamControlType** o **roamApplicabilityType**, pero no ambos. (Si un perfil usa ambos, se aplican ambos. El resultado es la intersección de los dos.

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

El tipo simple **roamControlType** define los siguientes valores.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllRoamAllowed</td>
<td><p>La itinerancia se permite en redes asociadas y no asociadas.</p></td>
</tr>
<tr class="even">
<td>PartnerRoamAllowed</td>
<td><p>La itinerancia solo se permite en redes de asociados.</p></td>
</tr>
<tr class="odd">
<td>NoRoamAllowed</td>
<td><p>No se permite la itinerancia.</p></td>
</tr>
</tbody>
</table>

 

 



