---
description: Enumeración que describe el tipo de conexión de red donde se aplica un perfil.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simple iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478961"
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


| Valor | Descripción | 
|-------|-------------|
| CellularOnly | <p>El perfil solo es válido para las conexiones de red de telefonía móvil.</p> | 
| CellularAndIwlan | <p>El perfil es válido para las conexiones de telefonía Wi-Fi o de descarga.</p> | 
| IwlanOnly | <p>El perfil es válido solo Wi-Fi conexiones descargados.</p> | 


 

 



