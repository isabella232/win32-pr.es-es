---
description: RoamApplicabilityType describe las condiciones de itinerancia para las que se aplica un perfil móvil.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple de roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907918"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo simple de roamApplicabilityType

RoamApplicabilityType describe las condiciones de itinerancia para las que se aplica un perfil móvil.

Este atributo es más expresivo que [**roamControlType**](simpletype-roamcontroltype.md)y un perfil debe utilizar **roamControlType** o **roamApplicabilityType**, pero no ambos. (Si un perfil usa ambos, se aplican ambos. El resultado es la intersección de los dos.

Use este atributo para diferenciar entre varios perfiles con condiciones de itinerancia no contiguas, para especificar atributos de perfil diferentes para, por ejemplo, Inicio o itinerancia.

Hay tres Estados posibles de registro en casa/móvil:

-   Inicio: registrado en la red doméstica
-   Asociado: registrado en una red estrechamente ligada a la red doméstica
-   No asociado: registrado en una red que no está estrechamente asociada con la red doméstica

El significado preciso de "asociado" varía en función de la red, pero representa una relación más estrecha con las tarifas más favorables que un no asociado. Este podría ser el caso si un operador basado en regiones tiene un acuerdo empresarial para usar la red de acceso de radio de otro operador fuera de su área principal. También podría representar la diferencia entre la itinerancia dentro de una región (por ejemplo, la Unión Europea) y fuera de ella.

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

El tipo simple **roamApplicabilityType** define los siguientes valores.

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
<td>NonPartnerOnly</td>
<td><p>Este perfil solo se utiliza cuando se usa la itinerancia en una red no asociada.</p></td>
</tr>
<tr class="even">
<td>PartnerOnly</td>
<td><p>Este perfil solo se utiliza cuando se usa la itinerancia en una red de asociados</p></td>
</tr>
<tr class="odd">
<td>HomeOnly</td>
<td><p>Este perfil solo se usa cuando se está en la red doméstica.</p></td>
</tr>
<tr class="even">
<td>HomeAndPartner</td>
<td><p>Este perfil se usa solo cuando está en casa o en una red de asociados.</p></td>
</tr>
<tr class="odd">
<td>PartnerAndNonpartner</td>
<td><p>Este perfil se usa cuando no está en casa (itinerancia en cualquier red)</p></td>
</tr>
<tr class="even">
<td>AllRoaming</td>
<td><p>Este perfil se usa en todas las redes</p></td>
</tr>
</tbody>
</table>

 

 



