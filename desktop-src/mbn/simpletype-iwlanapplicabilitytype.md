---
description: Enumeración que describe el tipo de conexión de red donde se aplica un perfil.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ede1e4c360bfd88fa8ca0eb3494a9400f4dfc2a1eb70f7857156caabf7b469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035753"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simple iwlanApplicabilityType

Enumeración que describe el tipo de conexión de red donde se aplica un perfil.

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

El **tipo simple iwlanApplicabilityType** define los valores siguientes.

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
<td><p>El perfil es válido para las conexiones de telefonía móvil Wi-Fi descargadas.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>El perfil es válido solo Wi-Fi conexiones descargados.</p></td>
</tr>
</tbody>
</table>

 

 



