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
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="9593d-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simple de iwlanApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="9593d-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="9593d-104">Enumeración que describe el tipo de conexión de red al que se aplica un perfil.</span><span class="sxs-lookup"><span data-stu-id="9593d-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

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

## <a name="enumeration-values"></a><span data-ttu-id="9593d-105">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="9593d-105">Enumeration values</span></span>

<span data-ttu-id="9593d-106">El tipo simple **iwlanApplicabilityType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="9593d-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9593d-107">Value</span><span class="sxs-lookup"><span data-stu-id="9593d-107">Value</span></span></th>
<th><span data-ttu-id="9593d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9593d-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9593d-109">CellularOnly</span><span class="sxs-lookup"><span data-stu-id="9593d-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="9593d-110">El perfil solo es válido para las conexiones de red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="9593d-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9593d-111">CellularAndIwlan</span><span class="sxs-lookup"><span data-stu-id="9593d-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="9593d-112">El perfil es válido para las conexiones móviles o Wi-Fi descargadas.</span><span class="sxs-lookup"><span data-stu-id="9593d-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9593d-113">IwlanOnly</span><span class="sxs-lookup"><span data-stu-id="9593d-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="9593d-114">Profile solo es válido para las conexiones descargadas de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="9593d-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



