---
description: Enumeración que describe el tipo de conexión de red al que se aplica un perfil.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple de iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542179"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simple de iwlanApplicabilityType

Enumeración que describe el tipo de conexión de red al que se aplica un perfil.

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El tipo simple **iwlanApplicabilityType** define los siguientes valores.

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
<td>CellularOnly</td>
<td><p>El perfil solo es válido para las conexiones de red de telefonía móvil.</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>El perfil es válido para las conexiones móviles o Wi-Fi descargadas.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>Profile solo es válido para las conexiones descargadas de Wi-Fi.</p></td>
</tr>
</tbody>
</table>

 

 



